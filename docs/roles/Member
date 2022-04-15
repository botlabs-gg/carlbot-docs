# Reaction Roles

!!! tip
    Deleted messages are also cleared from the database. Pin the reaction role message to make it immune to purging.

### RR Management

!!! info
	`reactrole`, `reactionrole`, and `rr` are all aliases for the same base command.

???+ tldr "RR Management"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **rr [make\|setup]** | !rr make | Starts the interactive setup to get you started with reaction roles |
	| **rr [list\|show] [msg\_id]** | !rr show | Shows the emoji-role pairs and their associated message id, useful for rr add. If a message id is specified, it will show additional information about that particular reaction role. |
	| **rr add [channel] &lt;msg\_id&gt; &lt;emoji&gt; &lt;role&gt;** | !rr add 458641514017587210 👼 @pure | Adds the emoji-role pair to the message and the database.<br>**NOTE:** This message id can belong to authors other than Carl-bot, and the same emoji can be used for different messages for different roles (useful for regional roles) |
	| **rr addmany [channel] &lt;msg\_id&gt; &lt;emoji role...&gt;** | !rr addmany 458641514017587210 👼 @pure<br>💩 @fortnite<br>😁 @league of legends | Works like **!rr add** except it adds more than one role at a time.<br>**SEPARATE EACH EMOJI-ROLE PAIR WITH A NEW LINE USING:  ** ++shift+enter++ |
	| **rr remove &lt;msg\_id&gt; &lt;role&gt;** | !rr remove 458641514017587210 @fortnite | Removes an emoji-reaction pair from the specified bot message. |
	| **rr clear [msg\_id]** | !rr clear 458641514017587210 | If you specify a message id, it removes all the roles from the message, if you don't, it will remove **all** reaction roles from the server. |
	| **rr bl &lt;msg\_id&gt; &lt;roles...&gt;** | !rr bl 458641514017587210 Staff | Prevents members with this role from picking up roles from the message.  |
	| **rr wl &lt;msg\_id&gt; &lt;roles...&gt;** | !rr wl 458641514017587210 Staff | Only members with one of these roles can pick up roles from the message. |
	| **rr unbl &lt;msg\_id&gt;&lt;roles...&gt;** | !rr unbl 458641514017587210 Staff | Removes a blacklisted role from the indicated reaction role message allowing for the role to pick up new roles from the message. |
	| **rr unwl &lt;msg\_id&gt;&lt;roles...&gt;** | !rr unwl 458641514017587210 Staff | Removes a whitelisted role from the indicated reaction role message preventing the role from picking up new roles from the message. |
	| **rr clearbl &lt;msg\_id&gt;** | !rr clearbl 458641514017587210  | Removes all roles from your blacklist for that set of reaction roles. |
	| **rr clearwl &lt;msg\_id&gt;** | !rr clearwl 458641514017587210  | Removes all roles from your whitelist for that set of reaction roles. |
	| **rr selfdestruct &lt;msg\_id&gt; &lt;time&gt;** | !rr selfdestruct 458641514017587210 7d | Deletes the message and all of its reaction roles after the time is up. |
	| **rr edit &lt;msg\_id&gt; &lt;title \| description&gt;** | !rr edit 458641514017587210 Games \| Click on the games you want to be notified by | Edits the title and description, works like it does in the make command |
	| **rr [channel\|cc] [name=get-roles]** | !rr cc color-roles | Creates a channel with the sort of permissions you most likely want for a reaction role channel (yes, add reactions is off, this is intentional) |
	| **rr fix** | !rr fix | Accidentally (or intentionally) cleared all reactions? Use this command to have the bot add the reactions missing |

### RR Types

!!! info
    Types are per message and change their behavior. Every message has a type which defaults to normal.

???+ tldr "RR Behavioral Types"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **rr unique &lt;msg\_id&gt;** | !rr unique 458641514017587210 | Marks a message as 'unique' meaning a member can only claim one role from this message at a time, this works per message. Automatically removes the old reactions for you |
	| **rr binding &lt;msg\_id&gt;** | !rr binding 458641514017587210 | A combination of rr verify and rr unique. Allowing for members to limit people to one choice ever. |
	| **rr link &lt;base\_id&gt; &lt;target\_id&gt;** | !rr link 458641514017587210 445066811097219082 | By linking two or more messages together, only one role from either message can be self-assigned. If you have 30 color roles for instance, linking the two messages together (since the limit is 20/message) allows a smooth, user-friendly experience when picking up roles. |
	| **rr unlink &lt;msg\_id&gt;** | !rr unlink 458641514017587210 | This breaks apart the entire group created by `!rr link` This means if you had three messages linked together, none of them will be after using this command. |
	| **rr verify &lt;msg\_id&gt;** | !rr verify 458641514017587210 | With this enabled, reactions can only assign roles, not take them away. Additionally the bot automatically removes the reaction after the user reacts. This is useful for servers that want a verification reaction |
	| **rr drop &lt;msg\_id&gt;** | !rr drop 458641514017587210 | Works sort of like rr verify, except it can only remove roles (and roles are removed when the emoji is added). This can be used for servers that automatically assign a role that you wish to remove. |
	| **rr normal &lt;msg\_id&gt;** | !rr normal 458641514017587210 | This returns the reaction role message back to a normal reaction role message. Meaning any commands applied to it such as verify or unique will be removed. |
	| **rr temp &lt;msg\_id&gt;  &lt;time&gt;** | !rr temp 458641514017587210 24h | [Patreon only](https://www.patreon.com/carlbot): This allows for roles to be temporarily be assigned to a member and then removed after the designated amount of time. |
	| **rr reversed &lt;msg\_id&gt;** | !rr reversed 458641514017587210 | Reacting removes roles, unreacting adds roles. |
	| **rr lock &lt;msg\_id&gt;** | !rr lock 458641514017587210 | Locks the message preventing any roles from being handed out. |
	| **rr limit &lt;msg\_id&gt; &lt;limit&gt;**  | !rr limit 458641514017587210 5 | Limits members to picking up x amount of roles from a message. |

### Advanced/niche

!!! warning
    These commands come in very handy in certain situations, but may cause confusion to people unfamiliar with how Carl-bot's reaction roles work.

???+ tldr "Advanced/niche RR Commands"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **rr move &lt;base\_id&gt; &lt;target\_id&gt;** | !rr move 458641514017587210 445066811097219082 | Moves the reaction roles from one message to another. This works even if the message was purged (using the message id found in !rr show). |
	| **rr aio &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | !rr aio \#reaction eeaaee "hello there \| this is a description" :red: hello :purple: there | **SEPARATE EACH EMOJI-ROLE PAIR WITH A NEWLINE** This is meant for power users who wish to create everything with just one command. The title and description have to be enclosed in double quotes. |
	| **rr aiou &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | Works like **!rr aio** but also marks the message as unique |
	| **rr aiov &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create a verification reaction role. |
	| **rr aioi &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create an inverse verification reaction role, i.e. one that only removes roles. |
	| **!rr fixforeign &lt;msg\_id&gt;** | !rr fixforeign 458641514017587210 | Super niche command which can be used to have the bot react to emojis the bot doesn't have access to. One reason you might want to use this is because you want to use google's blob emojis. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. **YOU HAVE TO REACT TO THE MESSAGE WITH THE EMOJIS YOURSELF BEFORE USING THIS COMMAND** |
	| **rr maxroles &lt;msg\_id&gt; [&lt;role&gt; &lt;number&gt;...]** | !rr maxroles 458641514017587210 DPS 10 | Want to limit the number of x role? With this, you can. **NOTE** This checks for how many people have the role, not how many reactions there are. |
	| **rr [colour\|color] &lt;msg\_id&gt; &lt;color&gt;** | !rr color 458641514017587210 \#00ee28 | Changes the accent color of the specified  bot message |

[The fastest and most reliable unique reaction roles of any bot.](https://i.imgur.com/A7ShLfZ.mp4)

![Me setting up reaction roles in my support server.](../images/reaction_role_setup.png)
