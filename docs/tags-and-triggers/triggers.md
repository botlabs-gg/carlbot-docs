# Triggers

!!! warning
    Autoresponses are not custom commands, if you want things that are triggered by a prefix and a keyword, see the tag section. They offer more functionality, better editing capabilities, will _never_ have a limit to them and are just generally nicer for their intended purpose.

| Name | Example | Usage |
| :--- | :--- | :--- |
| **\[ar\|autoresponse\]** | -- | Lists the triggers, and ignores for the server |
| **ar list** | -- | Lists all the triggers in a paginated fashion |
| **ar \[add\|create\] &lt;trigger&gt; &lt;response&gt;** | !ar add "hello there" Hello! I'm a bot created by carl :muscle: | Adds a trigger that carlbot will look for and say/do something when it is said. This command looks for a substring within the message, meaning that if you add _hi_ then _t_**hi**_s_ will also match. See the next command if that is too greedy for you. |
| **ar \[strict\|s\] &lt;trigger&gt; &lt;response&gt;** | !ar strict "its coming home" {reactu: ⚽️} | This works a lot like normal ar add with one vital exception: it looks for exact sequences of words, rather than substrings. What this means is that if you add the strict trigger `hell` and someone says `hello` it will not match, it also means that triggers with more than one word requires an exact match per word \(this is a lot more reasonable to use than this text makes it out to be\). |
| **ar \[exact\|e\] &lt;trigger&gt; &lt;response&gt;** | !ar exact "hey guys" Hello! | This matches if the content of a message is the same as the trigger. Some exceptions such as punctuation and capitalization applies. |
| **ar \[startswith\|sw\] &lt;trigger&gt; &lt;response&gt;** | !ar sw "how do i" read the wiki! | Matches if the start of the message matches |
| **ar \[endswith\|ew\] &lt;trigger&gt; &lt;response&gt;** | !ar ew "i think" no you don't | Like startswith except if it ends with it. |
| **ar \[remove\|del\|-\|delete\] &lt;trigger&gt;** | !ar del its coming home | Removes an autoresponse |
| **ar clear** | -- | Removes all autoresponses \(with a prompt\) |
| **ar \[channel\|cs\] &lt;trigger&gt; &lt;response&gt;** | !ar channel "king crimson" HOW DOES KING CRIMSON WORK I DON'T UNDERSTAND | Like a normal autoresponse except it only listens in the channel you used the command in. **Note:** This will bypass any channel ignores \(member ignores still work\). |
| **ar ignore &lt;members or channels...&gt;** | !ar ignore @Carl\#0001 @Kintark\#0588 \#general  @idiotuser\#1337 \#welcome | Blocks channels and or users from triggering responses |
| **ar unignore &lt;members or channels...&gt;** | !ar unignore \#general @Carl\#0001 | Undoes what !ar ignore does |

Autoreactions support most of tagscript, see [Tags - Advanced usage to learn more](https://docs.carl.gg/tags-and-responses/tags-advanced-usage)

