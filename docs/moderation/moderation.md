# Moderation

!!! info
    Purge Commands ignore pinned messages.

!!! warning
    Locking down a channel denies the @everyone role `send messages` as an override in the specified channel. Any roles explicitly granting send messages will override this for anyone with that role. Locking down the server removes send messages from the @everyone role. You set up your server correctly by removing send messages from all non-mod roles.

| Name | Example | Usage |
| :--- | :--- | :--- |
| **ban &lt;@member/ID&gt; \[days=2\] \[reason\]** | !ban 102130103012 raiding | Bans the member from the server. This works even if the member isn't on the server. If you supply a reason, it will show up in the modlogs and in discord's built in audit log. Days refer to the amount of days to purge messages from them. |
| **muterole &lt;role&gt;** | !muterole kids table | Selects a role to use for the mute command |
| **muterole create \[name='muted'\]** | !muterole create shhh | Creates a new role, adds the role as a channel override with "send messages" turned off for all text channels and sets it as the server's muterole. |
| **muterole update** |  | Updates the channel overwrites for the currently chosen muterole in any channels that miss them |
| **mute &lt;@member&gt; \[time \[reason\]\]** | !mute @Carl\#0001 20h45m spamming | Mutes a member \(using the muterole, read above\) for the specified time. If no time is given, it will mute indefinitely. If a reason is given, it shows up in the mod logs. |
| **unmute &lt;@member&gt;** | !unmute @Carl\#0001 | Unmutes a member |
| **kick &lt;@member&gt; \[reason\]** | !kick @Carl\#0001 racism | Kicks a member. Reason shows up in the modlogs and in audit logs |
| **softban &lt;@member&gt; \[days=2\]\[reason\]** | !softban @Carl\#0001 go away | Bans and immediately unbans a member to clear 48 hours of message history. |
| **tempban &lt;@user&gt; \[days=2\]\[reason\]** | !tempban @Carl\#0001 20h big ugly | Bans a user for the specified duration regardless if they're on the server or not. |
| **massban \[days=2\]&lt;@members...&gt;** | !massban 123124151241 @Carl\#0001 12152252634 123123901231 | Bans more than one person, each ban shows up in the modlog. |
| **warn &lt;@member&gt; \[reason\]** | !warn @Carl\#0001 do not spam reactions | Warns a user, pms them the reason and posts it to the modlog. |
| **removewarn &lt;case\_id&gt;** | !removewarn 17 | Removes a warning by its case id. |
| **clearwarn &lt;@member&gt;** | !clearwarn @Carl\#0001 | Removes all warnings from a user. |
| **setnote &lt;@member&gt; &lt;note&gt;** | !setnote @MichaelAus\#9999 favorite Australian | Assigns the note to the member specified. |
| **notes &lt;@member&gt;** | !notes @Carl\#0001 | Displays all of a member's notes. |
| **removenote &lt;note_id&gt;** | !removenote 56 | Removes a note by id. |
| **clearnotes &lt;@member&gt;** | !clearnotes @Carl\#0001 | Removes all notes from a member. |
| **purge \[count=100\]** | !purge 200 | Purges the last howmany messages. |
| **purge bot \[count=100\]** | !purge bot ? 20 | Purges the bot messages \(and messages with the specified prefix\) from the last howmany messages. |
| **purge contains \[count=100\]** | !purge contains thanos | Purges messages containing the substring |
| **purge user \[count=100\]** | !purge user @Carl\#0001 20 | Purges messages from the user |
| **purge all \[count=100\]** | !purge all 13 | Purges the last howmany messages |
| **purge embeds \[count=100\]** | !purge embeds 12 | Purges the last howmany messages with embeds |
|  **purge emoji \[count=100\]** | !purge emoji | Purges the last howmany messages containing custom emoji |
| **purge files \[count=100\]** | !purge files | Purges messages with attachments |
| **purge images \[count=100\]** | !purge images | Purges messages with attachments or embeds |
| **purge links \[count=100\]** | !purge links | Purges messages with links |
| **purge reactions \[count=100\]** | !purge reactions | Purges reactions from messages |
| **cleanup \[count=100\]** | -- | Sort of like !purge bot except just for carlbot and works for all prefixes |
| **lockdown &lt;\#channel&gt; &lt;duration&gt;** | !lockdown \#general 20m | Locks the specified channel \(or the one the command is used in if none is specified\) for \[duration\] if specified else forever. |
| **unlockdown &lt;\#channel&gt;** | !unlockdown \#general |  Undoes what !lockdown does. |
| **lockdown server &lt;duration&gt;** | !lockdown server 20m | Locks all channels in the server. |
| **unlockdown server** | !unlockdown server |  Undoes what !lockdown server ****does. |

