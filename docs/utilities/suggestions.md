# Suggestions

!!! info
    All commands require `!suggestion channel [#channel]` to have been used in order to work, please start with that.

### Suggestion Settings

???+ tldr "Suggestion Settings"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **suggestion channel [#channel=suggestions]** | !suggestion channel #cool-server-feedback | Sets a channel as the suggestion channel or creates a new one named "suggestions" if you don't mention one. |
	| **[suggestion\|suggestions]** | !suggestion | Displays the server's current suggestion config. |
	| **suggestion dm** | !suggestion dm | Toggles between sending the person who suggested something upon a moderator deciding on it. |
	| **suggestion limit &lt;number&gt;** | !suggestion limit 5 | The color of the approved/denied suggestions are based on the difference in upvotes and downvotes on the original post. This threshold is the amount of votes required for the decision to be fully green/red. |
	| **suggestion move [#channel=suggestion-log]** | !suggestion move #ideas-i-love | This will let you set a secondary channel to announce the suggestions that admins have approved/denied. Just like !suggestion channel this can be left blank to create a channel named "sugguestion-log". |
	| **suggestion edit** | !suggestion edit | When a decision is made regarding a suggestion, edit the original suggestion to display the decision instead of reposting it in the channel. If a move channel has been specified, it's posted there and edited in the original channel. |
	| **suggestion submit [#channel]** | !suggestion submit #botcommands | Lets you set a single channel where people are allowed to make suggestions. This can be useful if you don't want everyone to be able to make suggestions |
	| **suggestion anon** | !suggestion anon | Toggles member's name and avatar not appearing when making a suggestion. (Not retroactive) |
	| **suggestion who &lt;suggestion_number&gt;** | !suggestion who 6 | Shows who suggested something (useful for anonymous servers) |

### Making Suggestions

???+ tldr "Making Suggestions"
	Any user can use the `suggest` command to make a suggestion.

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| suggest &lt;message&gt; | !suggest The bot should be able to announce new youtube videos | Creates a suggestion |

### Suggestion Decisions

???+ tldr "Suggestion Decisions"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **approve &lt;suggestion_number&gt; [reason=No reason given]** | !approve 5 Great idea man, will add it for sure | Approves of a suggestion. If reason is left blank the reason will be "No reason given"|
	| **deny &lt;suggestion_number&gt; [reason=No reason given]** | !deny 6 This is literally impossible due to how discord works | Denies a suggestion. |
	| **consider &lt;suggestion_number&gt; [reason=No reason given]** | !consider 4 I'm not sure if this would really add that much, but if the people want it... | Marks a suggestion as being considered. |
	| **implemented &lt;suggestion_number&gt; [reason=No reason given]** | !implemented 5 the command is !youtubesub | Marks a suggestion as implemented. |

