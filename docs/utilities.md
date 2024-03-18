## Member Dump
?> **Flags**<br>
`--format/-f` Formatting rules for each member<br>
`--desc/-d` Sort descending<br>
`--has-roles/-r <roles...>` Show members with any of these roles<br>
`--order/-o <by>` Order by name, id, created_at, joined_at or nick<br>
`--limit/-l <number>` Only outputs that number of members<br>
`--has-all-roles <roles...>` Show members with all these roles<br>
`--no-roles` Show members without roles<br>
`--enumerate/-e` Enumerate entries<br>
`--separator/-s <sep>` Changes what the separator is (newline by default, no idea why anyone would want this)<br>
`--dateformat <fmt>` Changes the way dates are represented. See [strftime.org](https://strftime.org) for these flags.<br>

?> **Variables**<br>
Variables follow `--format` or `-f`<br><br>
`%u` is a full name, example: Carl-bot#1234
`%n` is the member's display name (nick if it exists otherwise username)
`%i` is their id
`%c` is the account creation date
`%j` is when they joined the server

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
**dump** Is a special command that deserves its own page.

The syntax is `!dump [role] [args]`<br><span class="user-permissions">Manage Roles</span>

If you're not used to using flags this might be confusing, so here are some examples and what they do:

> **!dump Patrons --enumerate --order id -f %n %c --dateformat %c --limit 10**<br>
Dumps the 10 oldest accounts with the patreon role. Output:<br>
`1. evlsmurf Mon Aug 31 22:23:33 2015`<br>
`2. Hammy:hamster: Thu Sep 24 23:04:31 2015`<br>
`3. iscottnoidea Tue Sep 29 14:35:10 2015`<br>
`4. Ahmad Fri Oct  2 14:22:21 2015`<br>
`5. Zerxion :coffee: Mon Oct  5 07:36:54 2015`<br>
`6. ! Whoozard Tue Oct 20 16:48:57 2015`<br>
`7. Iris Tue Oct 27 01:53:04 2015`<br>
`8. orangespire Thu Oct 29 06:51:14 2015`<br>
`9. aphoenix Mon Nov  9 02:09:03 2015`<br>
`10. Terra Fri Dec  4 02:49:17 2015`

> **!dump -o id --limit 10 --no-roles**<br>
Dumps the 10 oldest accounts without roles. Output:<br>
`Andy#7194 (23572087872421888)`<br>
`macki#9999 (48287434319855616)`<br>
`Xaric123#8510 (49188871384072192)`<br>
`Blackstar#1425 (49212295229739008)`<br>
`Nyte#0001 (49253701973442560)`<br>
`Xin#1645 (49548576702861312)`<br>
`Fondue#7609 (49663303806357504)`<br>
`Ryando#2997 (53163621441605632)`<br>
`ZeroMastery#1287 (53695818749706240)`<br>
`Tristin#7915 (54374655984668672)`

> **!dump -o joined_at -d --limit 1 -r Moderator**<br>
Dumps the moderator who joined most recently

The order of the flags does not matter, below is a more in-depth explanation of how it works.
!["Dump"](_images/dump.png ':size=65%')

<!-- tab:Slash Commands -->
**stats dump** Is a special command that deserves its own page.

The syntax is `/stats dump [role] [query]`<br><span class="user-permissions">Manage Roles</span>

If you're not used to using flags this might be confusing, so here are some examples and what they do:

> **/stats dump @Patrons --enumerate --order id -f %n %c --dateformat %c --limit 10**<br>
Dumps the 10 oldest accounts with the patreon role. Output:<br>
`1. evlsmurf Mon Aug 31 22:23:33 2015`<br>
`2. Hammy:hamster: Thu Sep 24 23:04:31 2015`<br>
`3. iscottnoidea Tue Sep 29 14:35:10 2015`<br>
`4. Ahmad Fri Oct  2 14:22:21 2015`<br>
`5. Zerxion :coffee: Mon Oct  5 07:36:54 2015`<br>
`6. ! Whoozard Tue Oct 20 16:48:57 2015`<br>
`7. Iris Tue Oct 27 01:53:04 2015`<br>
`8. orangespire Thu Oct 29 06:51:14 2015`<br>
`9. aphoenix Mon Nov  9 02:09:03 2015`<br>
`10. Terra Fri Dec  4 02:49:17 2015`

> **/stats dump -o id --limit 10 --no-roles**<br>
Dumps the 10 oldest accounts without roles. Output:<br>
`Andy#7194 (23572087872421888)`<br>
`macki#9999 (48287434319855616)`<br>
`Xaric123#8510 (49188871384072192)`<br>
`Blackstar#1425 (49212295229739008)`<br>
`Nyte#0001 (49253701973442560)`<br>
`Xin#1645 (49548576702861312)`<br>
`Fondue#7609 (49663303806357504)`<br>
`Ryando#2997 (53163621441605632)`<br>
`ZeroMastery#1287 (53695818749706240)`<br>
`Tristin#7915 (54374655984668672)`

> **/dump -o joined_at -d --limit 1 -r Moderator**<br>
Dumps the moderator who joined most recently

The order of the flags does not matter, below is a more in-depth explanation of how it works.
!["Dump"](_images/dump_slash.png ':size=65%')

<!-- tabs:end -->


## Highlights
Highlighting means you will receive a message when your keyword is said in chat. The matching is approximate and works really similarly to discord search (basically, if you search your keyword in discord search, you will find messages that would trigger the highlight, roughly speaking). This may also be called Pager/Paging.

?> You will only be highlighted if you have <span style="color: red;">Manage Messages</span> permission in the channel and if you haven't posted in the past 5 minutes.<br>
For multi-word highlights, it will look for a sequence of words, not a substring.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**highlight**\|**hl**] [+\|add] \<words...><br><span class="user-permissions">Manage Messages</span> | `!hl add carl-bot` | Adds a word that will notify you.                     
**highlight** [m\|match] \<sentence><br><span class="user-permissions">Manage Messages</span> | `!hl match carl-bot is cute` | Tests a sentence and sees which if any words would notify you.
**highlight block** \<members/channels><br><span class="user-permissions">Manage Messages</span> | `!hl block @Carl-bot #general` | Messages sent in this channel/from this user won't notify you.
**highlight unblock** \<members/channels><br><span class="user-permissions">Manage Messages</span> | `!hl unblock #general` | Unblocks the user/channel.                              
**highlight show**<br><span class="user-permissions">Manage Messages</span> | `!hl show` | Shows which words you have set to highlight you.                              
**highlight clear**<br><span class="user-permissions">Manage Messages</span> | `!hl clear` | Removes all of your highlighted words.                                        
**highlight del** \<word><br><span class="user-permissions">Manage Messages</span> | `!hl del carl-bot` | Removes a word from your highlighted words.                                  

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**highlight add** \<word><br><span class="user-permissions">Manage Messages</span> | `/highlight add carl-bot` | Adds a word that will notify you.                             
**highlight matches** \<words><br><span class="user-permissions">Manage Messages</span> | `/highlight matches carl-bot is cute` | Tests a sentence and sees which if any words would notify you. 
**highlight block** \<blocks><br><span class="user-permissions">Manage Messages</span> | `/highlight block @Carl-bot #general` | Messages sent in this channel/from this user won't notify you. 
**highlight unblock** \<unblock><br><span class="user-permissions">Manage Messages</span> | `/highlight unblock #general` | Unblocks the user/channel.                         
**highlight show**<br><span class="user-permissions">Manage Messages</span> | `/highlight show` | Shows which words you have set to highlight you.                              
**highlight clear**<br><span class="user-permissions">Manage Messages</span> | `/highlight clear` | Removes all of your highlighted words.                                     
**highlight remove** \<word><br><span class="user-permissions">Manage Messages</span> | `/highlight remove carl-bot` | Removes a word from your highlighted word.               

<!-- tabs:end -->


## Information
<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**i**\|**info**] [member] | `!i @Carl-bot` | Returns the specified user's name, avatar link, roles, ID, creation date, server join date and some cool related information.
**avatar** [member] [avatar_type=server] | `!avatar @Carl-bot global` | Shows the avatar of a mentioned user or yourself if you don't. If avatar_type is global then it will show the global avatar otherwise it defaults to server avatar if available.
**serverinfo**    | `!serverinfo`     | Displays server information.                                                  
**youngest** [count=5]<br><span class="user-permissions">Manage Server</span> | `!youngest 10` | Ranks up to 25 members by account creation.
**oldest** [count=5]<br><span class="user-permissions">Manage Server</span> | `!oldest 15`   | Ranks up to 25 members by account creation.
[**newmembers**\|**newusers**] [count=5]<br><span class="user-permissions">Manage Server</span> | `!newusers 10` | Ranks up to 25 members by server join date.
[**oldmembers**\|**oldusers**] [count=5]<br><span class="user-permissions">Manage Server</span> | `!oldusers 15` | Ranks up to 25 members by server join date.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**members info** [member] | `/members info @Carl-bot` | Returns the specified user's name, avatar link, roles, ID, creation date, server join date and some cool related information.
**avatars** [user] [global] | `/avatars @Carl-bot true` | Shows the avatar of a mentioned user or yourself if you don't. If global is set true then it will show the global avatar otherwise it defaults to server avatar if available.
**stats serverinfo** | `/stats serverinfo` | Displays server information.                                             
**members youngest** [count=5]<br><span class="user-permissions">Manage Server</span> | `/members youngest 10` | Ranks up to 25 members by account creation.
**members oldest** [count=5]<br><span class="user-permissions">Manage Server</span> | `/members oldest 15`   | Ranks up to 25 members by account creation.
**members newusers** [count=5]<br><span class="user-permissions">Manage Server</span> | `/members newusers 10` | Ranks up to 25 members by server join date.
**members oldusers** [count=5]<br><span class="user-permissions">Manage Server</span> | `/members oldusers 15` | Ranks up to 25 members by server join date.

<!-- tabs:end -->


## Polls
<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**poll** \<question_and_choices><br><span class="user-permissions">Manage Server</span>  | `!poll Is this nice?,Yes,No` | Creates a thumbs up-down poll where users vote with reactions. Use `\|` or `,` to separate the question and choices.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**poll** \<question> [choices]<br><span class="user-permissions">Manage Server</span>  | `/poll Is this nice?` | Creates a thumbs up-down poll where users vote with reactions. Use `\|` or `,` to separate the choices.

<!-- tabs:end -->


## Reminders
?> These reminders require you to have DMs open from at least one server you share with the bot.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**rm**\|**reminder**\|**remindme**\|**timer**] \<when> [about] | `!rm birthday 1d` | Sets up a reminder to send a message reminding you about the thing. If you use a human time like `at noon` it uses UTC.
**reminder mine** | `!rm mine`        | Shows your reminders.                                                        
**reminder** [-\|remove\|del] \<id> | `!rm - 42`| Removes the reminder with that ID.                                           
**subscribe** \<id>     | `!subscribe 97`         | Copies a reminder someone else made.                                          
**reminder clear**| `!rm clear`       | Removes all your reminders from the server or all reminders if used in DMs.
**reminder repeat** \<id> \<interval> | `!rm repeat 247 20d` | Sets a reminder to be repeated.                                  
**reminder when** \<id>     | `!rm when 247`    | Shows some information about a timer created in the server or from you if used in DMs.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | -----------------------------------------------------------------------------
**reminder remindme** \<about> \<when> | `/reminder remindme birthday 1d` | Sets up a reminder to send a message reminding you about the thing. If you use a human time like `at noon` it uses UTC.
**reminder mine** | `/reminder mine`  | Shows your reminders.                                                         
**reminder cancel** \<id> | `/reminder cancel 42`| Removes the reminder with that ID.                                     
**reminder subscribe** \<id> | `/reminder subscribe 97` | Copies a reminder someone else made.                            
**reminder clear** | `/reminder clear` | Removes all your reminders from the server or all reminders if used in DMs.   
**reminder repeat** \<rm_id> [duration] | `/reminder repeat 247 20d` | Sets a reminder to be repeated.                    
**reminder when** \<reminder_id> | `/reminder when 247` | Shows some information about a timer created in the server or from you if used in DMs.

<!-- tabs:end -->


## Giveaways
?> This feature is currently in open beta so expect frequent changes and updates.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**giveaway** \<duration> \<winners> \<prize> [channel=current]<br><span class="user-permissions">Manage Server</span> | `!giveaway 1h10m 2 Nitro #giveaways` | Creates a giveaway for the specified duration, number of winners, prize and optional channel which defaults to the channel that the command is used in.
**giveaway reroll** \<case_id> [members...]<br><span class="user-permissions">Manage Server</span> | `!giveaway reroll 23` | Rerolls the giveaway with the specified case id. Optionally, you can mention the members that should be excluded from the reroll.
**giveaway end** \<case_id><br><span class="user-permissions">Manage Server</span> | `!giveaway end 42` | Ends an ongoing giveaway prematurely. You will be asked if you want to announce winners or not.
**giveaway list** [choice=active]<br><span class="user-permissions">Manage Server</span> | `!giveaway list active` | Shows the list of active/inactive giveaways. 
**giveaway participants** \<case_id><br><span class="user-permissions">Manage Server</span> | `!giveaway participants 4` | Check the users that have participated in a particular giveaway.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**giveaway create** \<duration> \<winners> \<prize> [channel=current]<br><span class="user-permissions">Manage Server</span> | `/giveaway create 10m 1 Nitro` | Creates a giveaway for the specified duration, number of winners, prize and optional channel which defaults to the channel that the command is used in.
**giveaway reroll** \<giveaway_id> [members...]<br><span class="user-permissions">Manage Server</span> | `/giveaway reroll 23 @Carl-bot` | Rerolls the giveaway with the specified giveaway id. Optionally, you can mention the members that should be excluded from the reroll.
**giveaway end** \<giveaway_id><br><span class="user-permissions">Manage Server</span> | `/giveaway end 42` | Ends an ongoing giveaway prematurely. You will be asked if you want to announce winners or not.
**giveaway list** [choice=active]<br><span class="user-permissions">Manage Server</span> | `/giveaway list inactive` | Shows the list of active/inactive giveaways.
**giveaway participants** \<giveaway_id><br><span class="user-permissions">Manage Server</span> | `/giveaway participants 4` | Check the users that have participated in a particular giveaway.

<!-- tabs:end -->