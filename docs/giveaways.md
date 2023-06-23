## Giveaway Commands
?> This feature is currently in open beta so expect frequent changes and updates.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **giveaway \<duration> \<winners> \<prize> [channel=current]** | `!giveaway 1h10m 2 Nitro #giveaways` | Creates a giveaway for the specified duration, number of winners, prize and optional channel which defaults to the channel that the command is used in. |
| **giveaway reroll \<case_id>** | `!giveaway reroll 23` | Rerolls the giveaway with the specified case id.             |
| **giveaway end \<case_id>** | `!giveaway end 42` | Ends an ongoing giveaway prematurely. You will be asked if you want to announce winners or not. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **giveaway create \<duration> \<winners> \<prize> [channel=current]** | `/giveaway create 10m 1 Nitro` | Creates a giveaway for the specified duration, number of winners, prize and optional channel which defaults to the channel that the command is used in. |
| **giveaway reroll \<giveaway_id>** | `/giveaway reroll 23` | Rerolls the giveaway with the specified giveaway id.     |
| **giveaway end \<giveaway_id>** | `/giveaway end 42` | Ends an ongoing giveaway prematurely. You will be asked if you want to announce winners or not. |

<!-- tabs:end -->