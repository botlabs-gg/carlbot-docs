?> It is highly recommended to use the **[Dashboard](https://carl.gg)** for setting up automod.

![Automod](_images/automod.png ':size=75%')

## General Settings

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[am\|automod]** | `!am`             | Shows an overview of the current automod settings.                            |
| **automod drama \<channel>** | `!automod drama #drama` | This is a [Premium](https://www.patreon.com/carlbot) command.<br>Set the channel where mods can make decisions on rule breakers through reactions. |
| **automod log \<channel>** | `!automod log #automod` | Set the channel where the logs for automatic moderation actions go. |
| **automod [media\|mo] <channels...>** | `!am mo #show-off` | Set the channel(s) where only posting images/links is allowed. |
| **automod [unmedia\|umo\|unmo] <channels...>** | `!am umo #show-off` | Removes the media-only restriction from one or more channels. |
| **automod [whitelist\|wl] <roles/channels>** | `!am wl mods #admin-chat` | Whitelists roles and/or channels so that the automod ignores messages posted in/by them. |
| **automod [unwhitelist\|unwl] <roles/channels>** | `!automod unwl mods #admin-chat` | Removes roles and/or channels from the automod whitelist. |
| **deletefiles**   | `!deletefiles`    | Toggles deleting unsafe files. Safe formats include png, jpg, jpeg, gif, svg, bmp, tif, webp, webm, mp4, mov, pdf, txt, mp3, flac and wav. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **automod server**| `/automod server` | Shows an overview of the current automod settings.                            |
| **automod drama \<channel>** | `/automod drama #drama` | This is a [Premium](https://www.patreon.com/carlbot) command.<br>Set the channel where mods can make decisions on rule breakers through reactions. |
| **automod log \<channel>** | `/automod log #automod` | Set the channel where the logs for automatic moderation actions go. |
| **automod media <channels...>** | `/automod mo #show-off` | Set the channel(s) where only posting images/links is allowed. |
| **automod unmedia <channels...>** | `/automod umo #show-off` | Removes the media-only restriction from one or more channels. |
| **automod whitelist [add\|remove] <roles/channels>** | `!automod whitelist add mods #admin-chat` | Add or remove roles and/or channels from the automod whitelist. |
| **deletefiles**   | `/deletefiles`    | Toggles deleting unsafe files. Safe formats include png, jpg, jpeg, gif, svg, bmp, tif, webp, webm, mp4, mov, pdf, txt, mp3, flac and wav. |

<!-- tabs:end -->


### Punishments
The punishments available are:
- **delete** - Deletes the message.
- **warn** - Warns the offender.
- **tempmute <duration>** - Temporarily mutes for the duration specified.
- **mute** - Mute for indefinite duration.
- **timeout** - Timeout the offender.
- **kick** - Kicks the offender.
- **tempban <duration>** - Temporarily bans the offender for the duration specified.
- **ban** - Bans the offender.
- **defer** - Sends the context to the drama channel and lets the mods vote on it.
- **message** - Sends a message to the channel warning the member.
- **dm/pm** - Sends a private message to the offender.

?> Input the duration in this format `3h42m`. 

?>You can add more than one punishment by separating them with commas.


## Warn Threshold
Warns do not automatically expire. Managing warns is detailed on the [Moderation](moderation) page. The warn threshold determines how Carl-bot reacts when a user receives a new warning and their total number of warnings exceeds a limit. Unless a user's warnings are reset or reduced manually, this punishment will trigger each time a user receives new warning while their total number of warnings is above your server's set limit. Set it to 0 to turn it off.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **automod [warn\|threshold] \<limit>** | `!am warn 5`             | Sets the warn threshold for a punishment to be made. |
| **automod [warnpunish\|wp] <punishments...>** | `!am wp kick` | Sets the punishment for hitting the threshold.        |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **automod threshold \<limit>** | `/automod threshold 5`             | Sets the warn threshold for a punishment to be made. |
| **automod warnpunish <punishments...>** | `/automod warnpunish kick` | Sets the punishment for hitting the threshold. |

<!-- tabs:end -->


## Spam Settings

<!-- tabs:start -->

<!-- tab:Message -->
Message spam will not be active without setting a rate limit of at least 1+ messages in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[slowmode\|sm] [rate] [per]** | `!slowmode 5 25` | Rate is the number of messages you can send per timeframe. Per is the timeframe. If you only supply one value, it sets that value as the per. (1/x) |
| **slowmode [punishment\|punish\|p] <punishments...>** | `!sm p delete, tempmute 20m` | Sets the punishment(s) for hitting the rate limit. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **slowmode set \<rate>** | `/slowmode set 5 25` | Sets slowmode in the current channel. If you want the rate to be X messages in Y time then input `x y`. If only one value is supplied then it sets it as 1 message every supplied value. |
| **slowmode disable** | `/slowmode disable` | Disables slowmode in the current channel.                                |
| **slowmode punishment <punishments...>** | `/slowmode punishment delete, tempmute 20m` | Sets the punishment(s) for hitting the rate limit. |

<!-- tabs:end -->

<!-- tab:Attachments -->
Attachmentspam will not be active without setting a rate limit of at least 1+ files in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **attachmentspam [rate] [per=1]** | `!attachmentspam 3 5` | Rate limits the number of attachments a member can post in a specific timeframe. |
| **attachmentspam punishment <punishments...>** | `!attachmentspam p mute, defer` | Sets the punishment(s) for hitting the rate limit. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **attachmentspam set \<rate>** | `/attachmentspam set 3 5` | Rate limits the number of attachments a member can post in a specific timeframe. |
| **attachmentspam disable** | `/attachmentspam disable` | Disables attachmentspam in the current channel.              |
| **attachmentspam punishment <punishments...>** | `/attachmentspam punishment mute, defer` | Sets the punishment(s) for hitting the rate limit. |

<!-- tabs:end -->

<!-- tab:Mentions -->
Mentionspam will not be active without setting a rate limit of at least 1+ mentions in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **mentionspam [rate] [per=1]** | `!mentionspam 25 5` | Enables the bot to automatically punish the mentionspammers.   |
| **mentionspam punishment <punishments...=mute>** | `!mentionspam p tempban 24h` | Sets the punishment(s) for hitting the rate limit. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **mentionspam set \<rate>** | `/mentionspam set 25 5` | Enables the bot to automatically punish the mentionspammers.   |
| **mentionspam disable** | `/mentionspam disable` | Disables mentionspam in the current channel.                       |
| **mentionspam punishment <punishments...=mute>** | `/mentionspam punishment tempban 24h` | Sets the punishment(s) for hitting the rate limit. |

<!-- tabs:end -->

<!-- tab:Links -->
Linkspam will not be active without setting a rate limit of at least 1+ links in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **linkspam**      | `!linkspam`       | Shows the current settings.                                                   |
| **linkspam \<rate> [per=1]** | `!linkspam 1 1` | Sets the link rate limit. Use the example command to block all links. |
| **linkspam punishment <punishments...>** | `!linkspam p delte, mute, defer` | Sets the punishment(s) for hitting the rate limit. |
| **linkspam bl <links...>** | `!linkspam bl reddit.com twitter.com` | Blacklists one or more links.                   |
| **linkspam wl <links...>** | `!linkspam wl reddit.com twitter.com` | Whitelists one or more links.                   |
| **linkspam unbl <links...>** | `!linkspam unbl reddit.com twitter.com` | Removes one or more links from the blacklist. |
| **linkspam unwl <links...>** | `!linkspam unwl reddit.com twitter.com` | Removes one or more links from the whitelist. |
| **linkspam clearbl** | `!linkspam clearbl` | Clears the blacklist.                                                    |
| **linkspam clearwl** | `!linkspam clearwl` | Clears the whitelist.                                                    |
| **linkspam block**| `!linkspam block` | Punish all non-whitelisted links.                                             |
| **linkspam off**  | `!linkspam off`   | Punish only blacklisted links.                                                |
| **linkspam norole** | `!linkspam norole` | Punish only those without roles.                                           |



<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **linkspam server** | `/linkspam server` | Shows the linkspam settings.                                               |
| **linkspam rate \<rate>** | `/linkspam rate 1 1` | Sets the link rate limit. Use the example command to block all links. |
| **linkspam punishment <punishments...>** | `/linkspam punishment delte, mute, defer` | Sets the punishment(s) for hitting the rate limit. |
| **linkspam blacklist [add\|remove] <links...>** | `/linkspam blacklist add reddit.com twitter.com` | Adds or removes link(s) to/from the linkspam blacklist. |
| **linkspam whitelist [add\|remove] <links...>** | `/linkspam whitelist remove reddit.com twitter.com` | Adds or removes link(s) to/from the linkspam whitelist. |
| **linkspam clear [blacklist\|whitelist]** | `/linkspam clear blacklist` | Clears the blacklist or the whitelist.      |
| **linkspam block**| `/linkspam block` | Punish all non-whitelisted links.                                             |
| **linkspam off**  | `/linkspam off`   | Punish only blacklisted links.                                                |
| **linkspam norole** | `/linkspam norole` | Punish only those without roles.                                           |

<!-- tabs:end -->

<!-- tab:Invites -->
Invitespam will not be active without setting a rate limit of at least 1+ invites in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **invitespam**    | `!invitespam`     | Shows the invitespam settings.                                                |
| **invitespam \<rate> [per=1]** | `!invitespam 1 1` | Sets the invite rate limit. Use the example command to block all invites. |
| **invitespam punishment <punishments...>** | `!invitespam p delte, mute, defer, message` | Sets the punishment(s) for hitting the rate limit. |
| **invitespam bl <links...>** | `!invitespam bl discord.gg/fredboat` | Adds the server that the invite goes to, to the blacklist. |
| **invitespam wl <links...>** | `!invitespam wl discord.gg/fredboat` | Adds the server that the invite goes to, to the whitelist. |
| **invitespam unbl <links...>** | `!invitespam unbl discord.gg/fredboat` | Removes one or more servers from the blacklist. |
| **invitespam unwl <links...>** | `!invitespam unwl discord.gg/fredboat` | Removes one or more servers from the whitelist. |
| **invitespam clearbl** | `!invitespam clearbl` | Clears the blacklist.                                                    |
| **invitespam clearwl** | `!invitespam clearwl` | Clears the whitelist.                                                    |
| **invitespam [on\|block]**| `!invitespam on` | Punish all non-whitelisted invites.                                    |
| **invitespam off**| `!invitespam off` | Punish only blacklisted invites.                                              |
| **invitespam norole** | `!invitespam norole` | Punish only those without roles.                                       |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **invitespam server** | `/invitespam server` | Shows the invitespam settings.                                         |
| **invitespam punishment <punishments...>** | `/invitespam punishment delte, mute, defer, message` | Sets the punishment(s) for hitting the rate limit. |
| **invitespam norole** | `/invitespam norole` | Punish only those without roles.                                       |

<!-- tabs:end -->

<!-- tab:Bad Words -->
Bad words detection is case insensitive, looks for substrings and ignores punctuation. Censoring `boat` would cause Carl-bot to punish any user that said `fredboat`.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **censor <words...>** | `!censor boat`| Adds one or more words to the list of blacklisted words.                     |
| **censor add <words...>** | `!censor add boat` | Same as above.                                                       |
| **censor remove <words...>** | `!censor remove boat` | Removes a word from the blacklist.                             |
| **censor list**   | `!censor list`    | Lists all censored words.                                                     |
| **censor clear**  | `!censor clear`   | Clears all censored words.                                                    |
| **censor punishment <punishments...=delete, defer>** | `!censor p mute, delete, defer` |  Sets the punishment(s) for bad words. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **censor server** | `/censor server`  | View censor settings for server.                                              |
| **censor words [add\|remove] <words...>** | `/censor words add boat`| Adds or removes one or more words to/from the list of blacklisted words. |
| **censor display**| `/censor display` | Lists all censored words.                                                     |
| **censor clear**  | `/censor clear`   | Clears all censored words.                                                    |
| **censor punishment <punishments...=delete, defer>** | `/censor punishment mute, delete, defer` |  Sets the punishment(s) for bad words. |

<!-- tabs:end -->

<!-- tab:Caps Limit -->

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **capslimit \<percentage>** | `!capslimit 70` | Punishes messages with the % of its characters being uppercase. The message has to be at least 6 characters long. |
| **[capspunish\|capsp\|capspunishment] <punishments...>** | `!capsp delete, warn` | Sets the punishment(s) for sending a message which hits the threshold. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **caps limit \<percentage>** | `/caps limit 70` | Punishes messages with the % of its characters being uppercase. The message has to be at least 6 characters long. |
| **caps punishment <punishments...>** | `/caps punishment delete, warn` | Sets the punishment(s) for sending a message which hits the threshold. |

<!-- tabs:end -->

<!-- tabs:end -->