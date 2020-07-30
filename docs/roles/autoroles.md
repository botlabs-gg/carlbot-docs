# Autoroles & Delayed Autoroles

!!! info
	If you have autoroles and reassigned roles, the returning member will receive the union of both.

### Automatic Roles

???+ tldr "Automatic Roles"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **[autorole\|autoroles]** | !autoroles | Shows which roles will be added upon joining and if the bot will readd roles when someone leaves and rejoins the server |
	| **autorole [readd\|reassign]** | !autorole readd | Turns reassigning roles on/off |
	| **autorole add &lt;role&gt;** | !autorole add peon | Autoroles are roles that are given to the user upon joining the server. |
	| **autorole remove &lt;role&gt;** | !autorole remove admin | Removes a role from being auto assigned |
	| **autorole [bl\|blacklist] &lt;roles...&gt;** | !autorole bl admin newbie | Prevents the mentioned roles from being reassigned |
	| **autorole unblacklist &lt;roles...&gt;** | !autorole unblacklist "fortnite expert" admin | Undoes what !autorole bl does |

### Delayed Autoroles

???+ tldr "Delayed Autoroles"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **[tr\|timedrole]** | !timedrole | Shows the roles being assigned with their delay |
	| **timedrole [add\|+] &lt;time&gt; &lt;role&gt;** | !timedrole add 42h19m22s fortnite expert | Adds a role to be added with a delay |
	| **timedrole remove &lt;role&gt;** | !tr remove newbie | Removes the role from being automatically assigned and also cancels any pending roles (Note: all pending delayed roles with the same delay as the removed role will be removed, sorry!) |

