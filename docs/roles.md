## Autoroles
?> If you have autoroles and reassigned roles, the returning member will receive the union of both.

![Autoroles](_images/autoroles.png ':size=75%') ![Sticky Roles](_images/sticky_roles.png ':size=75%')

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**autorole**\|**autoroles**]<br><span class="user-permissions">Manage Roles</span> | `!autoroles` | Shows which roles will be added upon joining and if the bot will re-add roles when someone leaves and rejoins the server.
**autorole** [readd\|reassign]<br><span class="user-permissions">Manage Roles</span> | `!autorole readd` | Toggles reassigning roles.                                       
**autorole add** \<role><br><span class="user-permissions">Manage Roles</span> | `!autorole add regular` | Autoroles are roles that are given to the user upon joining the server.
**autorole remove** \<role><br><span class="user-permissions">Manage Roles</span> | `!autorole remove admin` | Removes a role from being auto assigned.                     
**autorole** [bl\|blacklist] \<roles...><br><span class="user-permissions">Manage Roles</span> | `!autorole bl admin newbie` | Prevents the mentioned roles from being reassigned.
**autorole unblacklist** <br>\<roles...><br><span class="user-permissions">Manage Roles</span> | `!autorole unblacklist "fortnite expert"` | Removes roles from blacklist.      

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**autorole show**<br><span class="user-permissions">Manage Roles</span> | `/autorole show`  | Shows which roles will be added upon joining and if the bot will re-add roles when someone leaves and rejoins the server.
**autorole reassign**<br><span class="user-permissions">Manage Roles</span> | `/autorole reassignn` | Toggles reassigning roles.                                            
**autorole add** \<role><br><span class="user-permissions">Manage Roles</span> | `/autorole add regular` | Autoroles are roles that are given to the user upon joining the server.
**autorole remove** \<role><br><span class="user-permissions">Manage Roles</span> | `/autorole remove admin` | Removes a role from being auto assigned.                     
**autorole blacklist** \<roles...><br><span class="user-permissions">Manage Roles</span> | `/autorole bl admin newbie` | Prevents the mentioned roles from being reassigned.
**autorole unblacklist** <br>\<roles...><br><span class="user-permissions">Manage Roles</span> | `/autorole unblacklist "fortnite expert"` | Removes roles from blacklist.      

<!-- tabs:end -->

### Timedroles
Autoroles but roles are assigned with a delay.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | -----------------------------------------------------------------------------
[**tr**\|**timedrole**]<br><span class="user-permissions">Manage Roles</span> | `!timedrole`    | Shows the roles being assigned with their delay.                              
**timedrole** [add\|+] \<time> \<role><br><span class="user-permissions">Manage Roles</span> | `!timedrole add 2h newbie` | Adds a role to be added with a delay.           
**timedrole remove** \<role><br><span class="user-permissions">Manage Roles</span> | `!tr remove newbie` | Removes the role from being automatically assigned and also cancels any pending roles.<br>All pending delayed roles with the same delay as the removed role will be removed.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**timedrole show**<br><span class="user-permissions">Manage Roles</span> | `/timedrole show` | Shows the roles being assigned with their delay.                              
**timedrole add** \<time> \<role><br><span class="user-permissions">Manage Roles</span> | `/timedrole add 2h newbie` | Adds a role to be added with a delay.                
**timedrole remove** \<role><br><span class="user-permissions">Manage Roles</span> | `/timedrole remove newbie` | Removes the role from being automatically assigned and also cancels any pending roles.<br>All pending delayed roles with the same delay as the removed role will be removed.

<!-- tabs:end -->



## Reaction Roles
?> Deleted messages are also cleared from the database. Pin the reaction role message to make it immune to purging.

[How to Setup Reaction Roles](https://www.youtube.com/embed/eoeomVNDnII?si=LvMOouqqnlzvIW3n ':include :type=iframe width=560 height=315')


### RR Management

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**rr**\|**reactionrole**\|**reactrole**] [make\|setup]<br><span class="user-permissions">Manage Server</span> | `!rr make` | Starts the interactive setup to get you started with reaction roles.
**rr** [list\|show] [msg_id] | `!rr show` | Shows the emoji-role pairs and their associated message id, useful for rr add. If a message id is specified, it will show additional information about that particular reaction role.
**rr add** [channel]<br><span class="user-permissions">Manage Server</span> \<msg_id> \<emoji> \<role> | `!rr add 123445 👼 @pure` | Adds the emoji-role pair to the message and the database.
**rr addmany** [channel]<br><span class="user-permissions">Manage Server</span> \<msg_id> \<emoji roles...> | `!rr addmany 123456 👼 @pure 💩 @fn` | Works like `rr add` except it adds more than one role at a time.<br>**Separate each emoji-role pair using Shift + Enter**.
**rr remove** \<msg_id> \<role><br><span class="user-permissions">Manage Server</span> | `!rr remove 123456 @fortnite` | Removes an emoji-reaction pair from the specified bot message.
**rr clear** [msg_id]<br><span class="user-permissions">Manage Server</span> | `!rr clear 123456` | If you specify a message id, it removes all the roles from the message and if you don't, it will remove all reaction roles from the server.
**rr bl** \<msg_id> \<roles...><br><span class="user-permissions">Manage Server</span> | `!rr bl 123456 Staff` | Prevents members with this role from picking up roles from the message.
**rr wl** \<msg_id> \<roles...><br><span class="user-permissions">Manage Server</span> | `!rr wl 123456 Staff` | Only members with one of these roles can pick up roles from the message.
**rr unbl** \<msg_id> \<roles...><br><span class="user-permissions">Manage Server</span> | `!rr unbl 123456 Staff` | Removes a blacklisted role from the indicated reaction role message allowing for the role to pick up new roles from the message.
**rr unwl** \<msg_id> \<roles...><br><span class="user-permissions">Manage Server</span> | `!rr unwl 123456 Staff` | Removes a whitelisted role from the indicated reaction role message preventing the role from picking up new roles from the message.
**rr clearbl** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr clearbl 123456` | Removes all roles from your blacklist for that set of reaction roles.
**rr clearwl** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr clearwl 123456` | Removes all roles from your whitelist for that set of reaction roles.
**rr selfdestruct** \<msg_id> \<time><br><span class="user-permissions">Manage Server</span> | `!rr selfdestruct 123456 7d` | Deletes the message and all of its reaction roles after the time is up.
**rr edit** \<msg_id> \<title\|description><br><span class="user-permissions">Manage Server</span> | `!rr edit 123456 Games \| Game notifs` | Edits the title and description, works like it does in the make command.
**rr** [channel\|cc] [name=get-roles]<br><span class="user-permissions">Manage Server</span> | `!rr cc color-roles` | Creates a channel with the sort of permissions you most likely want for a reaction role channel.
**rr fix**<br><span class="user-permissions">Manage Server</span>        | `!rr fix`         | Use this command to have the bot add the reactions missing/cleared.           

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**reactionrole setup**<br><span class="user-permissions">Manage Server</span> | `/reactionrole setup` | Starts the interactive setup to get you started with reaction roles.
**reactionrole show** [message_id] | `/reactionrole show` | Shows the emoji-role pairs and their associated message id, useful for rr add. If a message id is specified, it will show additional information about that particular reaction role.
**reactionrole add** \<message_id> \<emoji> \<role> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole add 👼 @pure #roles` | Adds the emoji-role pair to the message and the database.
**reactionrole addmany** \<message_id> \<emoji-role-pair> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole addmany 👼 @pure 💩 @fn #roles` | Works like `reactionrole add` except it adds more than one role at a time.<br>**Separate each emoji-role pair using Shift + Enter**.
**reactionrole remove** \<role> [message_id]<br><span class="user-permissions">Manage Server</span> | `/reactionrole remove @fortnite 123456` | Removes an emoji-reaction pair from the specified bot message.
**reactionrole purge** [message_id]<br><span class="user-permissions">Manage Server</span> | `/reactionrole purge 123456` | If you specify a message id, it removes all the roles from the message and if you don't, it will remove all reaction roles from the server.
**reactionrole blacklist** \<choice> [message_id] [roles...]<br><span class="user-permissions">Manage Server</span> | `/reactionrole blacklist add 123456 Staff` | Putting in blacklist prevents members with this role from picking up roles from the message.
**reactionrole whitelist** \<choice> [message_id] [roles...]<br><span class="user-permissions">Manage Server</span> | `/reactionrole whitelist remove 123456 Staff` | Putting in whitelist makes it so that only members with one of these roles can pick up roles from the message.
**reactionrole selfdestruct** \<message_id> \<when><br><span class="user-permissions">Manage Server</span> | `/reactionrole selfdestruct 123456 7d` | Deletes the message and all of its reaction roles after the time is up.
**reactionrole edit** \<message_id> \<message_string><br><span class="user-permissions">Manage Server</span> | `/reactionrole edit 123456 Games \| Game notifs` | Edits the title and description, works like it does in the make command.
**reactionrole channel** [channel_name]<br><span class="user-permissions">Manage Server</span> | `/reactionrole channel color-roles` | Creates a channel with the sort of permissions you most likely want for a reaction role channel.
**reactionrole fix**<br><span class="user-permissions">Manage Server</span> | `/reactionrole fix` | Use this command to have the bot add the reactions missing/cleared.      

<!-- tabs:end -->

### RR Types
?> Types are per message and change their behavior. Every message has a type which defaults to normal.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**rr unique** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr unique 123456` | Marks a message as 'unique' meaning a member can only claim one role from this message at a time, this works per message. Automatically removes the old reactions for you.
**rr binding** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr binding 123456` | A combination of rr verify and rr unique. Allowing for members to limit people to one choice ever.
**rr verify** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr verify 123456` | With this enabled, reactions can only assign roles, not take them away. Additionally the bot automatically removes the reaction after the user reacts. This is useful for servers that want a verification reaction
**rr drop** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr drop 123456` | Works sort of like `verify`, except it can only remove roles (and roles are removed when the emoji is added).
**rr normal** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr normal 123456` | This returns the reaction role message back to a normal reaction role message. Meaning any commands applied to it such as verify or unique will be removed.
**rr reversed** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr reversed 123456` | Reacting removes roles, unreacting adds roles.                    
**rr lock** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr lock 123456` | Locks the message preventing any roles from being handed out.             
**rr temp** \<msg_id> \<time><br><span class="user-permissions">Manage Server</span> | `!rr temp 123456 24h` | This is a [Premium](https://www.patreon.com/carlbot) command. This allows for roles to be temporarily be assigned to a member and then removed after the designated amount of time.
**rr link** \<base_id> \<target_id><br><span class="user-permissions">Manage Server</span> | `!rr link 123456 456789` | By linking two or more messages together, only one role from either message can be self-assigned.
**rr unlink** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr unlink 123456` | This breaks apart the entire group created by `rr link`.              
**rr limit** \<msg_id> \<limit><br><span class="user-permissions">Manage Server</span> | `!rr limit 123456 5` | Limits members to picking up x amount of roles from a message.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**reactionrole modify** \<choice> \<message_id><br><span class="user-permissions">Manage Server</span> | `/reactionrole modify unique 123456` | Choose between the different types of reaction roles to apply to the message, all in just a single command.
**reactionrole normal** \<message_id><br><span class="user-permissions">Manage Server</span> | `/reactionrole normal 123456` | This returns the reaction role message back to a normal reaction role message. Meaning any commands applied to it such as verify or unique will be removed.
**reactionrole temp** \<message_id> \<duration><br><span class="user-permissions">Manage Server</span> | `/reactionrole temp 123456 24h` | This is a [Premium](https://www.patreon.com/carlbot) command. This allows for roles to be temporarily be assigned to a member and then removed after the designated amount of time.
**reactionrole links**<br><span class="user-permissions">Manage Server</span> | `/reactionrole links` | Shows the currently linked messages.                                 
**reactionrole link** \<message_ids><br><span class="user-permissions">Manage Server</span> | `/reactionrole link 123456 456789` | By linking two or more messages together, only one role from either message can be self-assigned.
**reactionrole unlink** \<message_id><br><span class="user-permissions">Manage Server</span> | `/reactionrole unlink 123456` | This breaks apart the entire group created by `reactionrole link`.
**reactionrole limit** \<message_id> \<limit><br><span class="user-permissions">Manage Server</span> | `/reactionrole limit 123456 5` | Limits members to picking up the specified amount of roles from a message.

<!-- tabs:end -->

### Advanced
!> These commands come in very handy in certain situations but may cause confusion to users unfamiliar with how Carl-bot's reaction roles work.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**rr move** \<base_id> \<target_id><br><span class="user-permissions">Manage Server</span> | `!rr move 123456 456789` | Moves the reaction roles from one message to another. This works even if the message was purged.
**rr aio** \<channel> \<color> \<title\|description> \<emoji> \<role><br><span class="user-permissions">Manage Server</span> | `!rr aio #roles FF0000`<br>`"title \| description" 👋🏻 hello` | This is meant for power users who wish to create everything with just one command. The title and description have to be enclosed in double quotes.<br>**Separate each emoji-role pair using Shift + Enter**.
**rr aiou** \<channel> \<color> \<title\|description> \<emoji> \<role><br><span class="user-permissions">Manage Server</span> | | All in one command to create a unique reaction role.
**rr aiov** \<channel> \<color> \<title\|description> \<emoji> \<role><br><span class="user-permissions">Manage Server</span> | | All in one command to create a verification reaction role.
**rr aioi** \<channel> \<color> \<title\|description> \<emoji> \<role><br><span class="user-permissions">Manage Server</span> | | All in one command to create an inverse verification reaction role, i.e. one that only removes roles.
**rr fixforeign** \<msg_id><br><span class="user-permissions">Manage Server</span> | `!rr fixforeign 123456` | Makes the bot react to emojis the bot doesn't have access to. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. You have to react to the message with Emojis you want before using this command.
**rr maxroles** \<msg_id> [\<role> \<number>...]<br><span class="user-permissions">Manage Server</span> | `!rr maxroles 123456 DPS 10` | Limit the number of each role in a reaction role. This actually checks for how many people have the role, not how many reactions there are.
**rr** [colour\|color] \<msg_id> \<color><br><span class="user-permissions">Manage Server</span> | `!rr color 123456 #FF0000` | Changes the accent color of the specified bot message.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**reactionrole move** \<base_id> \<target_id> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole move 123456 456789` | Moves the reaction roles from one message to another.
**reactionrole aio** \<type> \<color> \<text> \<emoji_role_pair> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole aio default FF0000`<br>`title \| description 👋🏻 hello` | This is meant for power users who wish to create everything with just one command.
**reactionrole fixforeign** \<message_id> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole fixforeign 123456` | Makes the bot react to emojis the bot doesn't have access to. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. You have to react to the message with Emojis you want before using this command.
**reactionrole maxroles** \<message_id> [roles_and_limits]<br><span class="user-permissions">Manage Server</span> | `/reactionrole maxroles 123456 DPS 10` | Limit the number of each role in a reaction role. This actually checks for how many people have the role, not how many reactions there are.
**reactionrole color** \<message_id> \<color> [channel]<br><span class="user-permissions">Manage Server</span> | `/reactionrole color 123456 #FF0000` | Changes the accent color of the specified bot message.

<!-- tabs:end -->


## Role Management
?> These commands are for administrators to manage role assignments in their servers. The bot might mention that you require additional permissions despite having <span style="color: red;">Manage Roles</span>. To fix this, make sure both you and the bot have roles higher in the role heirarchy than the role you are trying to assign.

### Role Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**role create** \<name> [color] [mentionable=False] [hoist=False]<br><span class="user-permissions">Manage Roles</span> | `!role create bot #FF0000 true true` | Creates a role. Hoist decides if it shows up in the sidebar or not.
**allroles**<br><span class="user-permissions">Manage Roles</span> | `!allroles` | Displays list of roles in the server.   
**role** \<member> \<role><br><span class="user-permissions">Manage Roles</span> | `!role @Carl-bot bot` | Adds/removes a role from the specified member.                   
**role add** \<member> \<role><br><span class="user-permissions">Manage Roles</span> | `!role add @Carl-bot bot` | Adds a role to the specified member.                     
**role remove** \<member> \<role><br><span class="user-permissions">Manage Roles</span> | `!role remove @Carl-bot bot` | Removes a role from the specified member.          
**role color** \<role> \<color><br><span class="user-permissions">Manage Roles</span> | `!role color bot #FF0000` | Changes the color of a role.                            
**role info** \<role> | `!role info bot` | Displays the role's Name, Member Count, Color, and when it was created.   
**role** [custom\|c] \<member> \<custom_string><br><span class="user-permissions">Manage Roles</span> | `!role custom @Carl-bot +bot -human` | Gives the ability to add and remove roles within a single command, useful for removing a pending role whilst granting a member/joined role.
**rolediagnose** | `!rolediagnose`  | Diagnose a role.   
**temprole** \<member> \<time> \<role><br><span class="user-permissions">Manage Roles</span> | `!temprole @Carl-bot 2h bot` | Adds a role for some time and removes it after the time is up. Time can be either before or after the role name.
**temprole** [custom\|c] \<member> \<time> \<custom_string><br><span class="user-permissions">Manage Roles</span> | `!temprole c @Carl-bot 3h +bot -human` | Gives the ability to add and remove roles temporarily within a single command, useful for removing roles for a period of time.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**role create** \<name> [color] [mentionable=False] [hoist=False]<br><span class="user-permissions">Manage Roles</span> | `/role create bot #FF0000 true true` | Creates a role. Hoist decides if it shows up in the sidebar or not. 
**role allroles** | `/role allroles` | Displays list of roles in the server.
**role add** \<user> \<role><br><span class="user-permissions">Manage Roles</span> | `/role add @Carl-bot bot` | Adds a role to the specified member.                       
**role remove** \<user> \<role><br><span class="user-permissions">Manage Roles</span> | `/role remove @Carl-bot bot` | Removes a role from the specified member.            
**role color** \<role> \<color><br><span class="user-permissions">Manage Roles</span> | `/role color bot #FF0000` | Changes the color of a role.                            
**role info** \<role> | `/role info bot` | Displays the role's Name, Member Count, Color, and when it was created.    
**role custom** \<member_and_roles><br><span class="user-permissions">Manage Roles</span> | `/role custom @Carl-bot +bot -human` | Gives the ability to add and remove roles within a single command, useful for removing a pending role whilst granting a member/joined role.
**role diagnose** | `/role diagnose`  | Diagnose a role.                                                              
**temprole add** \<member> \<duration_and_role><br><span class="user-permissions">Manage Roles</span> | `/temprole add @Carl-bot 2h bot` | Adds a role for some time and removes it after the time is up. Time can be either before or after the role name.
**temprole custom** \<member> \<time_and_roles><br><span class="user-permissions">Manage Roles</span> | `/temprole custom @Carl-bot 3h +bot -human` | Gives the ability to add and remove roles temporarily within a single command, useful for removing roles for a period of time.

<!-- tabs:end -->

### Rank Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**ranks**         | `!ranks`          | Lists all whitelisted ranks.                                                  
**addrank** \<roles...><br><span class="user-permissions">Manage Roles</span> | `!addrank members newbie` | Adds one or more roles to the list of whitelisted ranks that members can assign to themselves.
**removerank** \<roles...><br><span class="user-permissions">Manage Roles</span> | `!removerank members newbie` | Removes one or more roles from the list of whitelisted ranks, so that it can no longer be self assigned.
**rank** \<role>  | `!rank newbie`  | Adds/removes the role to the person who used the command. Requires the role to be on the list of whitelisted ranks.
**rank** [custom\|c] \<custom_string> | `!rank custom +pro -newbie` | Adds/removes multiple roles to the person using the command. Requires the role to be on the list of whitelisted ranks.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**rank allranks** | `/rank allranks`  | Lists all whitelisted ranks.                                                  
**rank addrank** \<roles...><br><span class="user-permissions">Manage Roles</span> | `/rank addrank members newbie` | Adds one or more roles to the list of whitelisted ranks that members can assign to themselves.
**rank removerank** \<roles...><br><span class="user-permissions">Manage Roles</span> | `/rank removerank members newbie` | Removes one or more roles from the list of whitelisted ranks, so that it can no longer be self assigned.
**rank custom** \<roles...> | `/rank custom +pro -newbie` | Adds/removes multiple roles to the person using the command. Requires the role to be on the list of whitelisted ranks.

<!-- tabs:end -->

### Bulk Role Management
!> Only one bulk assignment can be used at a time. Once started, a bulk role management command will give you an estimated time of completion and the process cannot be stopped.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**role all** \<role><br><span class="user-permissions">Manage Roles</span> | `!role all newb` | Adds a role to every single member.                                         
**role humans** \<role><br><span class="user-permissions">Manage Roles</span> | `!role humans members` | Adds a role to all non-bots.                                       
**role in** \<base_role> \<assigned_role><br><span class="user-permissions">Manage Roles</span> | `!role in valorant gamers` | Assigns a role to all members with the base role.
**role rall** \<role><br><span class="user-permissions">Manage Roles</span> | `!role rall admin` | Removes a role from all members.          
**role** [removeall\|purge\|clear] \<member><br><span class="user-permissions">Manage Roles</span> | `!role removeall @Carl-bot` | Removes all roles from a member.         
**role rbots** \<role><br><span class="user-permissions">Manage Roles</span> | `!role rbots members` | Removes a role from all bots.                                        
**role rhumans** \<role><br><span class="user-permissions">Manage Roles</span> | `!role rhumans robots` | Removes a role from all humans.                                   
**role rin** \<base_role> \<role><br><span class="user-permissions">Manage Roles</span> | `!role rin fortnite gamers` | Removes a role from all members with the base role.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**role all** \<role><br><span class="user-permissions">Manage Roles</span> | `/role all newb` | Adds a role to every single member.                                         
**role humans** \<role><br><span class="user-permissions">Manage Roles</span> | `/role humans members` | Adds a role to all non-bots.                                       
**role in** \<base_role> \<new_role><br><span class="user-permissions">Manage Roles</span> | `!role in valorant gamers` | Assigns new role to all members with the base role.
**role rall** \<role><br><span class="user-permissions">Manage Roles</span> | `/role rall admin` | Removes a role from all members.                                         
**role removeall** \<user><br><span class="user-permissions">Manage Roles</span> | `/role removeall @Carl-bot` | Removes all roles from a member.                           
**role removebots** \<role><br><span class="user-permissions">Manage Roles</span> | `/role removebots members` | Removes a role from all bots.                              
**role removehumans** \<role><br><span class="user-permissions">Manage Roles</span> | `/role removehumans robots` | Removes a role from all humans.                         
**role removein** \<base_role> \<new_role><br><span class="user-permissions">Manage Roles</span> | `/role removein fortnite gamers` | Removes new role from all members with the base role.

<!-- tabs:end -->