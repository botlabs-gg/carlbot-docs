## Setup
?> Anyone can use the `report` command, and by default Carl-bot will delete the command invocation when used. Instruct your users to use it in the channel where the event they're reporting happened, so your staff can make use of the jump link the report generates.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **reportchannel \<channel>** | `!reportchannel #reports` | Sets the channel where reports are sent.                   |
| report \<message> | `!report Carl-bot bad` | Sends a report to the report channel.                                    |
| **setnick \<user> \<name>** | `!setnick @Carl-bot God` | Changes the user's nickname in the server.                   |
| **lockdown setup**| `!lockdown setup` | Toggles off <span style="color: red;">Send Messages</span> from all roles execpt @everyone. This is a premium command. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **moderation reportchannel \<channel>** | `/moderation reportchannel #reports` | Sets the channel where reports are sent. |
| moderation report \<message> | `/moderation report Carl-bot bad` | Sends a report to the report channel               |
| **moderation setnick \<user> \<name>** | `/moderation setnick @Carl-bot God` | Changes the user's nickname in the server. |
| **lockdown setup**| `/lockdown setup` | Toggles off <span style="color: red;">Send Messages</span> from all roles except @everyone. This is a premium command. |

<!-- tabs:end -->


## Punishment Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **ban \<member> [days=2] [reason]** | `!ban @Carl-bot too good` | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged.                                                                               |
| **mute \<member> [duration] [reason]** | `!mute @Carl-bot 2h30m too good` | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config)                                                                                                        |
| **hardmute \<member> [duration] [reason]** | `!hardmute @Carl-bot 2h` | Similar to mute but also removes all of the roles of the user. |
| **unmute \<member> [reason]** | `!unmute @Carl-bot served` | Unmutes a member.                                        |
| **kick \<member> [reason]** | `!kick @Carl-bot bot` | Kicks a member.                                                 |
| **softban \<member> [days=2] [reason]** | `!softban @Carl-bot vacation` | Bans and immediately unbans a member to clear message history. |
| **tempban \<member> [days=2] [duration] [reason]** | `!tempban @Carl-bot 1h` | Bans a user for the specified duration.|
| **massban [days=2] <members...>** | `!massban @Carl-bot @John` | Bans multiple members.                               |
| **warn \<member> [reason]** | `!warn @Carl-bot` | Warns a member, DMs them a copy of the reason as well.              |
| **timeout \<member> [time] [reason]** | `!timeout @Carl-bot 10m` | Timeout a member, DMs them a copy of the reason as well. |
| **removetimeout \<member> [reason]** | `!removetimeout @Carl-bot served` | Removes timeout from a member.             |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **moderation ban \<member> [days] [reason]** | `/moderation ban @Carl-bot 2` | Bans the member from the server. This works even if the member isn't on the server. Days refer to the number of days old messages from them that should be purged.                                                                      |
| **moderation mute \<member> [duration] [reason]** | `/moderation mute @Carl-bot` | Mutes a member for the specified time. If no time is given, mutes are indefinite. This uses the Muterole set in [Config](config)                                                                                                     |
| **moderation hardmute \<member> [duration] [reason]** | `/moderation hardmute @Carl-bot` | Similar to mute but also removes all of the roles of the user. |
| **moderation unmute \<member> [reason]** | `/moderation unmute @Carl-bot` | Unmutes a member.                         |
| **moderation kick \<member> [reason]** | `/moderation kick @Carl-bot bot` | Kicks a member.                           |
| **moderation softban \<member> [days] [reason]** | `/moderation softban @Carl-bot vacation` | Bans and immediately unbans a member to clear message history. |
| **moderation tempban \<member> [delete_days] [duration] [reason]** | `/moderation tempban @Carl-bot 1h` | Bans a user for the specified duration. |
| **moderation massban \<members> [days]** | `/moderation massban @Carl-bot @John` | Bans multiple members.             |
| **moderation warn \<member> [reason]** | `/moderation warn @Carl-bot` | Warns a member, DMs them a copy of the reason as well. |
| **moderation timeout \<member> [duration] [reason]** | `/moderation timeout @Carl-bot` | Timeout a member, DMs them a copy of the reason as well. |
| **moderation removetimeout \<member> [reason]** | `/moderation removetimeout @Carl-bot` | Removes timeout from a member. |

<!-- tabs:end -->

?> Reason, if provided, shows up in the modlogs and Discord's audit logs. 

### Managing Warns

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **warns [member]**| `!warns @Carl-bot`| Lists all current warnings in the server or of the specified member.          |
| **removewarn \<case_id>** | `!removewarn 17` | Removes a warning by its case id.                                      |
| **clearwarn**     | `!clearwarn @Carl-bot` | Removes all warnings from a member.                                      |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **moderation warns [member]** | `/moderation warns @Carl-bot` | Lists all current warnings in the server or of the specified member. |
| **moderation removewarning \<case_id>** | `/moderation removewarning 17` | Removes a warning by its case id.          |
| **moderation clearwarnings** | `/moderation clearwarnings @Carl-bot` | Removes all warnings from a member.            |

<!-- tabs:end -->


## User Notes

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **setnote \<member> \<note>** | `!setnote @Carl-bot favorite bot` | Assigns the note to the member specified.         |
| **notes \<member>** | `!notes @Carl-bot` | Displays all of a member's notes.                                          |
| **removenote \<note_id>** | `!removenote 56` | Removes a note by number.                                              |
| **clearnotes \<member>** | `!clearnotes @Carl-bot` | Removes all notes from a member.                                 |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **notes setnote \<member> \<note>** | `/notes setnote @Carl-bot favorite bot` | Assigns the note to the member specified. |
| **notes view \<member>** | `/notes view @Carl-bot` | Displays all of a member's notes.                                |
| **notes removenote \<note_id>** | `/notes removenote 56` | Removes a note by number.                                  |
| **notes clearnotes \<member>** | `/notes clearnotes @Carl-bot` | Removes all notes from a member.                     |

<!-- tabs:end -->


## Lockdown
!> Locking down a channel denies the @everyone role <span style="color: red;">Send Messages</span> as an override in the specified channel. Any roles explicitly granting <span style="color: red;">Send Messages</span> will override this for anyone with that role. Set up your server correctly by removing <span style="color: red;">Send Messages</span> from all non-mod roles.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **lockdown [channel=current] [duration]** | `!lockdown #general 20m` | Locks the specified channel for the duration, if specified  else indefinitely. |
| **unlockdown \<channel>** | `!unlockdown #general` | Unlocks the specified channel.                                   |
| **lockdown server \<duration>** | `!lockdown server 20m` | Locks all the chanels in the server.                       |
| **unlockdown server** | `!unlockdown server` | Unlocks all the channels in the server.                                |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **lockdown channel [channel] [duration] [reason]** | `/lockdown channel #general 20m spam` | Locks the specified channel for the duration, if specified  else indefinitely. |
| **unlockdown channel [channel]** | `/unlockdown channel #general` | Unlocks the specified channel.                    |
| **lockdown server [duration] [reason]** | `/lockdown server 20m spam` | Locks all the chanels in the server.          |
| **unlockdown server** | `/unlockdown server` | Unlocks all the channels in the server.                                |

<!-- tabs:end -->


## Purging Messages
?> `purge` ignores pinned messages but `cleanup` does not.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **purge [search=100]** | `!purge 200` | Purges the number of messages specified.                                      |
| **purge bot [search=100] [prefix]** | `!purge bot 20 ?` | Purges bot messages and messages with the specified prefix. |
| **purge contains [search=100] \<substring>** | `!purge contains 12 thanos` | Purges messages containing the substring specified. |
| **purge [search=100] \<member>** | `!purge 20 @Carl-bot` | Purges messages from a specific member.                    |
| **purge all [search=100]** | `!purge all 13` | Purges the number of messages specified.                               |
| **purge embeds [search=100]** | `!purge embeds 12` | Purges messages with embeds.                                     |
| **purge emoji [search=100]** | `!purge emoji 6` | Purges messages that contain custom emoji.                          |
| **purge files [search=100]** | `!purge files 21` | Purges messages with attachments.                                  |
| **purge images [search=100]** | `!purge images 11` | Purges messages with attachments or embeds.                      |
| **purge links [search=100]** | `!purge links 15` | Purges messages containing links.                                  |
| **purge [mentions\|pings] [search=100]** | `!purge pings 25` | Purges messages containing pings.                      |
| **purge [human\|humans] [search=100]** | `!purge human 13` | Purges messages except those by bots.                    |
| **purge reactions [search=100]** | `!purge reactions` | Removes all reactions from messages.                          |
| **cleanup [search=100]** | `!cleanup 8` | Purges messages sent by @Carl-bot.                                          |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **purge bot \<search> [prefix]** | `/purge bot 20 ?` | Purges bot messages and messages with the specified prefix.    |
| **purge contains \<substring> [search]** | `/purge contains thanos 12` | Purges messages containing the substring specified. |
| **purge user \<member> [search]** | `/purge user @Carl-bot 20` | Purges messages from a specific member.              |
| **purge all \<count>** | `/purge all 13` | Purges the number of messages specified.                                   |
| **purge embeds \<count>** | `/purge embeds 12` | Purges messages with embeds.                                         |
| **purge emoji [count]** | `/purge emoji 6` | Purges messages that contain custom emoji.                               |
| **purge files \<count>** | `/purge files 21` | Purges messages with attachments.                                      |
| **purge images \<count>** | `/purge images 11` | Purges messages with attachments or embeds.                          |
| **purge links \<count>** | `/purge links 15` | Purges messages containing links.                                      |
| **purge mentions \<count>** | `/purge mentions 25` | Purges messages containing pings.                                |
| **purge human \<count>** | `/purge human 13` | Purges messages except those by bots.                                  |
| **purge reactions [count]** | `/purge reactions` | Removes all reactions from messages.                               |
| **moderation cleanup [count]** | `/moderation cleanup 8` | Purges messages sent by @Carl-bot.                         |

<!-- tabs:end -->