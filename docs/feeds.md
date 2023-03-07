Feeds are a way for you to make announcements and ping a specific role without having to deal with the annoyances and potential abuse from having a mentionable role or manually toggling a role inbetween mentionable and not. You need <span style="color: red;">Manage Server</span> permission to use the feed commands.

A feed is an association between a role and a channel. When you use the feed announce command, the role will be set to mentionable very briefly, the role will be pinged and your message will be sent in the channel with which the feed is associated, and the role will subsequently be set back to unmentionable.

## Feed Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[feed\|feeds]** | `!feeds`          | Lists all the feeds that have been set up in the server.                      |
| **feeds create \<name> \<role>** | `!feeds create got game of thrones` | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned. |
| **feeds announce \<name> \<content>** | `!feeds announce got Hey guys, everyone dies` | Makes an announcement to the specified feed. |
| **feeds [delete/del/remove] \<name>** | `!feeds del got` | Deletes a feed.                                            |
| **feeds clear**   | `!feeds clear`    | Delets all feeds from the server.                                             |
| **feeds move \<name> \<channel>** | `!feeds move got #tv-shows` | Moves a feed to a specified channel.                |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **feeds list**    | `/feeds list`     | Lists all the feeds that have been set up in the server.                      |
| **feeds create \<name> \<role>** | `/feeds create got @game of thrones` | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned. |
| **feeds announce \<name> \<content>** | `/feeds announce got Hey guys, everyone dies` | Makes an announcement to the specified feed. |
| **feeds delete \<name>** | `/feeds delete got` | Deletes a feed.                                                      |
| **feeds clear**   | `/feeds clear`    | Delets all feeds from the server.                                             |
| **feeds move \<name> \<channel>** | `/feeds move got #tv-shows` | Moves a feed to a specified channel.                |

<!-- tabs:end -->


## Autofeeds

Automatic feeds can be seen as group reminders, and they share a lot of functionality with reminders.

?> Timezones suck, use the [Dashboard](https://carl.gg) to create autofeeds with your local timezone.

![Autofeeds](_images/create_autofeed.png ':size=75%')

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[autofeed\|autofeeds\|af]** | `!af` | Lists all autofeeds that have been set up in the server.                      |
| **autofeeds \<role> \<time> \<message>** | `!af "Final Fantasy" 18h The servers have been reset.` | Autofeeds that will ping the role specified each time they run. |
| **autofeeds silent \<time> \<message>** | `!af silent 2h Vote for Carl-bot on Top.gg` | Autofeeds that won't ping any role each time they run. |
| **autofeeds silence \<id>** | `!af silence 37` | Silences an already existing autofeed.                               |
| **autofeeds repeat \<id> \<time>** | `!af repeat 13 24h` | Marks an autofeed to be repeated. This keeps going until you delete the autofeed. |
| **autofeeds remove \<id>** | `!af remove 77` | Removes an autofeed.                                                   |
| **autofeeds clear** | `!af clear`     | Removes all autofeeds.                                                        |
| **autofeeds move \<id> \<channel>** | `!af move 73 #general` | Moves an autofeed to the specified channel.            |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **autofeeds list**| `/autofeeds list` | Lists all autofeeds that have been set up in the server.                      |
| **autofeeds create \<role> \<when>** | `/autofeeds create @FF 18h The servers have been reset.` | Autofeeds that will ping the role specified each time they run. |\
| **autofeeds everyone \<duration>** | `/autofeeds everyone 24h Good morning` | Creates an autofeed that pings @everyone. |
| **autofeeds here \<duration>** | `/autofeeds here 24h Good morning` | Creates an autofeed that pings @here.           |
| **autofeeds silent \<duration>** | `/autofeeds silent 2h Vote for Carl-bot on Top.gg` | Autofeeds that won't ping any role each time they run. |
| **autofeeds silence \<id>** | `/autofeeds silence 37` | Silences an already existing autofeed.                        |
| **autofeeds repeat \<id> \<when>** | `/autofeeds repeat 13 24h` | Marks an autofeed to be repeated. This keeps going until you delete the autofeed. |
| **autofeeds delete \<id>** | `/autofeeds delete 77` | Removes an autofeed.                                            |
| **autofeeds clear** | `/autofeeds clear` | Removes all autofeeds.                                                     |
| **autofeeds move \<id> \<channel>** | `/autofeeds move 73 #general` | Moves an autofeed to the specified channel.     |

<!-- tabs:end -->