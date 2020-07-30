# Starboard

!!! info
    After you make a Starboard channel, your server's users can react to any message with a ⭐ `(:star:)` to 'vote' to display that message as a post on the starboard. Once the message gets enough :star: reactions, Carlbot posts it onto the starboard. By default, a user's :star: reaction on their own post doesn't count. Starboard is commonly described as being 'democratic pins'.

| Name | Example | Usage |
| :--- | :--- | :--- |
| **starboard [#channel=starboard]** | !starboard meme-archive | Sets up the starboard for the server. If an existing channel is mentioned that channel becomes the starboard, otherwise this creates a new channel with the specified name and makes it into the server's "starboard", with "starboard" as the name if no name is provided. Choose wisely, this channel cannot be changed. |
| **star limit &lt;number&gt;** | !star limit 3 | Sets the amount of stars required for a post to get posted to the starboard |
| **star nsfw** | !star nsfw | Toggles nsfw stars. With this enabled, posts starred in channels marked as nsfw will embed |
| **star self** | !star self | Toggles being able to star your own posts |
| star [stats\|top] [@member] | !star stats @Carl#0080 | Shows some information about the server's or user's starred posts and giving patterns. |
| star show &lt;message\_id&gt; | !star show 463069834968825856 | Shows a starred post from the starboard in the channel the command was used in, you can find the id in the footer of each starboard entry. |
| star [jump\|source] | !star jump |  Will add a jump link to the starred message. |

Star messages, have them posted to a channel. It's a fun way to save funny/interesting messages in a place where everyone can see them.

![](https://i.imgur.com/FIpBei2.png)

