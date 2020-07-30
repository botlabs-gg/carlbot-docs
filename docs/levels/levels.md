# Levels

!!! info 
    Levels is a premium feature offered to patrons as a way to show my gratitude for helping keep the bot alive.

[![become a patron](https://c5.patreon.com/external/logo/become_a_patron_button.png)](https://www.patreon.com/bePatron?u=11251319)

!!! warning
    In order for the bot to start tracking messages you need to change *any* setting. As long as `!lvl config` works then the bot is counting.

### Level Card Configuration

???+ tldr "Level Card Commands"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| [levels\|lvl\|level\|lvls] [member] | !level @Kintark#0588 | Displays the rank card for the member. |
	| lvl [background\|bg] &lt;link&gt; | !lvl bg https://i.imgur.com/s1ck3n1ng.png | Sets the background\* of your level card. Provide a link or upload an image directly. |
	| lvl [color\|colour] &lt;color&gt; | !lvl color 93ffdd | Sets the fill color of the XP bar and the border surrounding your profile picture on your rank card.|
	| lvl accent &lt;color&gt; | !lvl accent ffffff | Sets the color for text, the horizontal bar, and the border surrounding the XP bar on your rank card. |
	| lvl [opacity\|alpha] &lt;value&gt; | !lvl opacity 0 | Sets the amount of opacity present in the transparent overlay.<br>0 = fully transparent<br>1.0 or 100 = fully opaque |
	| **lvl [serverbackground\|serverbg] &lt;link&gt;** | !lvl serverbg https://i.imgur.com/s1ck3n1ng.png | Sets the default background\* of your server's level cards. This will not overwrite any background individually set. |

	\**Ideal background resolution is 934x282 pixels but if a different resolution is supplied it will be scaled to the ideal width and cropped to fit the height.*

	Example Level Card:
	![Example Level Card](../images/levelcard.png)

### Level Settings

???+ tldr "Level Settings"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **lvl config** | !lvl config | Shows the current configuration.  |
	| **lvl [blacklist\|bl] &lt;entities...&gt;** | !lvl bl #bot-abuse "bot abuser" | Blacklists one or more roles or channels. Messages sent in these channels will be ignored for xp and if a member has one or more of the blacklisted roles they gain no xp anywhere. |
	| **lvl [unblacklist\|unbl] &lt;entities...&gt;** | !lvl unbl #bot-abuse "bot abuser" | Undoes what !lvl bl does. |
	| **lvl mee6import** | !lvl mee6import | Since the bot uses the same xp curve as mee6 you can import your existing mee6 config. Please note that this replaces your current xp. |
	| **lvl rate [rate] [time frame]** | !lvl rate 5 60 | Changes how often you can gain experience. The example would allow a maximum of 5 xp drops per 60 seconds. |
	| **lvl reset &lt;member&gt;** | !lvl reset @Carl#0001 | Resets an individual user's level and XP to 0. Cannot be undone. |
	| **lvl resetall** | !lvl resetall | Resets your entire server's levels and XP to 0, but also creates a backup that you can restore. |
	| **lvl restore** | !lvl restore | Restores your entire server's levels and XP from the last backup made. |


### Level Notifications

???+ tldr "Level Notifications"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **lvl shh** | !lvl shh | Makes the bot no longer announce level up messages.  |
	| **lvl destination &lt;channel&gt;** | !lvl bg https://i.imgur.com/s1ck3n1ng.png | Changes the background image for !lvl. |
	| **lvl limit &lt;number&gt;** | !lvl limit 15 | Only announce level ups ABOVE this level (15 means 16 and above would be announced.) |
	| **lvl mod &lt;number&gt;** | !lvl mod 5 | Sets the bot to only announce level up messages if they are evenly divisible by the number. For instance you could set it to 10 to announce lvl 10, 20, 30 etc... |
	| **lvl rewardonly** | !lvl rewardonly | Only announce levels with associated rank rewards |
	| lvl log | !lvl log | Shows the last 25 level-up events in the server. |

### Level Rewards

???+ tldr "Level Rewards"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **lvl replace** | !lvl replace | Toggles between rewards being additive or replacing earlier rewards. |
	| **lvl reward &lt;lvl&gt; [role]** | !lvl reward 10 active member | Adds a reward for the specified level. Use the command without specifying a role to remove the reward at that level.  |