?> After you make a Starboard channel, your members can react to any message with a ⭐ `:star:` which counts as a vote to display that message as a post on the Starboard. Once the message gets enough reactions, Carl-bot posts it onto the Starboard. By default, a user's reaction on their own post doesn't count.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **starboard [channel=starboard]** | `!starboard #stars` | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`. |
| **star limit \<number>** | `!star limit 3` | Sets the amount of reactions required for a post to get posted on the Starboard. |
| **star nsfw**     | `!star nsfw`      | Toggles stars in NSFW channels.                                               |
| **star self**     | `!star self`      | Toggles being able to star your own posts.                                    |
| **star [stats\|top] [member]** | `!star stats @Carl-bot` | Shows some information about the server's or specified member's starred posts and giving pattern. |
| **star show \<message_id>** | `!star show 123456` | Shows a starred post from the Starboard in the channel the command was used in. |
| **star [jump\|source]** | `!star jump`| Sends the direct link to the starred message.                                 |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **stars setup [channel=starboard]** | `/stars setup #stars` | Sets up the Starboard for the server. Defaults to creating new channel named `#starboard`. |
| **stars limit \<limit>** | `/stars limit 3` | Sets the amount of reactions required for a post to get posted on the Starboard. |
| **stars nsfw**    | `/stars nsfw`     | Toggles embedding images from starred messages in NSFW channels.              |
| **stars self**    | `/stars self`     | Toggles being able to star your own posts.                                    |
| **stars server**  | `/stars server`   | Displays stats about the server's starboard.                                  |
| **stars stats [member]** | `/stars stats @Carl-bot` | Shows some information about the server's or specified member's starred posts and giving pattern. |
| **stars show \<message_id>** | `/stars show 123456` | Shows a starred post from the Starboard in the channel the command was used in. |
| **stars jump**    | `/stars jump`     | Sends the direct link to the starred message.                                 |
| **stars autostar**| `/stars autostar` | This is a [Premium](https://www.patreon.com/carlbot) command. Automatically stars new Starboard entries. |
| **stars blacklist \<channels>** | `/stars blacklist #staff` | Blocks channels from having their messages starred.     |
| **stars unblacklist \<channels>** | `/stars unblacklist #staff` | Unblocks channels from having their messages starred. |
| **stars config**  | `/stars config`   | View Starboard configuration for server.                                      |
| **stars lock**    | `/stars lock`     | Locks the Starboard making it completely uninteractive.                       |
| **stars random**  | `/stars random`   | Shows a random starred message.                                               |

<!-- tabs:end -->