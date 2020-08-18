# Moderation

### Setup

!!! tip
	Anyone can use the `report` command, and by default Carl-bot will delete the command invocation when used. Instruct your users to use it in the channel where the event they're reporting happened, so your staff can make use of the jump link the report generates.

???+ tldr "Setup Commands"
	
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **muterole &lt;role&gt;** | !muterole kids table | Selects a role to use for the mute command |
	| **muterole create [name='muted']** | !muterole create shhh | Creates a new role, adds the role as a channel override with "send messages" turned off for all text channels and sets it as the server's muterole. |
	| **muterole update** | !muterole update | Updates the channel overwrites for the currently chosen muterole in any channels that miss them |
	| **reportchannel &lt;channel&gt;** | !reportchannel \#reports |  Sets the channel where reports are sent. |
	| report &lt;message&gt; | !report Carl big meanie | Sends a report to the reportchannel. Usable by anyone. |
	| **setnick &lt;member&gt; &lt;name&gt;** | !setnick @Carl#0080 Do not ping | Changes the user&apos;s nickname. |
	| **lockdown setup** | !lockdown setup | Only available to Carl-bot Patrons. Toggles OFF send messages from all roles except @everyone |

### Punishments

???+ tldr "Punishment Commands"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **ban &lt;@member/ID&gt; [days=2] [reason]** | !ban 102130103012 raiding | Bans the member from the server. This works even if the member isn't on the server. If you supply a reason, it will show up in the modlogs and in discord's built in audit log. Days refer to the amount of days to purge messages from them. |
	| **mute &lt;@member&gt; [time] [reason]** | !mute @Carl\#0001 20h45m spamming | Mutes a member (using the muterole, read above) for the specified time. If no time is given, it will mute indefinitely. If a reason is given, it shows up in the mod logs. |
	| **hardmute &lt;@member&gt; [time] [reason]** | !hardmute @Carl\#0001 20h45m spamming | Functions similar to mute, but removes all of the specified user's other roles. If the hardmute is temporary the roles will be given back upon it expiring. |
	| **unmute &lt;@member&gt;** | !unmute @Carl\#0001 | Unmutes a member |
	| **kick &lt;@member&gt; [reason]** | !kick @Carl\#0001 racism | Kicks a member. Reason shows up in the modlogs and in audit logs |
	| **softban &lt;@member&gt; [days=2] [reason]** | !softban @Carl\#0001 go away | Bans and immediately unbans a member to clear 48 hours of message history. |
	| **tempban &lt;@user&gt; [days=2] [reason]** | !tempban @Carl\#0001 20h big ugly | Bans a user for the specified duration regardless if they're on the server or not. |
	| **massban [days=2] &lt;@members...&gt;** | !massban 123124151241 @Carl\#0001 12152252634 123123901231 | Bans more than one person, each ban shows up in the modlog. |
	| **warn &lt;@member&gt; [reason]** | !warn @Carl\#0001 do not spam reactions | Warns a user, pms them the reason and posts it to the modlog. |

### Managing Warns

???+ tldr "Managing Warns"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **warns &lt;@member&gt;** | !warns @Carl\#0001 | Lists all current warnings in the server. Specify a member to see all of their warnings. |
	| **removewarn &lt;case\_number&gt;** | !removewarn 17 | Removes a warning by its case number. |
	| **clearwarn &lt;@member&gt;** | !clearwarn @Carl\#0001 | Removes all warnings from a user. |

### User Notes

???+ tldr "Note Commands"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **setnote &lt;@member&gt; &lt;note&gt;** | !setnote @MichaelAus\#9999 favorite Australian | Assigns the note to the member specified. |
	| **notes &lt;@member&gt;** | !notes @Carl\#0001 | Displays all of a member's notes. |
	| **removenote &lt;note_number&gt;** | !removenote 56 | Removes a note by number. |
	| **clearnotes &lt;@member&gt;** | !clearnotes @Carl\#0001 | Removes all notes from a member. |

### Server/Channel Lockdown

!!! warning
    Locking down a channel denies the @everyone role `send messages` as an override in the specified channel. Any roles explicitly granting send messages will override this for anyone with that role. Locking down the server removes send messages from the @everyone role. You set up your server correctly by removing send messages from all non-mod roles.

???+ tldr "Lockdown Commands"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **lockdown &lt;\#channel&gt; &lt;duration&gt;** | !lockdown \#general 20m | Locks the specified channel (or the one the command is used in if none is specified) for [duration] if specified else forever. |
	| **unlockdown &lt;\#channel&gt;** | !unlockdown \#general |  Undoes what !lockdown does. |
	| **lockdown server &lt;duration&gt;** | !lockdown server 20m | Locks all channels in the server. |
	| **unlockdown server** | !unlockdown server |  Undoes what !lockdown server ****does. |

### Bulk Message Deletion

!!! info
    Purge Commands ignore pinned messages. `cleanup` does **NOT**.
	
???+ tldr "Bulk Message Deletion Commands"
	The search number is how many messages you want Carl-bot to look through whilst checking for offenders, or messages that match the parameters of the purge type used.

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **purge [search=100]** | !purge 200 | Purges the last howmany messages. |
	| **purge bot [search=100] [prefix]** | !purge bot 20 ? | Purges the bot messages (and messages with the specified prefix) from the last howmany messages. |
	| **purge contains [search=100] &lt;substring&gt;** | !purge contains 12 thanos | Purges messages containing the specified substring. |
	| **purge user &lt;member&gt; [search=100]** | !purge user @Carl#0001 20 | Purges messages from the specified user. |
	| **purge all [search=100]** | !purge all 13 | Purges the last howmany messages |
	| **purge embeds [search=100]** | !purge embeds 12 | Purges messages with embeds. |
	| **purge emoji [search=100]** | !purge emoji 6 | Purges messages that contain custom emoji. |
	| **purge files [search=100]** | !purge files 21 | Purges messages with attachments. |
	| **purge images [search=100]** | !purge images 11 | Purges messages with attachments or embeds |
	| **purge links [search=100]** | !purge links 15 | Purges messages that contain links. |
	| **purge [mentions\|pings] [search=100]** | !purge pings 25 | Purges messages that contain mentions. |
	| **purge [human\|humans] [search=100]** | !purge humans 13 | Purges messages sent by user accounts, ignores bot messages. |
	| **purge reactions [search=100]** | !purge reactions | Removes all reactions from messages that have them. |
	| **cleanup [search=100]** | !cleanup 8 | Sort of like !purge bot except just for carlbot and works for all prefixes. |