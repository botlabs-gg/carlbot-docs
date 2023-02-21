?> Levels is a premium feature offered to our Patrons as a way to show our gratitude for helping keep the bot alive.

[![Patron Button](_images/patron_button.png)](https://www.patreon.com/bePatron?u=11251319)

## Level Card

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
!> In order for the bot to start tracking messages you need to change <i>any</i> setting. As long as `!lvl config` works, the level system works.

| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[levels\|lvl\|level\|lvls] [member]** | `!level @Carl-bot` | Displays the rank card for a member.                   |
| **level [background\|bg] \<link>** | `!lvl bg https://i.imgur.com/L1n\|<` | Sets the [background](#background) of your level card.    |
| **level [color\|colour] \<color>** | `!lvl color FF0000` | Sets the fill color of the XP bar and the border surrounding your profile picture. |
| **level accent \<color>** | `!lvl accent FFFFFF` | Sets the color for text, the horizontal bar, and the border surrounding the XP bar. |
| **level [opacity\|alpha] \<value>** | `!lvl alpha 0` | Sets the opacity of the overlay.<br>0 - Transparent<br>1.0 or 100 - Opaque |
| **level [serverbackground\|serverbg] \<link>** | `!lvl serverbg https://i.ibb.co/L1n\|<` | Sets the default [background](#background) for level cards in your server. This won't overwrite individually set backgrounds. |

<!-- tab:Slash Commands -->
!> In order for the bot to start tracking messages you need to change <i>any</i> setting. As long as `/level config` works, the level system works.

| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level member [member]** | `/level member @Carl-bot` | Displays the rank card for a member.                          |
| **level background [link] [attachment]** | `/level background image.png` | Sets the [background](#background) of your level card.    |
| **level color \<color>** | `/level color FF0000` | Sets the fill color of the XP bar and the border surrounding your profile picture. |
| **level accent \<color>** | `/level accent FFFFFF` | Sets the color for text, the horizontal bar, and the border surrounding the XP bar. |
| **level opacity \<opacity>** | `/level opacity 0` | Sets the opacity of the overlay.<br>0 - Transparent<br>1.0 or 100 - Opaque |
| **level serverbackground [link] [attachment]** | `/level serverbackground image.png` | Sets the default [background](#background) for level cards in your server. This won't overwrite individually set backgrounds. |

<!-- tabs:end -->

### Background
Ideal background resolution is `934x282` pixels but if a different resolution is supplied it will be scaled to the ideal width and cropped to fit the height.

> **Example Level Card:**
![Example Level Card](_images/level_card.png)


## Level Settings

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level config**  | `!lvl config`     | Shows the current configuration.                                              |
| **level [blacklist\|bl] <entities...>** | `!lvl bl #welcome Muted` | Blacklists one or more roles and/or channels from gaining xp. |
| **level [unblacklist\|unbl] <entities...>** | `!lvl unbl #welcome Muted` | Removes one or more roles and/or channels from the blacklist. |
| **level mee6import** | `!lvl mee6import` | Import exisitng Mee6 config. Carl-bot uses the same XP curve as Mee6. This will replace your current XP. |
| **level rate [rate] [time]** | `!lvl rate 5 60` | Changes how often you can gain XP.                                  |
| **level reset \<member>** | `!lvl reset @Carl-bot` | Resets the level and XP of the member. This can't be undone.     |
| **level resetall**| `!lvl resetall`   | Resets the level and XP of the entire server but also creates a backup that you can restore. |
| **level restore** | `!lvl restore`    | Restores the level and XP of the entire server from the last backup made.     |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level config**  | `/level config`   | Shows the current configuration.                                              |
| **level blacklist \<add\|remove> \<channels_or_roles>** | `/level blacklist add #welcome Muted` | Adds or removes roles and/or channels to/from the blacklist. |
| **level mee6import** | `/level mee6import` | Import exisitng Mee6 config. Carl-bot uses the same XP curve as Mee6. This will replace your current XP. |
| **level rate [rate]** | `/level rate 5 60` | Changes how often you can gain XP.                                       |
| **level reset \<user_id>** | `/level reset @Carl-bot` | Resets the level and XP of the member. This can't be undone.  |
| **level resetall**| `/level resetall` | Resets the level and XP of the entire server but also creates a backup that you can restore. |
| **level restore** | `/level restore`  | Restores the level and XP of the entire server from the last backup made.     |

<!-- tabs:end -->


## Level Notifications

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level shh**     | `!lvl shh`        | Bot stops announcing level up messages.                                       |
| **level dm**      | `!lvl dm`         | Makes the bot DM the level up message to the user.                            |
| **level channel [channel=current]** | `!lvl channel #level-up` | Sets a channel to send level up messages to.         |
| **level limit \<number>** | `!lvl limit 15` | Only announce level ups above the limit.                                |
| **level mod \<number>** | `!lvl mod 5`| Only announce level ups if they are evenly divisble by the number.            |
| **level rewardonly** | `!lvl rewardonly` | Only announce level ups with associated rank rewards.                      |
| **leaderboard [page]** | `!leaderboard` | Lists the members based on their XP.                                        |
| **level log**     | `!lvl log`        | Shows the last 25 level ups in the server.                                    |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level shh**     | `/level shh`      | Bot stops announcing level up messages.                                       |
| **level dm**      | `/level dm`       | Makes the bot DM the level up message to the user.                            |
| **level channel [channel=current]** | `/level channel #level-up` | Sets a channel to send level up messages to.       |
| **level limit \<limit>** | `/level limit 15` | Only announce level ups above the limit.                               |
| **level mod \<mod>** | `/level mod 5` | Only announce level ups if they are evenly divisble by the number.            |
| **level rewardonly** | `/level rewardonly` | Only announce level ups with associated rank rewards.                    |
| **leaderboard [page]** | `/leaderboard` | Lists the members based on their XP.                                        |
| **level log**     | `/level log`      | Shows the last 25 level ups in the server.                                    |

<!-- tabs:end -->


## Level Rewards

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level replace** | `!lvl replace`    | Toggles between rewards being additive or replacing earlier rewards.          |
| **level reward \<lvl> [role]** | `!lvl reward 10 Member` | Adds a reward for the specified level. Use without specifying a role to remove the reward at that level. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **level replace** | `/level replace`  | Toggles between rewards being additive or replacing earlier rewards.          |
| **level reward \<level> [role]** | `/level reward 10 Member` | Adds a reward for the specified level. Use without specifying a role to remove the reward at that level. |

<!-- tabs:end -->