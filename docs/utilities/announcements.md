# Announcements

!!! info
    Timezones suck, use the dashboard at [https://carl.gg](https://carl.gg) to create autofeeds with your local timezone

!!! info
    The id argument is the autofeed id which the bot spits out when you create an autofeed or when you do !af

| Name | Example | Usage |
| :--- | :--- | :--- |
| **feed** | -- | Lists all the feeds that have been set up in the server. |
| **feed create &lt;name&gt; &lt;role&gt;** | !feed create got game of thrones | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned. |
| **announce** | !feed announce got Hey guys, everyone dies | Makes an announcement to the specified feed. |
| **feed \[delete\|-\|del\|remove\]** | !feed delete got | Deletes a feed. Note: This does not delete the associated role, so if you created one specifically for a feed, you need to delete it. |
| **!feed clear** | -- | Deletes ALL feeds from the server. |
| **!feed move** | !feed move bot \#announcements | Moves a feed to a specified channel. Note: You need send messages permissions in the channel you move it to. |
| **\[af\|autofeed\]** | -- | Lists all autofeeds set up in the server. |
| **autofeed &lt;role&gt; &lt;time&gt; &lt;message&gt;** | !autofeed "final fantasy xiv" 18h The servers have been reset, get out there! | Normal autofeeds \(the ones created by this command\) will ping the role  specified when setting them up. |
| **autofeed silent &lt;time&gt; &lt;message&gt;** | !autofeed silent 2 hours Vote for carlbot on discord bots! | Like a normal autofeed except it does not have a role associated with it and thus, does not ping anything. |
| **autofeed silence &lt;id&gt;** | !autofeed silence 37 | Silences an already existing normal feed. |
| **autofeed repeat &lt;id&gt;** | !autofeed repeat 13 24h | Marks an autofeed to be repeated. This keeps going until you delete the autofeed. |
| **autofeed remove &lt;id&gt;** | !autofeed remove 77 | Removes an autofeed |
| **autofeed clear** | -- | Removes ALL autofeeds. |
| **autofeed move &lt;id&gt; &lt;\#channel&gt;** | !autofeed move 73 \#general | Moves an autofeed to a specified channel. Note: You need send messages permissions in the channel you move it to. |

What are feeds? Feeds are a way for you to make announcements and ping a specific role without having to deal with the annoyances and potential abuse from either having a pingable role or manually toggling inbetween pingable and not.

Automatic feeds on the other hand can be seen as group reminders, and they share a lot of functionality with reminders.

