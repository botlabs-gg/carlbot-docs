# Autoroles and delayed autoroles



#### Automatic Roles

| Name | Example | Usage |
| :--- | :--- | :--- |
| **autorole** | -- | Shows which roles will be added upon joining and if the bot will readd roles when someone leaves and rejoins the server |
| **autoroles \[readd\|reassign\]** | -- | Turns reassigning roles on/off |
| **autorole add &lt;role&gt;** | !autorole add peon | Autoroles are roles that are given to the user upon joining the server. |
| **autorole remove &lt;role&gt;** | !autorole remove admin | -//- |
| **autorole \[bl\|blacklist\] &lt;roles...&gt;** | !autorole bl admin newbie | Prevents the mentioned roles from being reassigned |
| **autorole unblacklist &lt;roles...&gt;** | !autorole unblacklist "fortnite expert" admin | Undoes what !autorole bl does |

If you have autoroles and reassigned roles, the member will receive the union of both.

#### Delayed autoroles

| Name | Example | Usage |
| :--- | :--- | :--- |
| **\[tr\|timedrole\]** | -- | Shows the roles being assigned with their delay |
| **timedrole \[add\|+\] &lt;time&gt; &lt;role&gt;** | !timedrole add 42h19m22s fortnite expert | Adds a role to be added with a delay |
| **timedrole remove &lt;role&gt;** | !tr remove newbie | Removes the role from being automatically assigned and also cancels any pending roles \(Note: all pending delayed roles with the same delay as the removed role will be removed, sorry!\) |

