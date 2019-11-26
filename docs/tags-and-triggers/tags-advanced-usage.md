# Tags - Advanced usage

Tags are custom commands. They are easy to use and can be very powerful. With some ingenuity, you can create your own. It is for instance entirely possible to create an 8ball command, a hug command and many other things using just tags. Though to do more than just output plaintext, you must configure the command's behavior using what is called Tagscript. Tagscript is a small language the bot interprets, made up of dynamic "blocks". To build a tag you will need to combine various blocks to tell the tag what you want it to do. Some parts of Tagscript can be used elsewhere within Carl-bot, like in Triggers, Autofeeds, and Welcome/Leave/Ban Messages.

## Anatomy of a Tagscript Block

All Tagscript blocks begin with a left curly brace `{`, and end with a right curly brace `}`.

Immediately after the left curly brace is the block _name_, which determines the behavior of the block. Some blocks have aliases or multiple names that produce the same behavior.

Depending on the block name and desired behavior, there might be _parameters_ following the block name. These are put inside parentheses: `(parameters)`

If the block performs an action upon a variable or string, that object, called the *payload*, must follow the parameters or block name. The payload is separated from the rest of the block by a colon. `:`

!!! info "Anatomy of a Tagscript Block"
    `{blockname(parameters):payload}`

Now to get to the blocks themselves. Tagscript blocks are split into rough categories based on their behavior or characteristics:

## Default Arguments

Tagscript comes with a few default arguments. These are:

!!! example "Default Arguments"
    * `{unix}`<br>Current Unix time, useful for math blocks. This only works in Tags.
    * `{uses}`<br>The number of times the tag has been used. This only works in Tags.
    * `{args}`<br>The arguments (words used) after the tag invocation.<br>!foo bar baz means `{args}`==bar baz<br>For triggers `{args}` contains the entire message.
    * `{mention}`<br>Mentions the user of the tag<br><br>
    __Discord Objects:__
    * `{user}`<br>Nickname of the user that used the tag
    * `{target}`<br>Similar to `{user}`, if the tag user mentions someone after the invocation, this variable is the mentioned user's nickname. If nobody is not mentioned, `{target}`==`{user}`.
    * `{server}`<br>The name of the server
    * `{channel}`<br>The name of the channel the tag was used in

### Discord Object Properties

Discord Object blocks, which are listed under Default Arguments above, contain certain properties. To access a property, you specify the property name as the block's parameter, like `{user(id)}`. You can access properties relating to the `{user}`, `{target}`, `{server}` and `{channel}` blocks.

!!! example "{user} & {target} Properties"
    * (avatar): a link to the user's avatar
    * (id): the user's Discord ID, a multi-digit number that is unique to that user. 
    * (mention): a string to mention the user.
    * (created_at): outputs the date the account was created in the format yyyy-mm-dd HH.MM.SS 
    * (joined_at): outputs the date the account joined the server in the format yyyy-mm-dd HH.MM.SS 
    * (color): the hexadecimal color code relating to the user's highest non-default role color.
    * (name): their Discord account username, not their nickname.
    * (proper): their username followed by their discriminator. username#0001
    * (roleids): a list of the role IDs for every role the user has, listed from lowest in the hierarchy to highest
    * (position): their position in the role hierarchy. Position starts with 0 for @everyone at the bottom and increases by 1 for each role in the server going upwards.

!!! example "{server} Properties"
    * (icon): a link to the Server's icon 
    * (id): the Server's ID 
    * (owner): username#discrim format of the server owner 
    * (random): username#discrim format of a random member of the server
    * (randomonline): username#discrim format of a random member who is online 
    * (randomoffline): username#discrim format of a random member who is offline 
    * (members): number of members in the server 
    * (bots): number of bots in the server
    * (humans): number of humans in the server
    * (roles): number of roles in the server
    * (channels): number of channels in the server
    * (created_at): when the server was created in the format yyyy-mm-dd HH.MM.SS 

!!! example "{channel} Properties"
    * (id): the channel's id 
    * (topic): the channel's topic 
    * (slowmode): the current slowmode delay 
    * (position): the channel's position. This is the order in which the channels were created, 0 being the first channel in the server.
    * (mention): clickable link to the channel

## Meta Blocks

Meta blocks change the tag's overall behavior. Where the output is sent, if the invocation is deleted, if any commands blocks used in the tag should output their standard output in addition to the tag's output, who can and can't use the tag, if the bot should react to the invocation or the output, etc.

### Action Blocks

Action blocks change how the invocation, tag output, and command blocks contained within the tag act.

!!! example "Action Blocks"
    * `{delete}`<br>Deletes the message or invocation that triggered the tag.
    * `{silence}`<br>Silences the usual output of any command being used in a command block.
    * `{override}`<br>This instructs the tag to act as if the tag user has the modrole. It still respects role hierarchy. For a tag creator to add this they must have manage server or the modrole.

### Redirection Blocks

Redirects the output of the tag and any command blocks unless otherwise specified in the command. You can only specify one tag output destination, if multiple are provided the latter will override the former.

!!! example "Redirection Blocks"
    * `{dm}`<br>Redirects output as a direct message to the user who uses the tag.
    * `{redirect:channel}`<br>Redirects output to the specified channel. The tag's creator needs to have send message permissions in the pointed channel.
    
The "channel" must either be valid a channel name, a channel id, or a mention formatted channel id `<#556675168634798111>`. 

!!! memo "Example - Redirection Blocks"
    * `{user}` says: `{args}` `{redirect:screaming-out-loud}`
    * `{redirect:186980582863929345}`

### Require & Blacklist Blocks

Restricts tag usage to users with or without roles, to only certain channels, or to exclude specific channels.

!!! example "Require & Blacklist Blocks"
    * `{require(message):channel,role}`<br>Limits the tag to executing when the user has a role listed or when used in a channel listed.
    * `{blacklist(message):channel,role}`<br>Prevents the tag from executing when the user has a role listed or when used in a channel listed.

The message in the parameters is optional. It will display *instead of* the warning emoji if the require block or blacklist block prevent the user from using the tag.

Both accept roles and channels. Entries must be separated by a comma.<br>
They must either be a role/channel name, a role/channel id, or a mention formatted role/channel id `<@&554342061428572170>` or `<#556675168634798111>`.

!!! memo "Examples - Require & Blacklist" 
    * `{require(you're not cool enough):Cool kids}` Word around the office is that `{user}` is kind of a big deal
    * `{blacklist:Staff}` You have no power here

!!! warning "Channel and Role Names"
	Be cautious of using channel and role names in restrict, require, and blacklist blocks. If the channel or role name is changed, the tag must be changed or it will not function as intended. Using IDs makes this a non-issue as channel and role IDs cannot change.

### React Blocks

React Blocks instruct Carl-bot to react to either the invocation or the output. Carl-bot, like all discord accounts, must be in the server where the emoji is hosted to be able to use it. If the emoji is from a server he is in but not the server the tag is in, the emoji id may need to be used instead of just the name. `<:carlpat:590335691968348191>`

React Blocks are limited to using one emoji, but this restriction is lifted for premium servers in which react blocks can use 5 emojis.

!!! example "React Blocks"
    * `{react: :laughing: :fortnight:}`<br>Reacts to the tag's output with the emoji(s) listed.
    * `{reactu: :laughing: :fortnight:}`<br>Reacts to the tag's invocation with the emoji(s) listed.
    
Use a space to separate multiple emoji.

## Command Blocks

Command blocks execute a Carl-bot command. The formatting and syntax do not change compared to how Carl-bot commands are normally used, except you do not include a prefix. Tags are limited to using one command block per tag unless the server is marked as premium, then they can use 3 command blocks per tag. Command blocks cannot use reaction role commands, nor can they call other tags or use tag commands. If the tag's user does not have the permissions required to use the command, Carl-bot will not use it and will output an error message as if they had tried to use the command. As stated in the Action Blocks section, `{override}` can be a useful tool in allowing users that would not otherwise have permission to use a specific command. Command blocks can only be used in Tags.

!!! example "Command Block Aliases"
    * `{cmd:echo {args}}`
    * `{c:role add {user(id)} Verified}`<br>Executes the Carl-bot command in the payload. Block names are synonymous.

Command blocks can also be used to rename a command or create an alias for it.

!!! memo "Example - Command Alias"
    `!tag + whois {cmd:info {args}}`

## Control Blocks

Control blocks control the flow of your tag and determine what payloads are passed to the rest of the tag or block. They are conditional statements that evaluate boolean equations you provide as block parameters. A boolean is a binary variable, having two possible values called *true* and *false*. Boolean equations compare a value on the left of an operator to a value to the right of the operator, and depending on the comparison the operator requires, it evaluates to either true or false. To begin, you need to understand how to form a boolean equation.

!!! summary "Boolean Operators in Tagscript"
    * `==`<br>Evaluates to true if the value on the left is equal to the value on the right.
    * `!=`<br>Evaluates to true if the value on the left is not equal to the value on the right.
    * `>` and `>=`<br>Evaluates to true if the number on the left side is greater than the number on the right.<br>`>=` is greater than or equal.
    * `<` and `<=`<br>Evaluates to true if the number on the left side is less than the number on the right.<br>`<=` is less than or equal.

!!! memo "Examples - Boolean Equations"
    * `cat==dog` This would evalute to false.
    * `tree!=car` This would evaluate to true.
    * `15>20` This would evalute to false.
    * `1<=1` This would evaluate to true.
    
If the boolean equation in the block's parameters evaluates as true, the control block will continue executing the payload. If the boolean equation evaluates as false, the control block will execute the portion of the payload designated by a `|` if it exists, otherwise, it will act as if the control block is null, or does not exist.

!!! example "If Blocks"
    * `{if(booleanEQ):then|else}`<br>If the boolean equation evaluates to true, the block will result in the payload. If the boolean equation evaluates to false, the block will result in the second portion of the payload after the `|` if provided.
    
!!! example "Any Block Aliases"
    * `{any(booleanEQ1|booleanEQ2|etc):then|else}`
    * `{or(booleanEQ1|booleanEQ2|etc):then|else}`<br>If any of the boolean equations provided evaluate to true, the block will result in the payload. If all of the boolean equations evaluate to false, the block will result in the second portion of the payload after the `|` if provided. Separate boolean equations inside the parameters with a pipe character `|`.
    
!!! example "All Block Aliases"
    * `{all(booleanEQ1|booleanEQ2|etc):then|else}`
    * `{and(booleanEQ1|booleanEQ2|etc):then|else}`<br>If all of the boolean equations provided evaluate to true, the block will result in the payload. If any of the boolean equations evaluate to false, the block will result in the second portion of the payload after the `|` if provided. Separate boolean equations inside the parameters with a pipe character `|`.
    
!!! example "Break Block Aliases"
    * `{shortcircuit(booleanEQ):then}`
    * `{short(booleanEQ):then}`
    * `{break(booleanEQ):then}`<br>If the boolean equation evaluates to true, the tag's output will ONLY be the payload of this block.<br>However, Carl-bot commands in command blocks will still execute, and if an embed is defined in the tag's attached embed builder it will still send.

For the `if`, `any`, and `all` control blocks, an optional else statement can be added after the payload by using a pipe character `|`.

If the boolean equation is true the payload is what is between the colon `:` and the pipe `|`. 

If the boolean equation is false, the payload is what is between the pipe `|` and the end of the block `}`. If the control block does not have an else statement and the boolean is false, the Tagscript Engine ignores that control block.

!!! memo "Examples - Control Blocks"
    * `{if({user(id)}=={target(id)}):You didn't mention someone else.|{user} says {target} is a wuss!}`
    * `{any({user(color)}==#5989ab|{user(color)}==#6296ff|{user(color)}==#000001):You're awesome}`
    * `{all({args}>0|{args}<=100):You ate {args} tacos last night|You must input a number between 1 and 100}`
    * `{break({args}==):You did not provide the proper input.}`

## Data Storage & Parsing

Tags cannot save data between invocations. There is no database you can read from or write to. But tags can still store data and values to variables and reference them within the instance of the tag.

### Variable Assignment Blocks

Often in a tag, you might want to reference the same string of words, or the same number multiple times in your tag. Assigning variables is how you would assign a value to a name for reuse across your entire tag.

!!! example "Variable Assignment Block Aliases"
    * `{=(variablename):Content}`
    * `{assign(variablename):Content}`
    * `{let(variablename):Content}`
    * `{var(variablename):Content}`<br>Assigns the content in the payload to the name given in the parameters. Block names are synonymous.

!!! info "Variable Naming"
    You can name variables whatever you would like, but if they share the name of any other Tagscript block or block alias, they will not work to reference the payload. A common error is to name a variable<br>`{=(c):content}`<br>`{c:}` is an alias for the command block. It is recommended that variable names be at least 2 characters long.
    
### Variable Blocks

To call the variable, or use the value stored in `variablename`, you reference the variable's name as a block: `{variablename}`

!!! memo "Example - Nested Variables"
    `{=(t1):A}`<br>`{=(t2):B}`<br>`{=(b1):C}`<br>`{=(b2):D}`<br>`{=(letter):{if({args}>5):t|b}}`<br>`{=(number):{if({args}<20):1|2}}`<br>You could reference any of the first four variables by nesting the last two together as a block.<br>`{{letter}{number}}` would be `{t1}` which is `A` whenever `{args}` is a number greater than 5 and less than 20.

With a variable block, you can reference individual words in the variable, like parsing through a list, by specifying the index, or number, for that word as a parameter. The elements in a list are indexed according to their sequence. Index values for variables start at 1 and increment with each delimiter encountered. A delimiter is a sequence of one or more characters for specifying the boundary between separate, independent strings. The default delimiter for variables in Tagscript is a space. You can also set a custom delimiter for a variable block by specifying it as the variable block's payload.

!!! memo "Example - Variable Parsing"
    `{args}` is the most common variable used in tags, because it is how a tag's creator accesses the information included with the tag's invocation.<br>
    In this example:<br>
    `{args}`==`Carl likes Subway. Today he got a Spicy Italian with - double pepperoni, double salami, provolone, and tomatoes.`<br>
    
    Since space is the default delimiter, you can easily grab individual words<br>
    `{args(1)}==Carl`, `{args(2)}==likes`, and `{args(3)}==Subway.`<br>
    You can also use `{1}` to mean `{args(1)}`, `{2}` to mean `{args(2)}` etc...<br>
    
    You can parse backwards by using index values below 1.<br>
    `{args(0)}==tomatoes.`, `{args(-1)}==and`, `{args(-2)}==provolone,`<br>
    
    Use a `+` before the index to reference every element up to and including the index value.<br>
    `{args(+9)}==Carl likes Subway. Today he got a Spicy Italian`<br>
    Use a `+` after the index to reference the index value and every element after it.<br>
    `{args(-11+)}==a Spicy Italian with - double pepperoni, double salami, provolone, and tomatoes.`<br>
    
    You can grab the sentences separately by redefining the delimiter as a `.`<br>
    `{args(2):.}==Today he got a Spicy Italian with - double pepperoni, double salami, provolone, and tomatoes`<br>
    
    What if you wanted to parse through just the toppings? Set the toppings to another variable then parse that.<br>
    `{=(toppings):{args(2):-}}`<br>
    `{toppings(1):,}== double pepperoni`, `{toppings(2):,}== double salami`, `{toppings(0):,}== and tomatoes.`<br>
    
    If you attempt to reference an element with an index that is out of bounds for the variable, Tagscript will return the whole variable.<br>
    `{args(19)}==Carl likes Subway. Today he got a Spicy Italian with - double pepperoni, double salami, provolone, and tomatoes.`<br>
    If you attempt to reference a span of elements using `+` after an index that is out of bounds for the variable, Tagscript will return nothing.<br>
    `{args(3+):.}==`
    
### List & Cycle Blocks

List and Cycle Blocks are another way to parse through a list of values in Tagscript. They both **strictly** use commas `,` as the delimiter for the list placed in the block's payload. These blocks only functions in Tags.

!!! example "List & Cycle Blocks"
    * `{list(index):elem, elem2...}`<br>Returns the element in the payload the corresponds to the index value in the parameters. Block is null if the index is out of bounds.
    * `{cycle(index):elem, elem2...}`<br>Returns the element in the payload the corresponds to the index value in the parameters. Loops around if the index is out of bounds.

Both lists and cycles use 0 as the index for the first element in the list. List blocks will return null if the index is out of bounds, while a cycle block will loop if the index is greater than the number of elements in the list, essentially `index` = index % list_length. Both allow for backward parsing using negative values. Both blocks will return an error message if the value in parameters is not a number.

!!! memo "Example - List & Cycle Blocks"
    * `{list(3):Carl,Pysnow,Michael,Whoozard,DeaFiore,Viosmic,Pebbles,Kable,Raffael}`==`Whoozard`
    * `{cycle(31):Carl,Pysnow,Michael,Whoozard,DeaFiore,Viosmic,Pebbles,Kable,Raffael}`==`DeaFiore`
    
### Index Blocks

The index block functions inversely compared to other data parsing blocks. Instead of using an index value to return an element from a list or string, it finds the specified element in the payload and returns that element's index value. This block only functions in Tags.

!!! example "Index Blocks"
    `{index(element):list of elements}`<br>Returns the index value of the element in the parameters for the content in the payload.
    
The index block uses 0 as the index for the first element in the payload. The index block always views the payload as being delimited by spaces. If the element specified in the parameters is not found in the payload, the index block will return `-1`. The index block will always return the index for the first instance of the element in the payload, regardless of how many times it is present.

!!! memo "Example - Index Blocks"
    `{index(bread):Which do you like more, bread or chocolate? I like bread more}`==`5`

### Membership Test Operations

Membership test operations are blocks that check a value in the block's parameters against the content in the payload and return a boolean value depending on if the value is present. Again, a boolean is a binary variable, having two possible values called *true* and *false*. They check to see if the parameter is a *member* of the payload. These blocks only function in Tags.

!!! example "In & Contains Blocks"
    * `{in(string):string}`<br>Checks the payload for the presence of the parameter in the payload. Returns *true* if found or *false* if not.
    * `{contains(element):list}`<br>Checks the payload for the presence of the parameter as an element of the payload delimited by spaces. Returns *true* if found or *false* if not.

The in block is the more powerful of the two, as it checks the payload as a string for the parameter string. Contains is useful to check a list for an element, but is bound to checking for only one element and will return false if that exact element is not present.

!!! memo "Example - In & Contains"
    * `{in(spam):Most server rules prohibit spamming.}` would return `true`
    * `{in(spicy italian):Today Carl had a spicy italian sub.}` would return `true`
    * `{in(kable):Kable's beard is majestic}` would return `false` because everything in Tagscript is case-sensitive.
    * `{contains(violet):blue black green grey violet red yellow}` would return `true`
    * `{contains(maple):pine fir aspen oak dogwood}` would return `false`
    
!!! info "In & Contains Blocks"
    Because these blocks return a boolean value, in almost all use cases it is necessary to use them inside Control blocks and check their value by using them as one side of a boolean equation.<br>
    A common use for the contains block is to check if a user has a role.<br>
    `{if({contains(514905279188434972):{user(roleids)}}==true):That's user is a Fake Canadian!}`

## Embed Blocks    

Embed blocks change specific values in a tag's attached embed builder (accessible from [Carl-bot's Dashboard](https://carl.gg)). There are only embed blocks for 1st level JSON attributes which are specified as the block's parameters.

!!! example "Embed Blocks"
    * `{embed(title):string}`<br>Sets the embed's title to the payload.
    * `{embed(URL):https://carl.gg}`<br>Sets the embed title's URL to the payload.
    * `{embed(description):string}`<br>Sets the embed's description to the payload.
    * `{embed(color):#5989ab}`<br>Sets the color of the embed's left vertical bar to the hexidecimal value in the payload.
    * `{embed(timestamp):now}`<br>Sets the embed's timestamp to the value in the payload.
    
The tag's attached embed builder must have a value in it set via the dashboard before an embed block will work to change values in it. Tags created by command line alone will not display an embed even if these embed blocks are present.

The embed block with the timestamp parameter accepts only `now` as a value following the payload. The embed block with the color parameters *must* have a preceding # before the hexadecimal color code.

## Manipulation Blocks

These are blocks that manipulate the string in the payload in specific ways to return different desired results. They can be used to concatenate a string onto the end of a search URL with the correct encoding for spaces, or to sanitize inputs before using the input in a conditional statement, or to remove spaces or specific characters from the payload. They have many potential uses and are versatile. This entire category of blocks only functions in Tags.

### Case Blocks

Case blocks change the case of the text in the payload.

!!! example "Lower & Upper Case Blocks"
    * `{lower:string}`<br>Returns the payload in all lowercase.
    * `{upper:string}`<br>Returns the payload in all uppercase.

These blocks are useful in sanitizing input when checking it against a list that is all one case.

!!! memo "Example - Case Blocks"
    * `{lower:Whoozard is a Wizard}` would return `whoozard is a wizard`
    * `{upper:carl-bot best bot}` would return `CARL-BOT BEST BOT`
    
### URL Encode Blocks

The urlencode block encodes the payload into [Percent-encoding](https://en.wikipedia.org/wiki/Percent-encoding "Wikipedia: Percent-encoding") so it can be included in a URL and understood by the browser of the user that clicked the link.

!!! example "URL Encode Blocks"
    * `{urlencode:payload}`<br>Encodes the payload into percent-encoding.
    * `{urlencode(+):payload}`<br>Encodes the payload into percent-encoding, but replaces spaces with `+` instead of `%20`

!!! memo "Example - URL Encode Blocks"
    * `{urlencode:Hey there, how are you?}` will return `Hey%20there%2C%20how%20are%20you%3F` 
    * `{urlencode(+):Hey there, how are you?}` will return `Hey+there%2C+how+are+you%3F`
    * `https://www.google.com/search?q={urlencode(+):Carl-bot's dashboard}`<br>will result in this link: [Google Search Results](https://www.google.com/search?q=Carl-bot%27s+dashboard "Search for Carl-bot's Dashboard")

### Join & Replace Blocks

Join and replace blocks both involve replacing specific characters or substrings in the payload with other characters or substrings.

!!! example "Join & Replace Blocks"
    * `{join(string):string}`<br>Replaces every space in the payload with the parameters.
    * `{replace(1st string,2nd string):string}`<br>Replaces every instance of the 1st string in the payload with 2nd string.
    
Parameters **must** be set for these blocks, even if they are null. If the 2nd parameter value for the replace block is null, the block will return the payload with every instance of the 1st parameter value removed. If the 1st parameter value for the replace block is null, the block will return the payload with the 2nd parameter value on each side of every character in the payload.

!!! memo "Example - Join & Replace Blocks"
    * `{join(_):hello friends}` will result in `hello_friends`
    * `{join():an example sentence}` will result in `anexamplesentence`
    * `{replace(oo,ee):Goose Tooth Moose}` will result in `Geese Teeth Meese`
    * `/{replace(, ):Carl-Bot}/` will result in `/ C a r l - B o t /`

## Math Blocks

Math blocks perform the mathematical operations in the payload and return the results.

!!! example "Math Block Aliases"
    * `{math:8+9}`<br>
    * `{calc:7-4}`<br>
    * `{+:8/2}`<br>
    * `{m:5*6}`<br>Evaluates the mathematical operations in the payload in the correct order of operations and returns the result. Block names are synonymous.

!!! summary "Supported Mathematical Operations, Functions and Variables"
    * `a+b` Addition
    * `a-b` Subtraction
    * `a*b` Multiplication
    * `a/b` Division
    * `a%b` Modulo
    * `a^b` Exponent
    * `abs(x)` Absolute value of x
    * `round(x)` Rounds x to the nearest whole number
    * `trunc(x)` Truncates x to integer value (chops off decimals)
    * `sin(x)` Returns the sine of x radians
    * `cos(x)` Returns the cosine of x radians
    * `tan(x)` Returns the tangent of x radians
    * `exp(x)` Returns Euler's number raised to the power of x
    * `sgn(x)` Returns the Sign of x. For `x>0` returns 1, for `x=0` returns 0, for `x<0` returns -1.
    * `log(x)` Returns the logarithm of x (base 10)
    * `ln(x)` Returns the natural logarithm of x (base e)
    * `log2(x)` Returns the logarithm of x (base 2)
    * `pi` or `PI` can be used to indicate 𝜋 (3.141592653589793)
    * `e` or `E` can be used to indicate Euler's Number (2.718281828459045)
    
!!! memo "Examples - Math Blocks"
    * `{math:cos(pi)}` would return `-1.0`
    * `{m:round(7.8)+trunc(8.9)}` would return `16`
    
## RNG Blocks

Sometimes you want some random in your tag. These blocks have the Tagscript Engine pick a random value out of a list or range you provide.

### Random Blocks

Random blocks choose a random value from the payload. 

!!! example "Random Block Aliases"
    * `{random(optional_seed):List,of,elements}`
    * `{rand(optional_seed):List~of~elements}`
    * `{#(optional_seed):4|Weighted,2|list,of,3|elements}`<br>Chooses a random value out of the list in the payload. Block names are synonymous.

You can use `,` to separate simple lists, but if you want to use commas as part of an element, you must instead use `~` to separate all the elements.

Seed values are optional. When a seed value is included as a random block's parameter, the block will 'lock' the random choice to the same index value of the payload every time that same seed value is used. This works similar to a cycle block; the seed value might lock to an index value larger than the number of elements in the list and cycle around. Thus, seed_index % list_length might result in different index values being chosen should the same seed be used in random blocks with different list lengths.

Elements in the payload can be weighted if that is desired. Weighting a value is the same as if that value was in the list of elements that many times.<br>`{random:4|a,2|b}` is the same as `{random:a,a,a,a,b,b}`

!!! memo "Example - Random Blocks"
    * `{rand:Hello, how are you?~Howdy}` will return either `Hello, how are you?` or `Howdy`
    * `{#({args}):1,2,3} {#({args}):one,two,three}`<br>will always return elements with matching indices. `1 one`, `2 two`, or `3 three`
    * `{random:99|You lost,You won!}` has a 1% chance of returning `You won!`
    
!!! info "Seed values"
    If you want tag users to receive the same random value each time they use the tag, a common method of doing so is setting the seed value to one of the `{user}` objects immutable properties, like `{user(id)}` or `{user(created_at)}`.

### Range Blocks

Range blocks return a random number in the range of numbers in the payload.

!!! example "Range Block"
    * `{range(optional_seed):Lower#-Higher#}`<br>Returns a random whole number in the specified range
    * `{rangef(optional_seed):Lower#-Higher#}`<br>Returns a random number in the specified range with tenths place decimal numbers.
    
The number range is inclusive, meaning it can pick either endpoint of the specified range as well. It can be seeded similar to the Random block. Rangef will multiply both range endpoints by 10, get a random number in that range, and divide it by 10 to return a number with a tenths place decimal value.
    
!!! memo "Example - Range Blocks"
    * `{range:1-100}` would pick a number from 1 to 100, like 19
    * `{rangef:8-9}` would pick a number from 8.0 to 9.0, like 8.7

### 50/50 Blocks

!!! example "50/50 Block Aliases"
    * `{5050:payload}`
    * `{50:payload}`
    * `{?:payload}`<br>Has a 50% chance of returning the payload, and a 50% chance of being null    

## Time Blocks

Time blocks deal with time and how it is represented, as well as calculating the duration between two dates. All time blocks use and display time values for Coordinated Universal Time (or UTC).

Within this section whenever "DateTime" is mentioned, it means a date and time in the following format:<br>`yyyy-mm-dd HH.MM.SS`

### Strf Blocks

Strf blocks return the time data formatted according to Python's strftime, see [http://strftime.org/](http://strftime.org/) for more information.

!!! example "Strf Blocks"
    * `{strf(optional DateTime or Unix time):strf formatting codes}`<br>Returns the DateTime value listed in the parameters in the format described in the payload.
    
If no parameters are provided, the Tagscript Engine defaults to using the current DateTime as the implied parameters.

!!! memo "Example - Strf Blocks"
    * `December 31st 1999 was a {strf(1999-12-31 23.59.59):%A}` will output `December 31st 1999 was a Friday`
    * `The current time is {strf:%-I:%M %p}` will output `The current time is` followed by whatever the current 12h clock is for UTC, like `2:19 AM`
    * `Your account was created on {strf({user(created_at)}: %x}` will output `Your account was created on 2015/12/24` (for me at least)
    
!!! info "Strf Formats for Reference"
    * `%Y-%m-%d %H.%M.%S` is the DateTime format in strf codes, which can be useful for defining the payload of the timedelta block described below.
    * `{strf:%Y-%m-%dT%X}.000Z` is the strf block for the ISO 8601 format, which is used when setting the timestamp in an embed's JSON. Useful if you're using Carl-bot's `cembed` or `ecembed` commands in a tag.

### Timedelta Blocks

Timedelta blocks calculate the delta, or difference, between two time values.

!!! example "Timedelta Blocks"
    * `{td(optional DateTime or Unix time):DateTime value}`<br>Outputs a string describing the difference in time between the parameters and the payload.
    
If no parameters are provided, the Tagscript Engine defaults to using the current DateTime as the implied parameters.

!!! memo "Example - Timedelta Blocks"
    * `{td:2020-01-01 00.00.00}` as of 2019-11-25 would output `1 month, 5 days and 21 hours`, or the time until Midnight New Years Day
    * `{td({m:trunc({unix}-3600)}):{strf:%Y-%m-%d %H.%M.%S}}` will always output `1 hour` because `{unix}` is the current time and we subtracted 3600 seconds.

## Important Note on Block Behavior

Blocks can be placed and nested inside any parts of other blocks to change or modify their behavior. However, all complete, properly formatted blocks "execute". What does that mean?

As an example, let's say you want to give a user the Verified role if they supply a passphrase. Many readers with some experience using other programming languages would type something like,

!!! fail "Example of what NOT TO DO"
    `{if({args}=={passphrase}):{cmd:role add {user} Verified}}`
    
However, that command block is a complete, properly formatted block. Tagscript does not care that it is the payload of a control block. The command block will execute, and give the user the role even if the control block's parameters are false. This is not a bug, this is intentional and due to how the Tagscript interpreter works. This applies to all blocks. Because we cannot use conditional statements outside complete blocks to negate complete blocks from executing, we must use control blocks _inside_ complete blocks to determine what the contents of the complete blocks are.

Because the control block must be inside the complete block, it creates a small issue. What part of the previous command block should we use as the if block's payload, and how do we avoid the bot complaining when the boolean equation in the if block is incorrect. Here are some of the different correct options available:

!!! success "Correct ways to conditionally run a command"
    * `{cmd:{if({args}=={passphrase}):role add {user} Verified|echo That is not the passphrase}}`<br>This passes the echo command to the command block if the boolean equation is incorrect, so the command block is not empty.
    * `{cmd:role add {user} {if({args}=={passphrase}):Verified|UnVerified}}`<br>This adds an alternate role the command grants if the boolean equation is incorrect, so the role add command is not incomplete.
    * `{=(null):}{{if({args}=={passphrase}):cmd:role add {user} Verified|null}}`<br>This defines the variable null, and double brackets the if statement. Depending on the output of the boolean equation, it will either result in `{cmd:role add {user} Verified}` or `{null}`. The variable null makes sure if the boolean equation is incorrect, the tag does not output a pair of empty brackets `{}`
    
Another common goal is to conditionally set variables to a value.

!!! fail "Example of what NOT TO DO"
    `{if({args}==xmas):{assign(name):Christmas}{assign(date):-12-25}{assign(emoji):🎄}}`
    `{if({args}==vday):{assign(name):Valentine's Day}{assign(date):-02-14}{assign(emoji):❤️}}`
    
This is similar to the example above. Because those variable assignment blocks are complete, properly formatted blocks, Tagscript executes them and assigns the values in their payloads to the variable names in the blocks' parameters. Since the vday assignment line comes after the xmas one, no matter what `{args}` is, `{name}` will be `Valentine's Day`, `{date}` will be `-02-14`, and `{emoji}` will be `❤️`. Again, we must move our control blocks inside our complete blocks.

!!! warning "Technically correct but inefficient"
    `{assign(name):{if({args}==xmas):Christmas|{if({args}==vday):Valentine's Day}}}`<br>
    `{assign(date):{if({args}==xmas):-12-25|{if({args}==vday):-02-14}}}`<br>
    `{assign(emoji):{if({args}==xmas):🎄|{if({args}==vday):❤️}}}`<br>
    Holiday: `{name}`<br>
    Date: `{date}`<br>
    Emoji: `{emoji}`<br>
    While this is correct, it's long, and not really the best way to do this. Think about the data and how it could be better collected.

!!! success "A correct way to conditionally assign variables"
    `{assign(xmas):Christmas|-12-25|🎄}`<br>
    `{assign(vday):Valentine's Day|-02-14|❤️}`<br>
    `{any({args}==xmas|{args}==vday):`<br>
    Holiday: `{{args}(1):|}`<br>
    Date: `{{args}(2):|}`<br>
    Emoji: `{{args}(3):|}}`<br>
    This method assigns all the data that is related to the same holiday to variables split by a pipe symbol, then references each by doublebracketing args when args matches either variable's name.