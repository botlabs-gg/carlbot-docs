## Twitch
?> **Limits**<br>Non-Premium Carl-bot servers are limited to subscribing to 1 Twitch channel notifications.<br>Premium Carl-bot servers are limited to subscribing to 5 Twitch channel notifications.

![Twitch](_images/twitch.png ':size=100%')

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**twitch** \<name> [channel=current] [message]<br><span class="user-permissions">Manage Server</span> | `!twitch tansmh #live {name} went live` | Binds the streamer's live alerts to the channel.
**twitch add** \<name> [channel=current] [message]<br><span class="user-permissions">Manage Server</span> | `!twitch add tansmh #live {name} went live` | Binds the streamer's live alerts to the channel.
**twitch list**<br><span class="user-permissions">Manage Server</span>   | `!twitch list`    | Shows all the binded streamers and their live status.                         
**twitch online**<br><span class="user-permissions">Manage Server</span> | `!twitch online`  | Shows all currently live streamers.                                           
**twitch remove** \<name><br><span class="user-permissions">Manage Server</span> | `!twitch remove tansmh` | Unbinds a streamer's live alerts.                               
**twitch move** \<name> \<channel><br><span class="user-permissions">Manage Server</span> | `!twitch move tansmh #notifs` | Rebinds a streamer's live alerts to a different channel.
**twitch fmt** \<name> \<message><br><span class="user-permissions">Manage Server</span> | `!twitch fmt tansmh {name} is playing {game}` | Change a streamer's live alert message.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**twitch add** \<name> [channel=current] [format]<br><span class="user-permissions">Manage Server</span> | `/twitch add tansmh #live {name} went live` | Binds the streamer's live alerts to the channel.
**twitch list**<br><span class="user-permissions">Manage Server</span>   | `/twitch list`    | Shows all the binded streamers and their live status.                         
**twitch online**<br><span class="user-permissions">Manage Server</span> | `/twitch online`  | Shows all currently live streamers.                                           
**twitch remove** \<name><br><span class="user-permissions">Manage Server</span> | `/twitch remove tansmh` | Unbinds a streamer's live alerts.                               
**twitch move** \<name> \<channel><br><span class="user-permissions">Manage Server</span> | `/twitch move tansmh #notifs` | Rebinds a streamer's live alerts to a different channel.
**twitch format** \<name> \<format><br><span class="user-permissions">Manage Server</span> | `/twitch format tansmh {name} is playing {game}` | Changes a streamer's live alert message.

<!-- tabs:end -->

### Variables
These variables can be used in the message that is sent when a streamer goes live:
- `{link}` - Stream link
- `{name}` - Streamer's username
- `{game}` - Game being played
- `{everyone}` - Tags @everyone


## YouTube

!> To move the youtube alert channel or format the youtube alert message, you need to head over to the **[Dashboard](https://carl.gg)**.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**youtube**\|**yt**] \<name> [channel=current] [message]<br><span class="user-permissions">Manage Server</span> | `!yt https://youtube.come/ygaming` | Binds the youtuber channel's alerts to the channel.
**youtube sub** \<name> [channel=current] [message]<br><span class="user-permissions">Manage Server</span> | `!yt sub https://youtube.come/ygaming` | Binds the youtuber channel's alerts to the channel.
**youtube list**<br><span class="user-permissions">Manage Server</span>  | `!yt list`        | Shows all the binded youtubers and the connected channels.                    
**youtube unsub** \<name><br><span class="user-permissions">Manage Server</span> | `!yt unsub https://youtube.come/ygaming` | Unbinds a youtuber channel's alerts.           

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | -----------------------------------------------------------------------------
**youtube add** \<name> [channel=current] [format]<br><span class="user-permissions">Manage Server</span> | `/youtube add https://youtube.come/ygaming` | Binds the youtuber channel's alerts to the channel. Can use channel name, handle name, custom channel link or even video links (which is the most accurate way).
**youtube list**<br><span class="user-permissions">Manage Server</span> | `/youtube list` | Shows all the binded youtubers and the connected channels.         
**youtube remove** \<name><br><span class="user-permissions">Manage Server</span> | `/youtube remove https://youtube.come/ygaming` | Unbinds a youtuber channel's alerts.

<!-- tabs:end -->

### Variables
These variables can be used in the message that is sent when a youtube alert is received:
- `{link}` - Channel link
- `{author}` - Channel name
- `{everyone}` - Tags @everyone