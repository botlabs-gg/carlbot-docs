?> After you make a Starboard channel, your members can react to any message with a ⭐ `:star:` which counts as a vote to display that message as a post on the Starboard. Once the message gets enough reactions, Carl-bot posts it onto the Starboard. By default, a user's reaction on their own post doesn't count.

![Starboard Settings](_images/starboard_settings.png ":size=75%")

<!-- tabs:start -->

<!-- tab:Prefix Commands -->

| Name                                                                                     | Example                    | Usage                                                                                                |
| ---------------------------------------------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------- |
| **starboard** [channel=starboard]<br><span class="user-permissions">Manage Server</span> | `!starboard #stars`        | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`.           |
| **star limit** \<number><br><span class="user-permissions">Manage Server</span>          | `!star limit 3`            | Sets the amount of reactions required for a post to get posted on the Starboard.                     |
| **star nsfw**<br><span class="user-permissions">Manage Server</span>                     | `!star nsfw`               | Toggles stars in NSFW channels.                                                                      |
| **star self**<br><span class="user-permissions">Manage Server</span>                     | `!star self`               | Toggles being able to star your own posts.                                                           |
| **star** [server\|stats\|top] [member]                                                   | `!star stats @Carl-bot`    | Shows some information about the server's or specified member's starred posts and giving pattern.    |
| **star show** \<message_id>                                                              | `!star show 123456`        | Shows a starred post from the Starboard in the channel the command was used in.                      |
| **star** [jump\|source]<br><span class="user-permissions">Manage Server</span>           | `!star jump`               | Sends the direct link to the starred message.                                                        |
| **star autostar**<br><span class="user-permissions">Manage Server</span>                 | `!star autostar`           | This is a [Premium](https://carl.gg/get-premium) command. Automatically stars new Starboard entries. |
| **star blacklist** \<channels><br><span class="user-permissions">Manage Server</span>    | `!star blacklist #staff`   | Blocks channels from having their messages starred.                                                  |
| **star unblacklist** \<channels><br><span class="user-permissions">Manage Server</span>  | `!star unblacklist #staff` | Unblocks channels from having their messages starred.                                                |
| **star config**<br><span class="user-permissions">Manage Server</span>                   | `!star config`             | View Starboard configuration for server.                                                             |
| **star lock**<br><span class="user-permissions">Manage Server</span>                     | `!star lock`               | Locks the Starboard making it completely uninteractive.                                              |
| **star random**                                                                          | `!star random`             | Shows a random starred message.                                                                      |
| **star remove**<br><span class="user-permissions">Manage Server</span>                   | `!star remove`             | Removes a channel as starboard.                                                                      |
| **star emoji** [emoji]<br><span class="user-permissions">Manage Server</span>            | `!star emoji 🔥`           | Sets or resets an emoji for starboard. This is a [Premium](https://carl.gg/get-premium) command.     |

<!-- tab:Slash Commands -->

| Name                                                                                       | Example                     | Usage                                                                                                |
| ------------------------------------------------------------------------------------------ | --------------------------- | ---------------------------------------------------------------------------------------------------- |
| **stars setup** [channel=starboard]<br><span class="user-permissions">Manage Server</span> | `/stars setup #stars`       | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`.           |
| **stars limit** \<limit><br><span class="user-permissions">Manage Server</span>            | `/stars limit 3`            | Sets the amount of reactions required for a post to get posted on the Starboard.                     |
| **stars nsfw**<br><span class="user-permissions">Manage Server</span>                      | `/stars nsfw`               | Toggles embedding images from starred messages in NSFW channels.                                     |
| **stars self**<br><span class="user-permissions">Manage Server</span>                      | `/stars self`               | Toggles being able to star your own posts.                                                           |
| **stars server**                                                                           | `/stars server`             | Displays stats about the server's starboard.                                                         |
| **stars stats** [member]                                                                   | `/stars stats @Carl-bot`    | Shows some information about the server's or specified member's starred posts and giving pattern.    |
| **stars show** \<message_id>                                                               | `/stars show 123456`        | Shows a starred post from the Starboard in the channel the command was used in.                      |
| **stars jump**<br><span class="user-permissions">Manage Server</span>                      | `/stars jump`               | Sends the direct link to the starred message.                                                        |
| **stars autostar**<br><span class="user-permissions">Manage Server</span>                  | `/stars autostar`           | This is a [Premium](https://carl.gg/get-premium) command. Automatically stars new Starboard entries. |
| **stars blacklist** \<channels><br><span class="user-permissions">Manage Server</span>     | `/stars blacklist #staff`   | Blocks channels from having their messages starred.                                                  |
| **stars unblacklist** \<channels><br><span class="user-permissions">Manage Server</span>   | `/stars unblacklist #staff` | Unblocks channels from having their messages starred.                                                |
| **stars config**<br><span class="user-permissions">Manage Server</span>                    | `/stars config`             | View Starboard configuration for server.                                                             |
| **stars lock**<br><span class="user-permissions">Manage Server</span>                      | `/stars lock`               | Locks the Starboard making it completely uninteractive.                                              |
| **stars random**                                                                           | `/stars random`             | Shows a random starred message.                                                                      |
| **stars remove**<br><span class="user-permissions">Manage Server</span>                    | `/stars remove`             | Removes a channel as starboard.                                                                      |
| **stars emoji** \<choice> [emoji]<br><span class="user-permissions">Manage Server</span>   | `/stars emoji set 🔥`       | Sets or resets an emoji for starboard. This is a [Premium](https://carl.gg/get-premium) command.     |

<!-- tabs:end -->
