# Welcome and leave messages

!!! info
    Use the dashboard! It allows for easier setup and embeds

!!! info
    These commands do nothing before using set welcome &lt;\#channel&gt;

| Name | Example | Usage |
| :--- | :--- | :--- |
| **set welcome &lt;\#channel&gt;** | !set welcome \#join-say-hi | Sets the channel where welcome/leave/banmsg messages will be posted. |
| **\[welcome\|greet\] &lt;text&gt;** | !greet Welcome {mention}, we've been expecting you | Sets up a welcome message that will be sent when a new user joins. |
| **\[leave\|farewell\] &lt;text&gt;** | !farewell Goodbye {user}, maybe it wasn't meant to be... | Like !greet but for people leaving |
| **banmsg &lt;text&gt;** | !banmsg **{user}** just got blown the fuck out | Like !greet but for people getting banned |
| **\[dmjoin\|pmjoin\|joindm\|joinpm\] &lt;text&gt;** | !dmjoin Hello and welcome to {server}, before chatting you need to assign roles in \#get-roles | Like !greet except it dms the message to the user upon joining |
| **testgreet** | !testgreet | Not sure how your welcome/farewell/dm messages actually look? Just type !testgreet and have the bot spit out all of them. |

All these messages will be sent to the channel saved with `!set welcome`. **Use a command without any text to remove the message.** Supports the following variables:

`{mention}` - Pings the user

`{user}` - The name of the user

`{server}` - The name of the server

`{user(id)}` - The ID of the user

`{user(proper)}` - The name including the last four digits \(Carl\#0001\).

`{server(members)}` - The number of members on the server \(after the event has happened\). Use `{ord:{server(members)}}` to turn 8102 into 8,102nd etc.

Also supports `{random: lists, separated by commas}` and `{math: 1 + 1} math blocks` not sure when you'd ever want a math block but random lists are pretty useful.

