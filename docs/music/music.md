# Music

!!! info 
    Music is a premium feature offered to patrons as a way to show my gratitude for helping keep the bot alive

[![become a patron](https://c5.patreon.com/external/logo/become_a_patron_button.png)](https://www.patreon.com/bePatron?u=11251319)

### Music management

| Name | Example | Usage |
| :--- | :--- | :--- |
| **music** | -- | Displays the music settings for the server. |
| **music announce &lt;mode&gt;** | !music announce mention | Changes the bot announcement when a new song is played, settings are off, on and mention which will ping the requester. |
| **music mode &lt;mode&gt;** | !music mode selective | Decides who can use undisruptive music commands. Values are ffa, restrictive, selective and djonly. ffa simply has no rules, everyone can always do anything. Restrictive is what I imagine 99% of servers will want to use as it restricts things like skipping, changing the volume etc. to djs and mods \(manage server\). Selective lets you choose exactly which members can use undisruptive commands. Dj only is what it says on the tin, it only lets mods and djs use any commands. |
| **music \[blacklist\|bl\] &lt;@members...&gt;** | !music bl @Carl\#0001 @Kintark\#0588 | Blacklists some members from using commands, only works for restrictive. |
| **music \[unblacklist\|unbl\] &lt;@members...&gt;**  | !music unbl @Kintark\#0588 | Unblacklists some members. |
| **music \[whitelist\|wl\] &lt;@members...&gt;** | !music wl @Carl\#0001 @Kintark\#0588 | Whitelists from members. Only works for selective. |
| **music \[unwhitelist\|unwl\] &lt;@members...&gt;** | !music unwl @Kintark\#0588 | Unwhitelists some members. |
| **music \[dj\|djrole\] \[role\]** | !music dj MUSIC OVERLORD | Sets the role as the dj role, pass no role to remove. |
| **music \[limit\|sl\|skiplimit\]**  | !music limit 3 | Total number of voteskips required to skip a song. |
| **music \[ratio\|sr\|skipratio\]**  | !music sl 65 | Percentage of non-bot, non-deafened members required to skip a song. |
| **music \[maxqueue\|mq\]**  | !music mq 300 | Limits the maximum size of the queue. |
| **music \[userqueue\|uq\]**  | !music uq 2 | Limits a member to a specified number of songs queued at once. |

#### Music commands

!!! info
    Mod commands are as always in **bold**. Unlike normal commands however, these mod only commands are also available to DJs.

| Name | Example | Usage |
| :--- | :--- | :--- |
| play &lt;name or link&gt; | !play despacito | Plays the song or playlist from youtube \(including livestreams\), bandcamp, soundcloud, vimeo, mixer, direct file links. |
| find &lt;query&gt; | !find momoland | Searches youtube for videos matching your query. You can then respond with the number next to the result to enqueue that result. |
| when &lt;index&gt; | !when 3 | Estimates when the song at the specified index will be played |
| queue | -- | Shows the queue, paginated and the full duration of the playlist. |
| np | -- | Shows the current song being played. |
| _**skip**_ | -- | Skips if you're a mod or if you requested the song, voteskips otherwise. |
| oops | -- | Removes your last queued track \(can be used multiple times\) |
| **movetofront &lt;index&gt;**  | !movetofront 27 | Moves the specified song to the head of the queue but does not play it |
| **skipto &lt;index&gt;**  | !skipto 22 | Skips the song and all songs inbetween to play the specific song |
| **link \[channel\]** | !link \#cool-tunes | The linked channel is where all announcements show up. |
| **seek &lt;time&gt;** | !seek 2:21 seek -27 | If you give it a MM:SS formatted timestamp it will jump to that part of the song, else it works relative to its current position. |
| **stop** | -- | Clears the queue and stops playing the current song. |
| **pause** | -- | Pauses the song. |
| **resume** | -- | Resumes the song. |
| **volume &lt;volume&gt;** | !volume 75 | Changes the volume between 1 and 150% \(100 is pretty loud as you can probably tell\) |
| **shuffle** | -- | Shuffles the playlist. |
| **repeat** | -- | Repeats the playlist \(the normal kind, not just the same song over and over again\) |
| **remove &lt;index&gt;**  | !remove 27 | Removes the song at the specified index |
| **disconnect** | -- | Disconnects the bot from the voice channel and clears the queue. |
| **summon \[channel\]** | !summon jamming | Summons the bot to your channel or to the specified one. |

