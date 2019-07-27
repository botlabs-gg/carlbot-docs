# Role management
!!! info
    These commands are for administrators to manage role assignments in their servers. The bot might mention it or you requiring additional permission despite having `manage roles`. To fix this, make sure both you and the bot have roles higher in the role hierarchy than the role you're trying to assign.
    
[This page does not go over reaction roles, click this text to go there instead](https://docs.carl.gg/roles/reaction-roles)

| Name | Example | Usage |
| :--- | :--- | :--- |
| **!role &lt;member&gt; &lt;role&gt;** | !role @Carl\#0001 fortnite pro | Adds/removes a role from the specified member |
| **!role add &lt;member&gt; &lt;role&gt;** | !role add @Carl\#0001 idiot | Adds a role to the specified member |
| **!role remove &lt;member&gt; &lt;role&gt;** | !role remove @Carl\#0001 idiot | Removes a role from the specified member |
| **!role color &lt;role&gt; &lt;color&gt;** | !role color weeb \#eeaaee | Changes the color of a role |
| **!role \[removeall\|purge\|clear\] &lt;@member&gt;** | !role removeall @dumbguy\#1337 | Removes all roles from a member. |
| **!temprole &lt;@member&gt; &lt;time&gt; &lt;role&gt;** | !temprole @coolguy\#0001 24h birthday boy | Adds a role for some time and removes it after the time is up. Time can be either before or after the role name. |
| **!addrank &lt;roles...&gt;** | !addrank fortnite weeb "f1 fanatic" "koishi fanboy" "tomato lover" | Adds one or more roles so that **any** member can assign it to themselves. |
| **!removerank &lt;roles...&gt;** | !removerank fortnite "f1 fanatic" | Removes a rank so that it can no longer be self assigned. |
| !rank &lt;role&gt; | !rank fortnite | Adds/removes the role to the person who used the command. |
| !ranks | -- | Lists all whitelisted ranks. |
| **role create &lt;name&gt; \[color\] \[mentionable=False\] \[hoist=False\]** | !role create "cool dude" eeaaee true true | Creates a role. Hoist decides if it shows up in the sidebar or not. |
| **!allroles** | -- | Displays list of roles in the server and member count assigned to the role. |
| !role info &lt;role&gt; | !role info fortnite | Displays the role's Name, Member Count, Color, and when it was created. |
| !role custom &lt;member&gt; &lt;custom\_string&gt; | !role custom @MichaelAus\#9999 +Role 1 -Role 2 | Gives the ability to add and remove roles within a single command, useful for removing a pending role whilst granting a member/joined role. |
| !rank custom &lt;custom\_string&gt; | !rank custom +Role 1 -Role 2 | Adds/removes multiple roles to the person using the command. Requires roles to be whitelisted. |

# Bulk management

!!! warning
    Only one bulk assignment can be used at a time

| Name | Example | Usage |
| :--- | :--- | :--- |
| **!role all &lt;role&gt;** | !role all peon | Adds a role to every single member. |
| **!role bots &lt;role&gt;** | !role bots metallic overlord | Adds a role to every single bot. |
| **!role humans &lt;role&gt;** | !role humans flesh haver | Adds a role to all non-bots |
| **!role in &lt;base\_role&gt; &lt;assigned\_role&gt;** | !role in "movie fan" game of thrones | Adds a role \(&lt;assigned\_role&gt;\) to all members with the &lt;base\_role&gt; role. In the previous example, all members with the movie fan role would be assigned the game of thrones role. |
| **!role rall &lt;role&gt;** | !role rall admin | Removes a role from all members. |
| **!role rbots &lt;role&gt;** | !role rbots people | Removes a role from all bots. |
| **!role rhumans &lt;role&gt;** | !role rhumans metallic | Removes a role from all humans. |
| **!role rin &lt;role&gt;** | !role rin weeb cool dude | Removes a role from all members with the base\_role. Previous example would have removed the "cool dude" role from all weebs. |
