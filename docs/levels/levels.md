# Levels



!!! info 
    Levels is a premium feature offered to patrons as a way to show my gratitude for helping keep the bot alive

[![become a patron](https://c5.patreon.com/external/logo/become_a_patron_button.png)](https://www.patreon.com/bePatron?u=11251319)


!!! warning
    In order for the bot to start tracking messages you need to change *any* setting. As long as `!lvl config` works then the bot is counting.

### Level commands

| Name | Example | Usage |
| :--- | :--- | :--- |
| **lvl \[member\]** | -- | Displays the rank card for the member. |
| **lvl config** | -- | Shows the current configuration.  |
| **lvl background &lt;link&gt;** | !lvl bg https://i.imgur.com/s1ck3n1ng.png | Changes the background image for !lvl. |
| **lvl blacklist &lt;entities...&gt;** | !lvl bl #bot-abuse "bot abuser" | Blacklists one or more roles or channels. Messages sent in these channels will be ignored for xp and if a member has one or more of the blacklisted roles they gain no xp anywhere. |
| **lvl unblacklist &lt;entities...&gt;** | -- | Undoes what !lvl bl does. |
| **lvl unblacklist &lt;entities...&gt;** | -- | Undoes what !lvl bl does. |
| **lvl color &lt;color&gt;** | !lvl color eeaaee | Sets the accent color for your rank card. |
| **lvl mee6import** | -- | Since the bot uses the same xp curve as mee6 you can import your existing mee6 config. Please note that this replaces your current xp. |
| **lvl rate \[rate\] \[time frame\]** | !lvl rate 5 60 | Changes how often you can gain experience. The example would allow a maximum of 5 xp drops per 60 seconds. |

### Level notifications

| Name | Example | Usage |
| :--- | :--- | :--- |
| **lvl shh** | -- | Makes the bot no longer announce level up messages.  |
| **lvl destination &lt;channel&gt;** | !lvl bg https://i.imgur.com/s1ck3n1ng.png | Changes the background image for !lvl. |
| **lvl blacklist &lt;entities...&gt;** | !lvl bl #bot-abuse "bot abuser" | Blacklists one or more roles or channels. Messages sent in these channels will be ignored for xp and if a member has one or more of the blacklisted roles they gain no xp anywhere. |
| **lvl unblacklist &lt;entities...&gt;** | -- | Undoes what !lvl bl does. |
| **lvl limit &lt;n&gt;** | !lvl limit 15 | Only announce level ups ABOVE this level (15 means 16 and above would be announced.) |
| **lvl mod &lt;n&gt;** | !lvl mod 5 | Sets the bot to only announce level up messages if they are evenly divisible by the number. For instance you could set it to 10 to announce lvl 10, 20, 30 etc... |
| **lvl rewardonly** | -- | Only announce levels with associated rank rewards |

### Level rewards
| Name | Example | Usage |
| :--- | :--- | :--- |
| **lvl replace** | -- | Toggles between rewards being additive or replacing earlier rewards. |
| **lvl reward &lt;lvl&gt; \[role\]** | !lvl reward 10 active member | Adds a reward for the specified level. Use the command without specifying a role to remove the reward at that level.  |