?> After you make a Starboard channel, your members can react to any message with a ⭐ `:star:` which counts as a vote to display that message as a post on the Starboard. Once the message gets enough reactions, Carl-bot posts it onto the Starboard. By default, a user's reaction on their own post doesn't count.

![Starboard Settings](_images/starboard_settings.png ":size=75%")

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                           | Example                         | Usage                                                                                                |
| ---------------------------------------------------------------------------------------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **starboard setup** [channel=starboard]<br><span class="user-permissions">Manage Server</span> | `/starboard setup #stars`       | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`.           |
| **starboard limit** \<limit><br><span class="user-permissions">Manage Server</span>            | `/starboard limit 3`            | Sets the amount of reactions required for a post to get posted on the Starboard.                     |
| **starboard nsfw**<br><span class="user-permissions">Manage Server</span>                      | `/starboard nsfw`               | Toggles embedding images from starred messages in NSFW channels.                                     |
| **starboard self**<br><span class="user-permissions">Manage Server</span>                      | `/starboard self`               | Toggles being able to star your own posts.                                                           |
| **starboard server**                                                                           | `/starboard server`             | Displays stats about the server's starboard.                                                         |
| **starboard stats** [member]                                                                   | `/starboard stats @user`        | Shows some information about the server's or specified member's starred posts and giving pattern.    |
| **starboard show** \<message_id>                                                               | `/starboard show 123456`        | Shows a starred post from the Starboard in the channel the command was used in.                      |
| **starboard jump**<br><span class="user-permissions">Manage Server</span>                      | `/starboard jump`               | Sends the direct link to the starred message.                                                        |
| **starboard autostar**<br><span class="user-permissions">Manage Server</span>                  | `/starboard autostar`           | This is a [Premium](https://carl.gg/get-premium) command. Automatically stars new Starboard entries. |
| **starboard blacklist** \<channels><br><span class="user-permissions">Manage Server</span>     | `/starboard blacklist #staff`   | Blocks channels from having their messages starred.                                                  |
| **starboard unblacklist** \<channels><br><span class="user-permissions">Manage Server</span>   | `/starboard unblacklist #staff` | Unblocks channels from having their messages starred.                                                |
| **starboard config**<br><span class="user-permissions">Manage Server</span>                    | `/starboard config`             | View Starboard configuration for server.                                                             |
| **starboard lock**<br><span class="user-permissions">Manage Server</span>                      | `/starboard lock`               | Locks the Starboard making it completely uninteractive.                                              |
| **starboard random**                                                                           | `/starboard random`             | Shows a random starred message.                                                                      |
| **starboard remove**<br><span class="user-permissions">Manage Server</span>                    | `/starboard remove`             | Removes a channel as starboard.                                                                      |
| **starboard emoji** \<choice> [emoji]<br><span class="user-permissions">Manage Server</span>   | `/starboard emoji set 🔥`       | Sets or resets an emoji for starboard. This is a [Premium](https://carl.gg/get-premium) command.     |

<!-- tab:Mention Commands -->

| Name                                                                                     | Example                             | Usage                                                                                                |
| ---------------------------------------------------------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **starboard** [channel=starboard]<br><span class="user-permissions">Manage Server</span> | `@Carl-bot starboard #stars`        | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`.           |
| **star limit** \<number><br><span class="user-permissions">Manage Server</span>          | `@Carl-bot star limit 3`            | Sets the amount of reactions required for a post to get posted on the Starboard.                     |
| **star nsfw**<br><span class="user-permissions">Manage Server</span>                     | `@Carl-bot star nsfw`               | Toggles stars in NSFW channels.                                                                      |
| **star self**<br><span class="user-permissions">Manage Server</span>                     | `@Carl-bot star self`               | Toggles being able to star your own posts.                                                           |
| **star** [server\|stats\|top] [member]                                                   | `@Carl-bot star stats @user`        | Shows some information about the server's or specified member's starred posts and giving pattern.    |
| **star show** \<message_id>                                                              | `@Carl-bot star show 123456`        | Shows a starred post from the Starboard in the channel the command was used in.                      |
| **star** [jump\|source]<br><span class="user-permissions">Manage Server</span>           | `@Carl-bot star jump`               | Sends the direct link to the starred message.                                                        |
| **star autostar**<br><span class="user-permissions">Manage Server</span>                 | `@Carl-bot star autostar`           | This is a [Premium](https://carl.gg/get-premium) command. Automatically stars new Starboard entries. |
| **star blacklist** \<channels><br><span class="user-permissions">Manage Server</span>    | `@Carl-bot star blacklist #staff`   | Blocks channels from having their messages starred.                                                  |
| **star unblacklist** \<channels><br><span class="user-permissions">Manage Server</span>  | `@Carl-bot star unblacklist #staff` | Unblocks channels from having their messages starred.                                                |
| **star config**<br><span class="user-permissions">Manage Server</span>                   | `@Carl-bot star config`             | View Starboard configuration for server.                                                             |
| **star lock**<br><span class="user-permissions">Manage Server</span>                     | `@Carl-bot star lock`               | Locks the Starboard making it completely uninteractive.                                              |
| **star random**                                                                          | `@Carl-bot star random`             | Shows a random starred message.                                                                      |
| **star remove**<br><span class="user-permissions">Manage Server</span>                   | `@Carl-bot star remove`             | Removes a channel as starboard.                                                                      |
| **star emoji** [emoji]<br><span class="user-permissions">Manage Server</span>            | `@Carl-bot star emoji 🔥`           | Sets or resets an emoji for starboard. This is a [Premium](https://carl.gg/get-premium) command.     |

<!-- tabs:end -->
