# Logging

## Quick start

1. Choose a channel with **!log channel &lt;\#channel&gt;**
2. Select which events you want logged with **!log &lt;event&gt;** where event is an event found at the bottom of this page
3. Split up logging into separate channels by using the commands found below

!!! info
    The command **!log aio** automatically creates a category, fills it with five channels and splits up logging into them.

!!! info
    Consider using the website at [https://carl.gg](https://carl.gg)

| Command | Example | Usage |
| :--- | :--- | :--- |
| **log channel \[\#channel\]** | !log channel \#logs | Sets the default channel where logged events go. Leave empty to clear the channel. |
| **log \[event\]** | !log channelcreate | Toggles an event from being logged or not. Leave blank to see current settings. |
| **log messagechannel \[\#channel\]** | !log messagechannel \#msglog | Sets the channel where message events are logged to. |
| **log memberchannel \[\#channel\]** | !log memberchannel \#member-logs | Sets the channel where member events are logged to. |
| **log joinchannel \[\#channel\]** | !log joinchannel \#hello-bye | Sets the channel where the bot logs members joining and leaving to. |
| **log serverchannel \[\#channel\]** | !log serverchannel \#server-updates | Sets the channel where updates to the server itself are logged. |
| **log voicechannel \[\#channel\]** | !log voicechannel \#spying | Sets the channel where members joining/moving between/leaving voice channels are logged. |
| **log ignore &lt;channels/members...&gt;** | !log ignore @Carl\#0001 \#bilderberg \#secret-shhh | Ignores message events posted in the channels or by the members. |
| **log unignore &lt;channels/members...&gt;** | !log unignore @Carl\#0001 \#bilderberg | Unignores the previous ignores. |
| **log \[prefix\|ip\] &lt;prefix&gt;** | !log ip ! | Ignores message deletions, edits and messages within purges starting with the prefixes. |
| **log \[removeprefix\|up\] &lt;prefix&gt;** | !log up ? | Unignores previously added prefixes. |
| **log export** |  | Exports the settings used in this server to be used with the next command. |
| **log \[import\|custom\] &lt;perms&gt;** | !log import 1337 | Imports some settings. |
| **log aio** |  | Creates a category, fills it with five channels and splits up logging into them. |

## Event list

Each event that Carl-bot logs has an associated value and channel. The values are only there for ultra-nerds, don't worry about it.



| Event | Associated logging | Value | Channel |
| :--- | :--- | ---: | :---: |
| delete | Deleted messages | 1 | messagechannel |
| edit | Message edits | 2 | messagechannel |
| purge | Bulk message deletion | 4 | messagechannel |
| discord | Discord invites posted | 2097152 | messagechannel |
| role | Member role updates | 8 | memberchannel |
| avatar | Avatar updates | 32 | memberchannel |
| bans | Bans and unbans | 192 | memberchannel |
| ban | Just bans | 64 | memberchannel |
| unban | Just unbans | 128 | memberchannel |
| join | Name or nickname updates | 256 | joinchannel |
| leave | Name or nickname updates | 512 | joinchannel |
| channels | Channel creations, updates and deletions | 7168 | serverchannel |
| channelcreate | Channel creation | 1024 | serverchannel |
| channelupdate | Channel updates | 2048 | serverchannel |
| channeldelete | Channel deletion | 4096 | serverchannel |
| rolecreate | Roles created | 65536 | serverchannel |
| roleupdate | Updates to roles | 131072 | serverchannel |
| roledelete | Roles deleted | 262144 | serverchannel |
| allroles | Roles being created, updated or deleted | 458752 | serverchannel |
| emoji | Emojis being created, updated or deleted | 1048576 | serverchannel |
| server | Updates to the server itself | 524288 | serverchannel |
| voicejoin | Members joining voice channels | 8192 | voicechannel |
| voicemove | Members changing voice channels | 16384 | voicechannel |
| voiceleave | Members leaving voice channels | 32768 | voicechannel |
| voice | All voice events | 57344 | voicechannel |
| everything | Every single event | 4194303 | depends |
| nothing | Nothing! | 0 | -- |
| default | Some messages and member events | 1019 | depends |

