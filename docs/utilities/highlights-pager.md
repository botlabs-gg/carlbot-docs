# Highlights/pager



### Highlights

Highlighting means you will receive a message when your keyword is said in chat. The matching is approximate and works really similarly to discord search \(basically, if you search your keyword in discord search, you will find messages that would trigger the highlight, roughly speaking\). 

!!! info
    You will only be highlighted if you have access to the channel and if you haven't posted in the past 5 minutes.



| Name | Example | Usage |
| :--- | :--- | :--- |
| hl \[+\|add\] &lt;word\(s\)&gt; | !hl add carl | Adds a word that will notify you. **IMPORTANT:** The bot tries to guess when you're aware of what's being typed and won't notify you if you've typed in the past 5 minutes, to see if your highlights work, please use `!hl match <sentence>`. Additionally, when adding a multi-word highlight, it will check for a sequence of words, not a substring. |
| hl \[m\|match\] &lt;sentence&gt; | !hl match carl is cute | Tests a sentence and sees which if any words would notify you. |
| hl block &lt;members/channels&gt; | !hl block @Kintark\#0588 \#general @angryloser\#0001 \#bilderberg | Messages sent in this channel/from this user won't notify you. |
| hl unblock &lt;members/channels&gt; | !hl unblock \#general | Unblocks the user/channel |
| hl show | -- | Shows which words you have set to highlight you |
| hl clear | -- | Removes all of your highlighted words |
| hl del &lt;word&gt; | !hl del math | Removes a word from your highlighted words |

