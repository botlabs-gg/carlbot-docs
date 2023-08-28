## Setup
?> Anyone can use the `report` command, and by default Carl-bot will delete the command invocation when used. Instruct your users to use it in the channel where the event they're reporting happened, so your staff can make use of the jump link the report generates.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**reportchannel** \<channel><br><span class="user-permissions">Manage Server</span> | `!reportchannel #reports` | Sets the channel where reports are sent.                   
**report** \<message> | `!report Carl-bot bad` | Sends a report to the report channel.                                    
**setnick** \<user> \<name><br><span class="user-permissions">Manage Nicknames</span> | `!setnick @Carl-bot God` | Changes the user's nickname in the server.                   
**lockdown setup**<br><span class="user-permissions">Manage Roles</span> | `!lockdown setup` | Toggles off <span style="color: red;">Send Messages</span> from all roles execpt @everyone. This is a premium command.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**moderation reportchannel** \<channel><br><span class="user-permissions">Manage Server</span> | `/moderation reportchannel #reports` | Sets the channel where reports are sent.
**moderation report** \<message> | `/moderation report Carl-bot bad` | Sends a report to the report channel              
**moderation setnick** \<user> \<name><br><span class="user-permissions">Manage Nicknames</span> | `/moderation setnick @Carl-bot God` | Changes the user's nickname in the server.
**lockdown setup**<br><span class="user-permissions">Manage Roles</span> | `/lockdown setup` | Toggles off <span style="color: red;">Send Messages</span> from all roles except @everyone. This is a premium command.

<!-- tabs:end -->


## Punishment Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**ban** \<member> [days=2] [reason]<br><span class="user-permissions">Ban Members</span> | `!ban @Carl-bot too good` | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged.                                                                               
**mute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span> | `!mute @Carl-bot 2h30m too good` | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config)                                                                                                        
**hardmute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span> | `!hardmute @Carl-bot 2h` | Similar to mute but also removes all of the roles of the user.
**unmute** \<member> [reason]<br><span class="user-permissions">Manage Roles</span> | `!unmute @Carl-bot served` | Unmutes a member.                                        
**kick** \<member> [reason]<br><span class="user-permissions">Kick Members</span> | `!kick @Carl-bot bot` | Kicks a member.                                                 
**softban** \<member> [days=2] [reason]<br><span class="user-permissions">Ban Members</span> | `!softban @Carl-bot vacation` | Bans and immediately unbans a member to clear message history.
**tempban** \<member> [days=2] [duration] [reason]<br><span class="user-permissions">Ban Members</span> | `!tempban @Carl-bot 1h` | Bans a user for the specified duration.
**massban** [days=2] <members...><br><span class="user-permissions">Ban Members</span> | `!massban @Carl-bot @John` | Bans multiple members.                               
**warn** \<member> [reason]<br><span class="user-permissions">Manage Roles</span> | `!warn @Carl-bot` | Warns a member, DMs them a copy of the reason as well.             
**timeout** \<member> [time] [reason]<br><span class="user-permissions">Timeout Members</span> | `!timeout @Carl-bot 10m` | Timeout a member, DMs them a copy of the reason as well.
**removetimeout** \<member> [reason]<br><span class="user-permissions">Timeout Members</span> | `!removetimeout @Carl-bot served` | Removes timeout from a member.             

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**moderation ban** \<member> [days] [reason]<br><span class="user-permissions">Ban Members</span> | `/moderation ban @Carl-bot 2` | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged.                                                                      
**moderation mute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span> | `/moderation mute @Carl-bot` | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config).
**moderation hardmute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span> | `/moderation hardmute @Carl-bot` | Similar to mute but also removes all of the roles of the user.
**moderation unmute** \<member> [reason]<br><span class="user-permissions">Manage Roles</span> | `/moderation unmute @Carl-bot` | Unmutes a member.                         
**moderation kick** \<member> [reason]<br><span class="user-permissions">Kick Members</span> | `/moderation kick @Carl-bot bot` | Kicks a member.                           
**moderation softban** \<member> [days] [reason]<br><span class="user-permissions">Ban Members</span> | `/moderation softban @Carl-bot vacation` | Bans and immediately unbans a member to clear message history.
**moderation tempban** \<member> [delete_days] [duration] [reason]<br><span class="user-permissions">Ban Members</span> | `/moderation tempban @Carl-bot 1h` | Bans a user for the specified duration.
**moderation massban** \<members> [days]<br><span class="user-permissions">Ban Members</span> | `/moderation massban @Carl-bot @John` | Bans multiple members.            
**moderation warn** \<member> [reason]<br><span class="user-permissions">Manage Roles</span> | `/moderation warn @Carl-bot` | Warns a member, DMs them a copy of the reason as well.
**moderation timeout** \<member> [duration] [reason]<br><span class="user-permissions">Timeout Members</span> | `/moderation timeout @Carl-bot` | Timeout a member, DMs them a copy of the reason as well.
**moderation removetimeout** \<member> [reason]<br><span class="user-permissions">Timeout Members</span> | `/moderation removetimeout @Carl-bot` | Removes timeout from a member.

<!-- tabs:end -->

?> Reason, if provided, shows up in the modlogs and Discord's audit logs. 

### Managing Warns

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**warns** [member]<br><span class="user-permissions">Manage Roles</span> | `!warns @Carl-bot`| Lists all current warnings in the server or of the specified member.          
**removewarn** \<case_id><br><span class="user-permissions">Manage Roles</span> | `!removewarn 17` | Removes a warning by its case id.                                      
**clearwarn**<br><span class="user-permissions">Manage Roles</span>     | `!clearwarn @Carl-bot` | Removes all warnings from a member.                                      

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**moderation warns** [member]<br><span class="user-permissions">Manage Roles</span> | `/moderation warns @Carl-bot` | Lists all current warnings in the server or of the specified member.
**moderation removewarning** \<case_id><br><span class="user-permissions">Manage Roles</span> | `/moderation removewarning 17` | Removes a warning by its case id.          
**moderation clearwarnings**<br><span class="user-permissions">Manage Roles</span> | `/moderation clearwarnings @Carl-bot` | Removes all warnings from a member.            

<!-- tabs:end -->


## User Notes

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**setnote** \<member> \<note><br><span class="user-permissions">Manage Server</span> | `!setnote @Carl-bot favorite bot` | Assigns the note to the member specified.         
**notes** \<member><br><span class="user-permissions">Manage Server</span> | `!notes @Carl-bot` | Displays all of a member's notes.                                          
**removenote** \<note_id><br><span class="user-permissions">Manage Server</span> | `!removenote 56` | Removes a note by number.                                              
**clearnotes** \<member><br><span class="user-permissions">Manage Server</span> | `!clearnotes @Carl-bot` | Removes all notes from a member.                                 

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**notes setnote** \<member> \<note><br><span class="user-permissions">Manage Server</span> | `/notes setnote @Carl-bot favorite bot` | Assigns the note to the member specified.
**notes view** \<member><br><span class="user-permissions">Manage Server</span> | `/notes view @Carl-bot` | Displays all of a member's notes.                                
**notes removenote** \<note_id><br><span class="user-permissions">Manage Server</span> | `/notes removenote 56` | Removes a note by number.                                  
**notes clearnotes** \<member><br><span class="user-permissions">Manage Server</span> | `/notes clearnotes @Carl-bot` | Removes all notes from a member.                     

<!-- tabs:end -->


## Lockdown
!> Locking down a channel denies the @everyone role <span style="color: red;">Send Messages</span> as an override in the specified channel. Any roles explicitly granting <span style="color: red;">Send Messages</span> will override this for anyone with that role. Set up your server correctly by removing <span style="color: red;">Send Messages</span> from all non-mod roles.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**lockdown** [channel=current] [duration]<br><span class="user-permissions">Manage Channels</span> | `!lockdown #general 20m` | Locks the specified channel for the duration, if specified  else indefinitely.
**unlockdown** \<channel><br><span class="user-permissions">Manage Channels</span> | `!unlockdown #general` | Unlocks the specified channel.                                   
**lockdown server** \<duration><br><span class="user-permissions">Manage Channels</span> | `!lockdown server 20m` | Locks all the chanels in the server.                      
**unlockdown server**<br><span class="user-permissions">Manage Channels</span> | `!unlockdown server` | Unlocks all the channels in the server.                                

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**lockdown channel** [channel] [duration] [reason] | `/lockdown channel #general 20m spam` | Locks the specified channel for the duration, if specified  else indefinitely.
**unlockdown channel** [channel]<br><span class="user-permissions">Manage Channels</span> | `/unlockdown channel #general` | Unlocks the specified channel.                    
**lockdown server** [duration] [reason]<br><span class="user-permissions">Manage Channels</span> | `/lockdown server 20m spam` | Locks all the chanels in the server.          
**unlockdown server**<br><span class="user-permissions">Manage Channels</span> | `/unlockdown server` | Unlocks all the channels in the server.                                

<!-- tabs:end -->


## Purging Messages
?> `purge` ignores pinned messages but `cleanup` does not.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**purge** [search=100] [member]<br><span class="user-permissions">Manage Server</span> | `!purge 200` | Purges the number of messages specified. If a member is specified then only that member's messages are purged.
**purge bot** [search=100] [prefix]<br><span class="user-permissions">Manage Server</span> | `!purge bot 20 ?` | Purges bot messages and messages with the specified prefix. 
**purge contains** [search=100] \<substring><br><span class="user-permissions">Manage Server</span> | `!purge contains 12 thanos` | Purges messages containing the substring specified.
**purge all** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge all 13` | Purges the number of messages specified.                               
**purge embeds** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge embeds 12` | Purges messages with embeds.                                     
**purge emoji** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge emoji 6` | Purges messages that contain custom emoji.                          
**purge files** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge files 21` | Purges messages with attachments.                                  
**purge images** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge images 11` | Purges messages with attachments or embeds.                      
**purge links** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge links 15` | Purges messages containing links.                                  
**purge** [mentions\|pings] [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge pings 25` | Purges messages containing pings.                      
**purge** [human\|humans] [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge human 13` | Purges messages except those by bots.                    
**purge reactions** [search=100]<br><span class="user-permissions">Manage Server</span> | `!purge reactions` | Removes all reactions from messages.                          
**cleanup** [search=100]<br><span class="user-permissions">Manage Messages</span> | `!cleanup 8` | Purges messages sent by @Carl-bot.                                          

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**purge bot** \<search> [prefix]<br><span class="user-permissions">Manage Server</span> | `/purge bot 20 ?` | Purges bot messages and messages with the specified prefix.    
**purge contains** \<substring> [search]<br><span class="user-permissions">Manage Server</span> | `/purge contains thanos 12` | Purges messages containing the substring specified.
**purge user** \<member> [search]<br><span class="user-permissions">Manage Server</span> | `/purge user @Carl-bot 20` | Purges messages from a specific member.              
**purge all** \<count><br><span class="user-permissions">Manage Server</span> | `/purge all 13` | Purges the number of messages specified.                                   
**purge embeds** \<count><br><span class="user-permissions">Manage Server</span> | `/purge embeds 12` | Purges messages with embeds.                                         
**purge emoji** [count]<br><span class="user-permissions">Manage Server</span> | `/purge emoji 6` | Purges messages that contain custom emoji.                               
**purge files** \<count><br><span class="user-permissions">Manage Server</span> | `/purge files 21` | Purges messages with attachments.                                      
**purge images** \<count><br><span class="user-permissions">Manage Server</span> | `/purge images 11` | Purges messages with attachments or embeds.                          
**purge links** \<count><br><span class="user-permissions">Manage Server</span> | `/purge links 15` | Purges messages containing links.                                      
**purge mentions** \<count><br><span class="user-permissions">Manage Server</span> | `/purge mentions 25` | Purges messages containing pings.                                
**purge human** \<count><br><span class="user-permissions">Manage Server</span> | `/purge human 13` | Purges messages except those by bots.                                  
**purge reactions** [count]<br><span class="user-permissions">Manage Server</span> | `/purge reactions` | Removes all reactions from messages.                               
**moderation cleanup** [count]<br><span class="user-permissions">Manage Messages</span> | `/moderation cleanup 8` | Purges messages sent by @Carl-bot.                         

<!-- tabs:end -->