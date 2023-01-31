## Prefix
?> Carl-bot's default prefixes are `@Carl-bot`, `/`, `!` & `?`.

!> If you use `!prefix clear` then you would be left with no prefix and you will either have to mention the bot to set a new one or use `/` slash commands. Better choice would be `!prefix set` in most of the cases.

<!-- tabs:start -->

<!-- tab:Chat Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| prefix        | `!prefix`         | Lists the prefixes currently in use by the server                             |
| **prefix add \<prefix\>** | `!prefix add -` | Adds a prefix to be used byb the bot (Limited to 10).<br>**NOTE**: If you want a two word prefix or a prefix with a space after it or an emoji, you must use quotes. |
| **prefix set \<prefix\>** | `!prefix set -` | Sets the specified prefix to be the only prefix in the server.          |
| **prefix remove \<prefix\>** | `!prefix remove -` | Removes a prefix. Can't remove mentioning the bot or `/` slash commands. |
| **prefix clear** | `!prefix clear` | Removes all prefixes except mentioning the bot or `/` slash commands. This *obviously* means that you need to mention the bot to register more prefixes. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| prefix list        | `/prefix list`         | Lists the prefixes currently in use by the server                   |
| **prefix add \<prefix\>** | `/prefix add -` | Adds a prefix to be used byb the bot (Limited to 10).<br>**NOTE**: If you want a two word prefix or a prefix with a space after it or an emoji, you must use quotes. |
| **prefix set \<prefix\>** | `/prefix set -` | Sets the specified prefix to be the only prefix in the server.          |
| **prefix remove \<prefix\>** | `/prefix remove -` | Removes a prefix. Can't remove mentioning the bot or `/` slash commands. |
| **prefix clear** | `/prefix clear` | Removes all prefixes except mentioning the bot or `/` slash commands. This *obviously* means that you need to mention the bot to register more prefixes. |

<!-- tabs:end -->


## Managing Commands
?> Consider using the **[Dashboard](https://carl.gg)**. It is much, much easier to manage commands through the Dashboard as it allows per-command customization *far* beyond what these commands offer.

!> Restricted commands require a bot channel to be set up.

<!-- tabs:start -->

<!-- tab:Chat Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **ignore [channels...] [commands...]** | `!ignore #general #log ping about` | If no channel is specified, the current channel is ignored. If no command is specified, all commands will be ignored in that channel. <span style="color: red;">Manage Server</span> bypasses this.                                          |
| **ignore server** | `!ignore server`  | This will make the bot mod-only.                                              |
| **ignore all [commands...]** | `!ignore all ping about` | This will ignore the specified command(s) in all current channels of the server that the bot can see. |
| **unignore [channels...] [commands...]** | `!unignore #general #log ping about` | Reverses what `!ignore` does        |
| **unignore all** | `!unignore all` | Unignores all channels. This won't take ignored commands into account.           |
| **disable <commands...>** | `!disable ping about` | This disables the command in the entire server and no permission can bypass this. |
| **disable mod**   | `!disable mod`    | Disables all moderation commands.                                             |
| **disable all**   | `!disable all`    | Disables all the commands.                                                    |
| **enable <commands...>** | `!enable ping about` | This enables a previously disabled command.                         |
| **enable mod**    | `!enable mod`     | Enables all moderation commands.                                              |
| **enable all**    | `!enable all`     | Enables all the commands.                                                     |
| **enable list**   | `!enable list`    | Shows all enabled and disabled commands.                                      |
| **restrict <command>** | `!restrict ping` | Restricts the response of the command to the specified bot channel.       |
| **unrestrict <command>** | `!unrestrict ping` | Unrestricts the response of the command.                              |
| **modonly <command>** | `!modonly ping` | Makes the command usable only by the role set in `modrole`.                 |
| **unmodonly <command>** | `!unmodonly ping` | Removes a command from the modonly list.                                |


<!-- tab:Slash Commands -->
?> Slash commands can be managed according to your needs in your server's settings:<br>
**Server Settings** > **Integrations** > **Carl-bot** > **Manage**

<!-- tabs:end -->


## Setting Channels

<!-- tabs:start -->

<!-- tab:Chat Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **set welcome [channel]**   | `!set welcome #welcome` | Sets the channel to send the welcome, farewell and ban messages. If no channel is specified, this will remove the welcome channel. |
| **set twitch [channel]** | `!set twitch #welcome` | Sets the channel to send twitch notifications to. If no channel is specified, this will remove the twitch channel. |

<!-- tab:Slash Commands -->
?> Slash commands can be managed according to your needs in your server's settings:<br>
**Server Settings** > **Integrations** > **Carl-bot** > **Manage**

<!-- tabs:end -->


## Setting Roles

<!-- tabs:start -->

<!-- tab:Chat Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **modrole <role>**   | `!modrole mod` | Any user with the specified role will be seen as a Moderator by the bot. This command won't give the users power to kick, ban, mute, warn, etc. |
| **modrole clear** | `!modrole clear`  | Removes the modrole.                                                          |
| **muterole create [role_name=Muted]** | `!muterole create prison` | Creates a role with the specified name or default name **Muted**, and changes permission for that role in all current channels |
| **muterole <role>** | `!muterole prison` | Sets an already created role as the muterole.                                |
| **muterole update** | `!muterole update` | Updates the muterole settings for the server.                              |

<!-- tab:Slash Commands -->
?> Slash commands can be managed according to your needs in your server's settings:<br>
**Server Settings** > **Integrations** > **Carl-bot** > **Manage**

| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **muterole create [name]** | `/muterole create @prison` | Creates a role with the specified name or default name **Muted**, and changes permission for that role in all current channels |
| **muterole set <role>** | `/muterole set @prison` | Sets an already created role as the muterole.                                |
| **muterole update** | `/muterole update` | Updates the muterole settings for the server.                              |

<!-- tabs:end -->