# Basic bot setup

!!! info
    This is much easier done on the website at [https://carl.gg](https://carl.gg)

This guide will cover everything you need to do to get started with everything carlbot offers.

**1. Setting up the prefix**

I want the bot to respond when I use the prefix `-` to do that, I can type `!prefix set -`. Carlbot offers up to 15 prefixes at once, so I could also add a second prefix by typing `!prefix add .`

**2. Setting up all the channels**

`!log channel <#channel>` Sets the channel where carlbot will log things such as message deletions, name changes, role updates. More on that later.

`!set welcome <#channel>` Decides where join/leave/ban messages go, more on that later.

**3. Setting up reaction roles**

Reaction roles work best in their own channels, so carlbot offers a command to create a channel specifically for reaction roles with some permissions that most people will find useful. We can create this channel by typing `!rr channel`

It's recommended that you use `!rr make` for this if you are new.

![](https://i.imgur.com/W2KAAPa.png)

**4. Setting up modlogs**

Since we're doing this from a clean slate, I will use `!modlogs create` to create a channel with the appropriate permissions. If we already had a channel where moderation actions were sent, we could have used `!modlogs set <#channel>`

**5. Setting up starboard**

`!starboard` will create the starboard

`!star limit <count>` will change the required number of stars for a post to show up in the starboard.

**6. Configuring the log to log what you care about**

By default, the log will log everything every member does in every channel, this isn't always what we want.

Let's say we don't care about message edits, the way we stop those from showing up in the log is by typing `!log edit`. The `!log` command takes an event as its argument and tries to figure out what you want toggled. Another thing we can do is ignore messages deleted in certain channels. Maybe we don't care about messages deleted in mod channels. `!log ignore #illuminati` is how we'd ignore events from the channel \#illuminati. Read the full page for more info, it's _very_ customizable.

**7. Setting up a mute role**

By typing `!muterole create` we can create a role with the permission "send messages" denied in every channel. Please note that any future channels created will not be covered by the bot. Users can now mute with the `!mute <@member> [time] [reason]` command

**8. Adding twitch streamers**

No point setting up a twitch channel if you don't have any streamers to track. I enjoy watching b0aty, so I'll add him by typing `!twitch b0aty`. Now any time b0aty comes online I will be notified.

**9. Setting up join messages**

First we will set the message sent to the previously set channel with `!welcome Hello there $user, glad to have you in the tutorial server`. Next up, we can also set a different message to be sent directly to the member upon joining by typing `!joindm Hello and welcome to the tutorial server, please read #rules and respect the other members`

This is far from everything carlbot has to offer, but at this point you will have set up most of the things that you can set up.

