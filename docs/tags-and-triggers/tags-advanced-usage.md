# Tags - Advanced usage

Tags are easy to use, but very powerful. With some ingenuity you can create your own, dynamic commands. To aid with this, dynamic "blocks" can be added. It is for instance entirely possible to create an 8ball command, a !hug command and many other things using just tags. To build a tag you will need to combine various blocks to tell the tag what you want it to do.

These blocks are split into rough categories based on their behaviour or characteristics:

## Default Arguments

Tagscript comes with a few default arguments. These are:

* `{unix}` - Unix time, useful for math blocks
* `{uses}` - The amount of times the tag has been used
* `{args}` - The arguments \(words used\) after the tag invocation. `!foo bar baz` means {args}==bar baz
* `{user}` - Nickname of the user that used the tag
* `{target}` - Like user, except if you mention someone, this variable works for the mentioned user. If you do not mention someone, target will act as user and reference the tag user.
* `{server}` - The name of the server
* `{mention}` - Mentions the user of the tag

## Discord Object Adapters

Additionally, tagscript 2.0 has better support for various discord objects like members, channels and servers. We call these 'adapters' and let you access certain properties that previously would have been too specific to justify putting in. To access a property, you put the property name in parens like `{user(id)}` Right now for tags there are four object adapters: {user}, {target}, {channel} and {server}.

!!! example "`{user}` & `{target}`"
    * \(avatar\): The user's avatar
    * \(id\): The user's id 
    * \(mention\): a string to mention the user
    * \(created\_at\): yyyy-mm-dd HH.MM.SS 
    * \(joined\_at\): yyyy-mm-dd HH.MM.SS 
    * \(color\): hex code 
    * \(name\): their actual _username_ 
    * \(position\): their position in the role hierarchy

!!! example "`{server}`"

    * \(icon\): server icon link 
    * \(id\): server id 
    * \(owner\): name\#discrim format of the server owner 
    * \(random\): random member 
    * \(randomonline\): random member who is online 
    * \(randomoffline\): random member who is offline 
    * \(members\): number of members: 
    * \(bots\): number of bots 
    * \(humans\): number of humans 
    * \(roles\): number of roles 
    * \(channels\): number of channels 
    * \(created\_at\): when the server was created

!!! example "`{channel}`"

    * \(id\): the channel id 
    * \(topic\): the channel topic 
    * \(slowmode\): the current slowmode delay 
    * \(position\): the channel's position 
    * \(mention\): clickable link to the channel

## Meta Blocks

Meta blocks always execute when included in a tag, and thus only one of each block can be included in the tag structure. Additionally because they always execute, they must stay outside of conditional statements, although conditional statements can be _inside_ some of them.

### Command Blocks

`{cmd: temp stockholm}` `{c:temprole {args(1)} MediaMute {args(2+)}}`

Do you think that `!info` really should be called `!whois`? with command blocks you can do just that.

!!! info "example"
    `!tag + whois {cmd: info {args}}`

### Actions Blocks

* `{dm}` Redirects output as a direct message to the user who uses the command.
* `{delete}` Deletes the message or invocation that triggered the tag.
* `{silence}` Silences the output of any command being used.
* `{override}` This is LITERALLY per-command modrole and allows for some neat new commands.

### Redirection blocks

`{redirect: channel}`

Redirects the output of the tag to the specified channel, the tag creator needs to have send message permissions in the pointed channel.

!!! info "example"
    `{user} says: {args} {redirect:screaming-out-loud}`

### Requirement and Blacklist Blocks

`{require:channel, role} {blacklist:channel, role}`

Both accept roles and channels. Don't include the \# just the channel name.

Also accepts mention formatted channel or role id's. `<#556675168634798111>` or `<@&554342061428572170>`.

Require will limit the tag to executing only when it is used by one of the roles listed, or in one of the channels listed.

Blacklist is the reverse of require. If the tag is used by any role or in any channel listed in the blacklist block, the tag will not execute.

!!! info "Examples" 
    Example: `{require:Cool kids} Word around the office is that {user} is kind of a big deal`

    Example: `{blacklist:Staff} You have no power here`

### React Blocks

**Reacting to the tag**

 `{react: :regional_indicator_f: :cool_roblox_emoji:}`

**Reacting to the author**

  `{reactu: :regional_indicator_f: :cool_roblox_emoji:}`


This will react to the tag {react:} or original message {reactu:} with the emojis placed inside the brackets after the `:`. Use a space to separate multiple emoji.

## Control Blocks

Control blocks control the flow of your tag. They do so by evaluating conditions you provide inside parentheses, and if the condition is true, it will continue executing the payload, or what follows the `:`. To begin, you need to understand how to form a conditional statement.

Each tag will take conditions in parentheses like so: `{if(1==1):hello world}` That would output `hello world`.

In these parentheses you can use the following operators:

* `==` Checks if the two are the exact same.
* `!=` Checks if the two are different in any way.
* `>` and `>=` checks if the number on the left side is larger than the one on the right.
* `<` and `<=` checks if the number on the left side is smaller than the one on the right.

There are 4 basic control blocks:

* `if` - If the condition provided evaluates to true, the payload \(portion after the `:`\) will continue.
* `any` - If any of the conditions provided evaluate to true, the payload will continue. Separate conditions with `|`.
* `all` - If all of the conditions provided evaluate to true, the payload will continue. Separate conditions with `|`.
* `break` - If the condition provided evaluates to true, the tag will stop and output ONLY the payload of the break block. 

Don't use break unless you are sure that is what you want.

For the `if`, `any`, and `all` control blocks, an else statement can be added after the payload using a `|`.

!!! info "Examples"

    * `{if({user(id)}=={target(id)}):You just mentioned yourself or didn't mention anyone.|{user(name)} says {target(name)} is a wuss!}`
    * `{any(condition1|condition2|condition3):Will evaluate to true if any of the conditions is true}`
    * `{all(condition1|condition2|condition3):Will evaluate to true if all of the conditions are true}`
    * `{break(condition):Will return ONLY what's inside this bracket}`

## Variable assignment

Often in a tag you might reference the same string of words, or the same number multiple times. Assigning is your way of assigning a value to a name for reuse across your entire tag.

You can use the following aliases to assign the example `Content` to `varname`:

* `{=(varname):Content}`
* `{assign(varname):Content}`
* `{let(varname):Content}`
* `{var(varname):Content}`

The text inside the parentheses is the identifier for the text beyond the `:`. You can use the value stored in `varname` with brackets: `{varname}`

Nested variables can be rather useful in some situations.

!!! info "Example"
    `{=(t1):A}{=(t2):B}{=(b1):C}{=(b2):D}{=(1stletter):{if({args}>5):t|b}}{=(2ndnumber):{if({args}<20):1|2}}`

allows you to use `{{1stletter}{2ndnumber}}` to conditionally reference any one of the first 4 variables.

Some important information about both variables and `{args}`. You can reference individual elements out of the entire arguments or variable by treating `{args}` or `{example}` like an indexed \(numbered\) list using the spaces as the separators, and putting index \# of the object you want from the list in parentheses following the variable name or args.

If `{example}==The quick brown fox jumps over the lazy dog`, then `{example(1)}==The`, `{example(5+)}==jumps over the lazy dog`, and `{example(+5)}==The quick brown fox jumps`.

You can also specify the separator you want used with a `:`. If `{args}==Hello world, What did you expect, this is an example`, then `{args(1):,}==Hello world`, and `{args(2+):,}==What did you expect, this is an example`.

If the \# you put in the parentheses is out of bounds for the variable or arguments, it will return the full {args}.

You can also use `{1}` to mean `{args(1)}`, `{2}` to mean `{args(2)}` etc...

List and Cycle Blocks: `{list(index):elem, elem2...} {cycle(index):elem, elem2...}`

Lists and cycles are different in the sense that lists that receive an index \(a \#\) out of bounds will return nothing while cycles are basically index = index % elements.length. Both lists and cycles are 0-indexed.

## RNG Blocks

Sometimes you want some random in your tag. The Random block is used to have the tag interpreter pick a random value out of a list of objects you provide.

You can use `,` to separate simple lists, but if you are using commas as part of actual grammar, you must instead use ~ to separate all the possible choices.

#### Random lists

* `{random:1,2,3}`
* `{#:Carl,Michael,Viosmic}`
* `{rand:Hello {user}, how are you?~Howdy {user}}`

Random lists randomly pick an element each time.

#### Seeded Random

* `{random(seed):a,b,c}`
* `{#(same):Carl,Michael,Viosmic}`
* `{rand({user(id)}):Hello {user}, how are you?~Howdy {user}}`

The parameter inside the parentheses after random denotes the Seed value. When the Seed value is provided it will 'lock' the choice to be the same every time it is given that same Seed value. Can be anything.

#### Weighted Random 

`{random:<weight>|a,<weight>|b,<weight>|c}`

Works as a shortcut for writing the same option many times. `{random:4|a,2|b}` is the same as `{random:a,a,a,a,b,b}`.

Range Block: `{range:1-200}`

Picks a random number between 1 and 200 \(inclusive\). Can be seeded just as `{random}`.

50/50 blocks: `{50:Will anyone see me?}`

Has a 50% chance of outputting the payload.

## Manipulation Blocks

These are blocks that manipulate a string in specific ways to achieve different desired results. This can be useful to concatenating a string onto the end of a search URL with the correct encoding for spaces, or to sanitize inputs before using the input in a conditional statement. They have many other potential uses as well as they are very versatile.

* `{lower:HELLO}` will result in `hello`
* `{upper:hello}` will result in `HELLO`
* `{urlencode:hello there}` will result in `hello%20there`
* `{urlencode(+):hello there}` will result in `hello+there`
* `{join(_):hello friends}` will result in `hello_friends`
* `{replace(a,b):carl bot}` will result in `cbrl bot`

## Math Blocks

Supports basic mathematical operations:

* `a+b` addition
* `a-b` subtraction
* `a*b` multiplication
* `a/b` division
* `a%b` modulo
* `abs(a)` absolute value
* `a^b` exponent
* `round(a)` rounds numbers with decimals to the nearest whole number
* `trunc(b)` truncates numbers with decimals, i.e: chopping off the decimals

!!! info "Examples"

    * `{math:1+1/(3^9)}`
    * `{m:round(7.8)+trunc(8.9)}`

## Timedelta Block: 
`{td({unix}): 2020-01-01 00.00.00}`

Calculates the difference between two date, time, or datetime instances. The above example would tell you how long until New Years Day.

## Strf Time Blocks

`{strf(optional datetime): _strftime_}`

Returns the current time formatted according to python's strftime, see [http://strftime.org/](http://strftime.org/) for more information.

!!! info "Examples"

    * `The current year is {strf:%Y} hehe`
    * `Your account was created at {strf({user(created_at)}: %x}`

