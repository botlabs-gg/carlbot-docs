# Twitch notifications

!!! danger
    You have to set a twitch channel with !set twitch &lt;\#channel&gt; before any notifications will be sent.

| Name | Example | Usage |
| :--- | :--- | :--- |
| **twitch &lt;name&gt; \[alias\]** | !twitch azortharion azor | Adds the user with the alias. In the example given, the stream announcement will say "azor is now live". This command also removes a streamer if used again. |
| twitch list | -- | Shows all registered streamers and when they were last online |
| twitch online |  | Shows all currently online streamers |
| **twitch own** | -- | With this enabled, users can't have the streams they themselves added removed by non-mods, this is useful if you want to allow users to add their own streams to a server |
| **twitch mod** | -- | If this is disabled, any user can add a stream of their choice |
| **twitch limit &lt;number&gt;** | !twitch limit 2 | Restricts how many streams non-mods are allowed to add |

