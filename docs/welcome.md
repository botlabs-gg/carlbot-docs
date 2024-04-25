## Welcome/Leave/Banmessage

?> We recommend using the [Dashboard](https://carl.gg) as it alllows for easier setup and embeds.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
?> All these messages will be sent to the channel saved with `!set welcome`. Use a command without any text to remove the message.

Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**set welcome** \<channel><br><span class="user-permissions">Manage Server</span> | `!set welcome #welcome` | Sets the channel where welcome, leave and banmsg notification messages will be posted.
[**welcome**\|**greet**] \<text><br><span class="user-permissions">Manage Server</span> | `!welcome Welcome` | Sets up a welcome message that will be sent when a new user joins.
[**leave**\|**farewell**] \<text><br><span class="user-permissions">Manage Server</span> | `!leave Goodbye` | Sets up a leave message that will be sent when a user leaves the server. 
**banmsg** \<text><br><span class="user-permissions">Manage Server</span> | `!banmsg {user} got banned` | Sets up a banmsg message that will be sent when a user gets banned.
[**dmjoin**\|**pmjoin**\|**joindm**\|**joinpm**] \<text><br><span class="user-permissions">Manage Server</span> | `!joindm Welcome` | DMs the user upon joining your server.             
**testgreet**<br><span class="user-permissions">Manage Server</span>     | `!testgreet`      | Sends a welcome, farewell and banmsg for testing.                             

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**welcome** \<message> | `/welcome Welcome` | Sets up a welcome message that will be sent when a new user joins.      
**farewell** [message] | `/farewell Goodbye` | Sets up a leave message that will be sent when a user leaves the server. 
**banmessage** [message] | `/banmessage {user} got banned` | Sets up a banmsg message that will be sent when a user gets banned.
**joindm** [message] | `/joindm Welcome` | DMs the user upon joining your server.                                    
**testgreet**     | `/testgreet`      | Sends a welcome, farewell and banmsg for testing.                            

<!-- tabs:end -->

![Set Welcome](_images/welcome_channel.png ':size=75%')

### Variables
Supports the following variables:
- `{mention}` - Pings the user
- `{user}` - Name of the user
- `{server}` - Name of the server
- `{user(id)}` - ID of the user
- `{user(proper)}` - Name including the last four digits (Carl-bot#1536)
- `{server(members)}` - Number of members in the server (after the event has happened). Use `{ord:{server(members)}}` to turn 8102 into 8,102nd etc
- `{random: lists, separated by commas}` - Random string from the list
- `{math: 1 + 1}` - Calculate stuff

![Welcome Settings](_images/welcome_settings.png ':size=75%')