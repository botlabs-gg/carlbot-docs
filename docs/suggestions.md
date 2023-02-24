?> All commands here require `suggestion channel` to have been used and set in order to work.

## Settings

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **[suggestion\|suggestions]** | `!suggestion` | Displays the server's current suggestion config.                      |
| **suggestion channel [channel=suggestions]** | `!suggestion channel` | Sets a channel as the suggestions channel or creates a new one named `suggestions`. |
| **suggestion dm** | `!suggestion dm`  | Toggles between sending the person who suggested something upon a moderator deciding on it. |
| **suggestion limit \<number>** | `!suggestion limit 5` | The amount of votes difference required to change the embed color to red/green. |
| **suggestion move [channel=suggestion-log]** | `!suggestion move` | Set a secondary channel to announce approved/denied suggestions. |
| **suggestion edit** | `!suggestion edit` | Toggles if orginal suggestion should be edited to show the decision made.  |
| **suggestion submit [channel]** | `!suggestion submit #submissions` | Sets a single channel where members are allowed to make suggestions. |
| **suggestion anon** | `!suggestion anon` | Toggles member's name and avatar to show/not show in their suggestions. This is not retroactive. |
| **suggestion who \<suggestion_id>** | `!suggestion who 6` | Shows who suggested a suggestion.                         |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **suggestion server** | `/suggestion server` | Displays the server's current suggestion config.                       |
| **suggestion channel [channel=suggestions]** | `/suggestion channel` | Sets a channel as the suggestions channel or creates a new one named `suggestions`. |
| **suggestion dm** | `/suggestion dm`  | Toggles between sending the person who suggested something upon a moderator deciding on it. |
| **suggestion limit \<limit>** | `/suggestion limit 5` | The amount of votes difference required to change the embed color to red/green. |
| **suggestion move [channel=suggestion-log]** | `/suggestion move` | Set a secondary channel to announce approved/denied suggestions. |
| **suggestion edit** | `/suggestion edit` | Toggles if orginal suggestion should be edited to show the decision made.  |
| **suggestion submit [channel]** | `/suggestion submit #submissions` | Sets a single channel where members are allowed to make suggestions. |
| **suggestion anonymous** | `/suggestion anonymous` | Toggles member's name and avatar to show/not show in their suggestions. This is not retroactive. |
| **suggestion who \<suggestion_id>** | `/suggestion who 6` | Shows who suggested a suggestion.                         |

<!-- tabs:end -->


## Making Suggestions

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Anyone can use the `suggest` command to make suggestions.

| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| suggest \<message>| `!suggest make vc`| Creates a suggestion.                                                         |

<!-- tab:Slash Commands -->
Anyone can use the `suggestion suggest` command to make suggestions.

| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| suggestion suggest \<content>| `/suggestion suggest make vc`| Creates a suggestion.                                   |

<!-- tabs:end -->


## Suggestion Decisions

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **aprove \<suggestion_id> [reaason]** | `!approve 3` | Approves a suggestion.                                         |
| **deny \<suggestion_id> [reason]** | `!deny 4 spam` | Denies a suggestion.                                            |
| **consider \<suggestion_id> [reason]** | `!consider 5` | Marks a suggestion as being considered.                      |
| **implemented \<suggestion_id> [reason]** | `!implemented 1 Added` | Marks a suggestion as implemented.               |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **suggestion aprove \<suggestionid> [reaason]** | `/suggestion approve 3` | Approves a suggestion.                    |
| **suggestion deny \<suggestionid> [reason]** | `/suggestion deny 4 spam` | Denies a suggestion.                       |
| **suggestion consider \<suggestionid> [reason]** | `/suggestion consider 5` | Marks a suggestion as being considered. |
| **suggestion implemented \<suggestionid> [reason]** | `/suggestion implemented 1 Added` | Marks a suggestion as implemented. |

<!-- tabs:end -->