# Announcements

### Feeds

???+ info "What are feeds?"
	What are feeds? Feeds are a way for you to make announcements and ping a specific role without having to deal with the annoyances and potential abuse from having a mentionable role or manually toggling a role inbetween mentionable and not. You need Manage Server Discord permissions to use the feed commands.<br><br>A feed is an association between a role and a channel. When you use the feed announce command, the role will be set to mentionable very briefly, the role will be pinged and your message will be sent in the channel with which the feed is associated, and the role will subsequently be set back to unmentionable.

???+ tldr "Feed Commands"
	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **feed** | !feed | Lists all the feeds that have been set up in the server. |
	| **feed create &lt;name&gt; &lt;role&gt;** | !feed create got game of thrones | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned. |
	| **announce** | !feed announce got Hey guys, everyone dies | Makes an announcement to the specified feed. |
	| **feed \[delete\|-\|del\|remove\]** | !feed delete got | Deletes a feed. Note: This does not delete the associated role, so if you created one specifically for a feed, you need to delete it. |
	| **!feed clear** | !feed clear | Deletes ALL feeds from the server. |
	| **!feed move** | !feed move bot \#announcements | Moves a feed to a specified channel. Note: You need send messages permissions in the channel you move it to. |

### Autofeeds

Automatic feeds can be seen as group reminders, and they share a lot of functionality with reminders.

!!! tip
    Timezones suck, use the dashboard at [https://carl.gg](https://carl.gg) to create autofeeds with your local timezone.

???+ tldr "Autofeed Commands"
    The id argument is the autofeed id which the bot spits out when you create an autofeed or when you do `!af`

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **\[af\|autofeed\]** | !af | Lists all autofeeds set up in the server. |
	| **autofeed &lt;role&gt; &lt;time&gt; &lt;message&gt;** | !autofeed "final fantasy xiv" 18h The servers have been reset, get out there! | Normal autofeeds \(the ones created by this command\) will ping the role  specified when setting them up. |
	| **autofeed silent &lt;time&gt; &lt;message&gt;** | !autofeed silent 2 hours Vote for carlbot on discord bots! | Like a normal autofeed except it does not have a role associated with it and thus, does not ping anything. |
	| **autofeed silence &lt;id&gt;** | !autofeed silence 37 | Silences an already existing normal feed. |
	| **autofeed repeat &lt;id&gt;** | !autofeed repeat 13 24h | Marks an autofeed to be repeated. This keeps going until you delete the autofeed. |
	| **autofeed remove &lt;id&gt;** | !autofeed remove 77 | Removes an autofeed |
	| **autofeed clear** | !af clear | Removes ALL autofeeds. |
	| **autofeed move &lt;id&gt; &lt;\#channel&gt;** | !autofeed move 73 \#general | Moves an autofeed to a specified channel. Note: You need send messages permissions in the channel you move it to. |