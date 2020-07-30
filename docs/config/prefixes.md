# Prefixes

!!! danger
    **!prefix clear** leaves you without a prefix meaning you have to mention the bot to set a new one. **!prefix set &lt;prefix&gt;** is most likely a better choice in most cases

!!! info
	Carl-bot's default prefixes are `@Carl-bot#1536`, `!` and `?`

| Name | Example | Usage |
| :--- | :--- | :--- |
| prefix | !prefix | Lists the prefixes currently in use by the server |
| **prefix add &lt;prefix&gt;** | !prefix add "sudo " | Adds a prefix to be used by the bot (limited to 10) **NOTE** if you want a two word prefix or a prefix with a space after it or an emoji you **must** use quotes, this is a discord limitation and can't be fixed |
| **prefix set &lt;prefix&gt;** | !prefix set "haha " | Sets the specified prefix to be the ONLY prefix in the server |
| **prefix remove &lt;prefix&gt;** | !prefix remove ! | Removes a prefix, same limits as !prefix add applies here, can't remove mentioning the bot. |
| **prefix clear** | !prefix clear | Removes all prefixes except mentioning the bot. This (obviously) means you need to mention the bot to register more prefixes |

![](../images/prefixes.png)

