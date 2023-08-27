?> Consider using the [Dashboard](https://carl.gg)

## Quick Setup

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
1. Choose a channel with `!log channel [channel]`
2. Select which events you want to be logged with `!log <event>` where event is an event found in the [Events List](#events-list).
3. Split up logging into separate channel by using the commands found in [Logging Commands](#logging-commands).

?> The `!log aio` command automatically creates a category, fills it with five channels and splits up logging into them.

<!-- tab:Slash Commands -->
1. Choose a channel with `/log channel [channel]`
2. Select which events you want to be logged with `/log config [event]` where event is an event found in the [Events List](#events-list).
3. Split up logging into separate channel by using the commands found in [Logging Commands](#logging-commands).

?> The `/log aio` command automatically creates a category, fills it with five channels and splits up logging into them.

<!-- tabs:end -->


## Logging Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**log channel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log channel #logs` | Sets the default channel where logged events go. Leave empty to clear the channel.
**log** [event<br><span class="user-permissions">Manage Server</span>]   | `!log timeout`    | Toggles an event from being logged or not. Leave blank to see current config.
**log messagechannel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log messagechannel #msglog` | Sets the channel where message events are logged.
**log memberchannel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log memberchannel #memberlog` | Sets the channel where member events are logged.
**log joinchannel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log joinchannel #joinlog` | Sets the channel where the bot logs joining and leaving.
**log serverchannel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log serverchannel #svlog` | Sets the channel where updates to the server are logged.
**log voicechannel** [channel]<br><span class="user-permissions">Manage Server</span> | `!log voicechannel #vclog` | Sets the channl where members joining/moving between/leaving voice channels are logged.
**log ignore** <channels/members...><br><span class="user-permissions">Manage Server</span> | `!log ignore @Carl-bot #staff` | Ignores message events posted in the channels or by the members.
**log unignore** <channels/members...><br><span class="user-permissions">Manage Server</span> | `!log unignore @Carl-bot` | Stops ignoring the channels and/or members.      
**log** <prefix\|ip> \<prefix><br><span class="user-permissions">Manage Server</span> | `!log ip !` | Ignores message deletions, edits and messages within purges starting with the prefix.
**log** <removeprefix\|up> \<prefix><br><span class="user-permissions">Manage Server</span> | `!log up !` | Stops ignoring the prefix in message deletions, edits and messages within purges.
**log export**<br><span class="user-permissions">Manage Server</span>    | `!log export`     | Exports the settings used in this server.                                     
**log** [import\|custom] \<perms><br><span class="user-permissions">Manage Server</span> | `!log import 1337` | Imports the settings.                                        
**log aio**<br><span class="user-permissions">Manage Server</span>       | `!log aio`        | Creates a category, fills it with five channels and splits up logging into them.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**log channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log channel #logs` | Sets the default channel where logged events go. Leave empty to clear the channel.
**log config** [event]<br><span class="user-permissions">Manage Server</span>   | `/log config timeout`    | Toggles an event from being logged or not. Leave blank to see current config.
**log message_channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log message_channel #msglog` | Sets the channel where message events are logged.
**log member_channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log member_channel #memberlog` | Sets the channel where member events are logged.
**log join_channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log join_channel #joinlog` | Sets the channel where the bot logs joining and leaving.
**log server_channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log server_channel #svlog` | Sets the channel where updates to the server are logged.
**log voice_channel** [channel]<br><span class="user-permissions">Manage Server</span> | `/log voice_channel #vclog` | Sets the channl where members joining/moving between/leaving voice channels are logged.
**log ignore** \<ignore><br><span class="user-permissions">Manage Server</span> | `/log ignore @Carl-bot #staff` | Ignores message events posted in the channels or by the members.
**log unignore** \<unignore><br><span class="user-permissions">Manage Server</span> | `/log unignore @Carl-bot` | Stops ignoring the channels and/or members.                 
**log prefix** \<prefix><br><span class="user-permissions">Manage Server</span> | `/log prefix !` | Ignores message deletions, edits and messages within purges starting with the prefix.
**log remove_prefix** \<prefix><br><span class="user-permissions">Manage Server</span> | `/log remove_prefix !` | Stops ignoring the prefix in message deletions, edits and messages within purges.
**log export**<br><span class="user-permissions">Manage Server</span>    | `/log export`     | Exports the settings used in this server.                                     
**log import** \<code><br><span class="user-permissions">Manage Server</span> | `/log import 1337` | Imports the settings.                                                   
**log aio**<br><span class="user-permissions">Manage Server</span>       | `/log aio`        | Creates a category, fills it with five channels and splits up logging into them.

<!-- tabs:end -->

### Events List
Each event that Carl-bot logs has an associated value and channel.

Event                 | Logging                                   | Value         | Channel                           
 -------------------- | ----------------------------------------- | ------------- | --------------------------------- 
delete                | Deleted messages                          | 1             | messagechannel                    
edit                  | Message edits                             | 2             | messagechannel
purge                 | Bulk message deletion                     | 4             | messagechannel
discord               | Discord invites posted                    | 2097152       | messagechannel
role                  | Member role updates                       | 8             | memberchannel                     
avatar                | Avatar updates                            | 32            | memberchannel                     
bans                  | Bans and unbans                           | 192           | memberchannel                     
ban                   | Just bans                                 | 64            | memberchannel                     
unban                 | Just unbans                               | 128           | memberchannel                     
timeout               | Timeouts given                            |               | memberchannel                     
removetimeout         | Timeouts removed                          |               | memberchannel                     
join                  | Joined the server                         | 256           | joinchannel                       
leave                 | Left the server                           | 512           | joinchannel                       
name                  | Name and nickname changes                 |               | memberchannel                     
channels              | Channel creations, updates and deletions  | 7168          | serverchannel                     
channelcreate         | Channel creation                          | 1024          | serverchannel                     
channelupdate         | Channel updates                           | 2048          | serverchannel                     
channeldelete         | Channel deletions                         | 4096          | serverchannel                     
allroles              | Role creations, updates and deletions     | 458752        | serverchannel                     
rolecreate            | Role creation                             | 65536         | serverchannel                     
roleupdate            | Role updates                              | 131072        | serverchannel                     
roledelete            | Role deletions                            | 262144        | serverchannel                     
emoji                 | Emoji creations, updates and deletions    | 1048576       | serverchannel                     
server                | Server updates                            | 524288        | serverchannel                     
voice                 | All voice channel events                  | 57344         | voicechannel                      
voicejoin             | Members joining voice channels            | 8192          | voicechannel                      
voicemove             | Members changing voice channels           | 16384         | voicechannel                      
voiceleave            | Members leaving voice channels            | 32768         | voicechannel                      
everything            | All events                                | 4194303       | depends                           
nothing               | No events                                 | 0             |                                   
default               | Some messages and member events           | 1019          | depends                           


## Modlogs

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**modlog create** [name=modlog]<br><span class="user-permissions">Manage Server</span> | `!modlog create auditlog` | Creates a channel where moderation actions will be logged.
**modlog set** \<channel><br><span class="user-permissions">Manage Server</span> | `!modlog set #modlog` | Sets an already existing channel to send actions to (make sure the bot has the permissions required to post in the channel).
**modlog clear**<br><span class="user-permissions">Manage Server</span>  | `!modlog clear`   | Makes the bot stop logging actions to the channel.                            
**modlog from** \<member><br><span class="user-permissions">Manage Server</span> | `!modlog from @Carl-bot` | Retrieves all infractions for a member with the responsible moderator.
**reason** \<case_id> \<reason><br><span class="user-permissions">Manage Server</span> | `!reason 17 Spamming` | Sets a reason for a modlog entry, useful for cases where you either banned manually or forgot to specify a reason.
**modlog highscores**<br><span class="user-permissions">Manage Server</span> | `!modlog highscores` | Shows the moderators ranked by how many actions they've taken.        
**modlog export** [member]<br><span class="user-permissions">Manage Server</span> | `!modlog export @Carl-bot` | Generates a `.txt` file of your server's modlogs or the modlogs relating to the user specified.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**modlog create** [name]<br><span class="user-permissions">Manage Server</span> | `/modlog create auditlog` | Creates a channel where moderation actions will be logged.
**modlog set** \<channel><br><span class="user-permissions">Manage Server</span> | `/modlog set #modlog` | Sets an already existing channel to send actions to (make sure the bot has the permissions required to post in the channel).
**modlog clear**<br><span class="user-permissions">Manage Server</span>  | `/modlog clear`   | Makes the bot stop logging actions to the channel.                            
**modlog from** \<member><br><span class="user-permissions">Manage Server</span> | `/modlog from @Carl-bot` | Retrieves all infractions for a member with the responsible moderator.
**modlog reason** \<case_id> \<reason><br><span class="user-permissions">Manage Server</span> | `/modlog reason 17 Spamming` | Sets a reason for a modlog entry, useful for cases where you either banned manually or forgot to specify a reason.
**modlog highscores**<br><span class="user-permissions">Manage Server</span> | `/modlog highscores` | Shows the moderators ranked by how many actions they've taken.        
**modlog export** \<all\|member> [member]<br><span class="user-permissions">Manage Server</span> | `/modlog export member @Carl-bot` | Generates a `.txt` file of your server's modlogs or the modlogs relating to the user specified.

<!-- tabs:end -->