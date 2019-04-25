# Embeds

!!! info
    !cembed and !ecembed take raw json as their arguments. If you're new to embeds, using [leovoel's embed visualizer](https://leovoel.github.io/embed-visualizer/) can be helpful as it shows you how it will end up looking instantly.

| Name | Example | Usage |
| :--- | :--- | :--- |
| !embed \[channel\] &lt;color&gt; &lt;title \| description&gt; | !embed \#get-roles eeaaee I'm a title \| and I'm the description | Creates a simple embed with the colored strip, a title and a description. |
| **!editembed &lt;msg\_id&gt; &lt;title \| description&gt;** | !editembed 32538901189123 I'm a new title \| and I'm an updated description | Edits a message in the same format you create basic embeds |
| **!rr color \[channel\] &lt;msg\_id&gt; &lt;color&gt;** | !rr color 182923492394927 eeeaaa | Edits the color strip on the left side of the embed. If the embed is not a reaction role embed, you need to either use the command in the same channel as the embed or specify it as the first argument. |
| !cembed  \[channel\] &lt;json&gt; | !cembed \#secret {"title": "hello world"} | Also accepts a pastebin link since it can be bigger than 2000 characters. |
| **!ecembed &lt;msg\_id&gt; &lt;channel&gt; &lt;json&gt;** | !ecembed 31203123191 \#secret {"title": "Woah, a new title!"} | Edits ANY embed the bot has posted. |
| !embedsource &lt;msg\_id&gt; \[channel\] | !embedsource 9312838121123 \#bilderberg | Gets the raw json from an embed |




