## Setup

?> Anyone can use the `/report` command, and by default Carl-bot will delete the command invocation when used. Instruct your users to use it in the channel where the event they're reporting happened, so your staff can make use of the jump link the report generates.

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                  | Example                   | Usage                                                                                                                                                 |
| ------------------------------------------------------------------------------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **reportchannel** \<channel><br><span class="user-permissions">Manage Server</span>   | `/reportchannel #reports` | Sets the channel where reports are sent.                                                                                                              |
| **report** \<message>                                                                 | `/report Carl-bot bad`    | Sends a report to the report channel                                                                                                                  |
| **setnick** \<user> \<name><br><span class="user-permissions">Manage Nicknames</span> | `/setnick @user God`      | Changes the user's nickname in the server.                                                                                                            |
| **lockdown setup**<br><span class="user-permissions">Manage Roles</span>              | `/lockdown setup`         | Toggles off <span style="color: red;">Send Messages</span> from all roles except @everyone. This is a [Premium](https://carl.gg/get-premium) command. |

<!-- tab:Mention Commands -->

| Name                                                                                  | Example                            | Usage                                                                                                                                                 |
| ------------------------------------------------------------------------------------- | ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **reportchannel** \<channel><br><span class="user-permissions">Manage Server</span>   | `@Carl-bot reportchannel #reports` | Sets the channel where reports are sent.                                                                                                              |
| **report** \<message>                                                                 | `@Carl-bot report Carl-bot bad`    | Sends a report to the report channel.                                                                                                                 |
| **setnick** \<user> \<name><br><span class="user-permissions">Manage Nicknames</span> | `@Carl-bot setnick @user God`      | Changes the user's nickname in the server.                                                                                                            |
| **lockdown setup**<br><span class="user-permissions">Manage Roles</span>              | `@Carl-bot lockdown setup`         | Toggles off <span style="color: red;">Send Messages</span> from all roles execpt @everyone. This is a [Premium](https://carl.gg/get-premium) command. |

<!-- tabs:end -->

## Punishment Commands

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                                         | Example                   | Usage                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------ | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ban** \<member> [days] [reason]<br><span class="user-permissions">Ban Members</span>                       | `/ban @user 2`            | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged. |
| **mute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span>                 | `/mute @user`             | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config).                                  |
| **hardmute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span>             | `/hardmute @user`         | Similar to mute but also removes all of the roles of the user.                                                                                                     |
| **unmute** \<member> [reason]<br><span class="user-permissions">Manage Roles</span>                          | `/unmute @user`           | Unmutes a member.                                                                                                                                                  |
| **kick** \<member> [reason]<br><span class="user-permissions">Kick Members</span>                            | `/kick @user bot`         | Kicks a member.                                                                                                                                                    |
| **softban** \<member> [days] [reason]<br><span class="user-permissions">Ban Members</span>                   | `/softban @user vacation` | Bans and immediately unbans a member to clear message history.                                                                                                     |
| **tempban** \<member> [delete_days] [duration] [reason]<br><span class="user-permissions">Ban Members</span> | `/tempban @user 1h`       | Bans a user for the specified duration.                                                                                                                            |
| **warn** \<member> [reason]<br><span class="user-permissions">Manage Roles</span>                            | `/warn @user`             | Warns a member, DMs them a copy of the reason as well.                                                                                                             |
| **timeout** \<member> [duration] [reason]<br><span class="user-permissions">Timeout Members</span>           | `/timeout @user`          | Timeout a member, DMs them a copy of the reason as well.                                                                                                           |
| **untimeout** \<member> [reason]<br><span class="user-permissions">Timeout Members</span>                    | `/untimeout @user`        | Removes timeout from a member.                                                                                                                                     |

<!-- tab:Mention Commands -->

| Name                                                                                                    | Example                                | Usage                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ban** \<member> [days=2] [reason]<br><span class="user-permissions">Ban Members</span>                | `@Carl-bot ban @user too good`         | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged. |
| **mute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span>            | `@Carl-bot mute @user 2h30m too good`  | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config)                                   |
| **hardmute** \<member> [duration] [reason]<br><span class="user-permissions">Manage Roles</span>        | `@Carl-bot hardmute @user 2h`          | Similar to mute but also removes all of the roles of the user.                                                                                                     |
| **unmute** \<member> [reason]<br><span class="user-permissions">Manage Roles</span>                     | `@Carl-bot unmute @user served`        | Unmutes a member.                                                                                                                                                  |
| **kick** \<member> [reason]<br><span class="user-permissions">Kick Members</span>                       | `@Carl-bot kick @user bot`             | Kicks a member.                                                                                                                                                    |
| **softban** \<member> [days=2] [reason]<br><span class="user-permissions">Ban Members</span>            | `@Carl-bot softban @user vacation`     | Bans and immediately unbans a member to clear message history.                                                                                                     |
| **tempban** \<member> [days=2] [duration] [reason]<br><span class="user-permissions">Ban Members</span> | `@Carl-bot tempban @user 1h`           | Bans a user for the specified duration.                                                                                                                            |
| **massban** [days=2] <members...><br><span class="user-permissions">Ban Members</span>                  | `@Carl-bot massban @user @John`        | Bans multiple members. There is a cooldown of 2x command usage per hour.                                                                                           |
| **warn** \<member> [reason]<br><span class="user-permissions">Manage Roles</span>                       | `@Carl-bot warn @user`                 | Warns a member, DMs them a copy of the reason as well.                                                                                                             |
| **timeout** \<member> [time] [reason]<br><span class="user-permissions">Timeout Members</span>          | `@Carl-bot timeout @user 10m`          | Timeout a member, DMs them a copy of the reason as well.                                                                                                           |
| **removetimeout** \<member> [reason]<br><span class="user-permissions">Timeout Members</span>           | `@Carl-bot removetimeout @user served` | Removes timeout from a member.                                                                                                                                     |

<!-- tabs:end -->

?> Reason, if provided, shows up in the modlogs and Discord's audit logs.

### Managing Warns

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                               | Example                | Usage                                                                |
| ---------------------------------------------------------------------------------- | ---------------------- | -------------------------------------------------------------------- |
| **warns** [member]<br><span class="user-permissions">Manage Roles</span>           | `/warns @user`         | Lists all current warnings in the server or of the specified member. |
| **removewarning** \<case_id><br><span class="user-permissions">Manage Roles</span> | `/removewarning 17`    | Removes a warning by its case id.                                    |
| **clearwarnings**<br><span class="user-permissions">Manage Roles</span>            | `/clearwarnings @user` | Removes all warnings from a member.                                  |

<!-- tab:Mention Commands -->

| Name                                                                            | Example                     | Usage                                                                |
| ------------------------------------------------------------------------------- | --------------------------- | -------------------------------------------------------------------- |
| **warns** [member]<br><span class="user-permissions">Manage Roles</span>        | `@Carl-bot warns @user`     | Lists all current warnings in the server or of the specified member. |
| **removewarn** \<case_id><br><span class="user-permissions">Manage Roles</span> | `@Carl-bot removewarn 17`   | Removes a warning by its case id.                                    |
| **clearwarn**<br><span class="user-permissions">Manage Roles</span>             | `@Carl-bot clearwarn @user` | Removes all warnings from a member.                                  |

<!-- tabs:end -->

## User Notes

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                       | Example                             | Usage                                     |
| ------------------------------------------------------------------------------------------ | ----------------------------------- | ----------------------------------------- |
| **notes setnote** \<member> \<note><br><span class="user-permissions">Manage Server</span> | `/notes setnote @user favorite bot` | Assigns the note to the member specified. |
| **notes view** \<member><br><span class="user-permissions">Manage Server</span>            | `/notes view @user`                 | Displays all of a member's notes.         |
| **notes removenote** \<note_id><br><span class="user-permissions">Manage Server</span>     | `/notes removenote 56`              | Removes a note by number.                 |
| **notes clearnotes** \<member><br><span class="user-permissions">Manage Server</span>      | `/notes clearnotes @user`           | Removes all notes from a member.          |

<!-- tab:Mention Commands -->

| Name                                                                                 | Example                                | Usage                                     |
| ------------------------------------------------------------------------------------ | -------------------------------------- | ----------------------------------------- |
| **setnote** \<member> \<note><br><span class="user-permissions">Manage Server</span> | `@Carl-bot setnote @user favorite bot` | Assigns the note to the member specified. |
| **notes** \<member><br><span class="user-permissions">Manage Server</span>           | `@Carl-bot notes @user`                | Displays all of a member's notes.         |
| **removenote** \<note_id><br><span class="user-permissions">Manage Server</span>     | `@Carl-bot removenote 56`              | Removes a note by number.                 |
| **clearnotes** \<member><br><span class="user-permissions">Manage Server</span>      | `@Carl-bot clearnotes @user`           | Removes all notes from a member.          |

<!-- tabs:end -->

## Lockdown

!> Locking down a channel denies the @everyone role <span style="color: red;">Send Messages</span> as an override in the specified channel. Any roles explicitly granting <span style="color: red;">Send Messages</span> will override this for anyone with that role. Set up your server correctly by removing <span style="color: red;">Send Messages</span> from all non-mod roles.

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                             | Example                               | Usage                                                                         |
| ------------------------------------------------------------------------------------------------ | ------------------------------------- | ----------------------------------------------------------------------------- |
| **lockdown channel** [channel] [duration] [reason]                                               | `/lockdown channel #general 20m spam` | Locks the specified channel for the duration, if specified else indefinitely. |
| **unlockdown channel** [channel]<br><span class="user-permissions">Manage Channels</span>        | `/unlockdown channel #general`        | Unlocks the specified channel.                                                |
| **lockdown server** [duration] [reason]<br><span class="user-permissions">Manage Channels</span> | `/lockdown server 20m spam`           | Locks all the chanels in the server.                                          |
| **unlockdown server**<br><span class="user-permissions">Manage Channels</span>                   | `/unlockdown server`                  | Unlocks all the channels in the server.                                       |

<!-- tab:Mention Commands -->

| Name                                                                                               | Example                           | Usage                                                                         |
| -------------------------------------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------------------------------------- |
| **lockdown** [channel=current] [duration]<br><span class="user-permissions">Manage Channels</span> | `@Carl-bot lockdown #general 20m` | Locks the specified channel for the duration, if specified else indefinitely. |
| **unlockdown** \<channel><br><span class="user-permissions">Manage Channels</span>                 | `@Carl-bot unlockdown #general`   | Unlocks the specified channel.                                                |
| **lockdown server** \<duration><br><span class="user-permissions">Manage Channels</span>           | `@Carl-bot lockdown server 20m`   | Locks all the chanels in the server.                                          |
| **unlockdown server**<br><span class="user-permissions">Manage Channels</span>                     | `@Carl-bot unlockdown server`     | Unlocks all the channels in the server.                                       |

<!-- tabs:end -->

## Purging Messages

?> `/purge` ignores pinned messages but `/cleanup` does not.

<!-- tabs:start -->

<!-- tab:Slash Commands -->

| Name                                                                                            | Example                     | Usage                                                       |
| ----------------------------------------------------------------------------------------------- | --------------------------- | ----------------------------------------------------------- |
| **purge bot** \<search> [prefix]<br><span class="user-permissions">Manage Server</span>         | `/purge bot 20 ?`           | Purges bot messages and messages with the specified prefix. |
| **purge contains** \<substring> [search]<br><span class="user-permissions">Manage Server</span> | `/purge contains thanos 12` | Purges messages containing the substring specified.         |
| **purge user** \<member> [search]<br><span class="user-permissions">Manage Server</span>        | `/purge user @user 20`      | Purges messages from a specific member.                     |
| **purge all** \<count><br><span class="user-permissions">Manage Server</span>                   | `/purge all 13`             | Purges the number of messages specified.                    |
| **purge embeds** \<count><br><span class="user-permissions">Manage Server</span>                | `/purge embeds 12`          | Purges messages with embeds.                                |
| **purge emoji** [count]<br><span class="user-permissions">Manage Server</span>                  | `/purge emoji 6`            | Purges messages that contain custom emoji.                  |
| **purge files** \<count><br><span class="user-permissions">Manage Server</span>                 | `/purge files 21`           | Purges messages with attachments.                           |
| **purge images** \<count><br><span class="user-permissions">Manage Server</span>                | `/purge images 11`          | Purges messages with attachments or embeds.                 |
| **purge links** \<count><br><span class="user-permissions">Manage Server</span>                 | `/purge links 15`           | Purges messages containing links.                           |
| **purge mentions** \<count><br><span class="user-permissions">Manage Server</span>              | `/purge mentions 25`        | Purges messages containing pings.                           |
| **purge human** \<count><br><span class="user-permissions">Manage Server</span>                 | `/purge human 13`           | Purges messages except those by bots.                       |
| **purge reactions** [count]<br><span class="user-permissions">Manage Server</span>              | `/purge reactions`          | Removes all reactions from messages.                        |
| **cleanup** [count]<br><span class="user-permissions">Manage Server</span>                      | `/cleanup 8`                | Purges messages sent by @user.                              |

<!-- tab:Mention Commands -->

| Name                                                                                                | Example                              | Usage                                                                                                          |
| --------------------------------------------------------------------------------------------------- | ------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| **purge** [search=100] [member]<br><span class="user-permissions">Manage Server</span>              | `@Carl-bot purge 200`                | Purges the number of messages specified. If a member is specified then only that member's messages are purged. |
| **purge bot** [search=100] [prefix]<br><span class="user-permissions">Manage Server</span>          | `@Carl-bot purge bot 20 ?`           | Purges bot messages and messages with the specified prefix.                                                    |
| **purge contains** [search=100] \<substring><br><span class="user-permissions">Manage Server</span> | `@Carl-bot purge contains 12 thanos` | Purges messages containing the substring specified.                                                            |
| **purge all** [search=100]<br><span class="user-permissions">Manage Server</span>                   | `@Carl-bot purge all 13`             | Purges the number of messages specified.                                                                       |
| **purge embeds** [search=100]<br><span class="user-permissions">Manage Server</span>                | `@Carl-bot purge embeds 12`          | Purges messages with embeds.                                                                                   |
| **purge emoji** [search=100]<br><span class="user-permissions">Manage Server</span>                 | `@Carl-bot purge emoji 6`            | Purges messages that contain custom emoji.                                                                     |
| **purge files** [search=100]<br><span class="user-permissions">Manage Server</span>                 | `@Carl-bot purge files 21`           | Purges messages with attachments.                                                                              |
| **purge images** [search=100]<br><span class="user-permissions">Manage Server</span>                | `@Carl-bot purge images 11`          | Purges messages with attachments or embeds.                                                                    |
| **purge links** [search=100]<br><span class="user-permissions">Manage Server</span>                 | `@Carl-bot purge links 15`           | Purges messages containing links.                                                                              |
| **purge** [mentions\|pings] [search=100]<br><span class="user-permissions">Manage Server</span>     | `@Carl-bot purge pings 25`           | Purges messages containing pings.                                                                              |
| **purge** [human\|humans] [search=100]<br><span class="user-permissions">Manage Server</span>       | `@Carl-bot purge human 13`           | Purges messages except those by bots.                                                                          |
| **purge reactions** [search=100]<br><span class="user-permissions">Manage Server</span>             | `@Carl-bot purge reactions`          | Removes all reactions from messages.                                                                           |
| **cleanup** [search=100]<br><span class="user-permissions">Manage Server</span>                     | `@Carl-bot cleanup 8`                | Purges messages sent by @user.                                                                                 |

<!-- tabs:end -->
