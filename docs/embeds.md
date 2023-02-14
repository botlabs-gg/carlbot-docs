?> The commands `cembed` and `ecembed` take raw JSON as their arguments. If you are new to embeds, using the **[Dashboard](https://carl.gg)** would be helpful as the **Embed** section lets you fill in an embed template and shows you how it will end up looking instantly.

## Embed Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **embed [channel] \<color> \<title> \| \<description>** | `!embed #welcome FF0000 Title \| Description` | Creates a simple embed with color, title and description. |
| **editembed \<message id> \<title> \| \<description>** | `!editembed 32538901190123 Title \| Description` | Edits an embed sent by the bot in a message. |
| **cembed [channel] \<JSON>** | `!cembed #welcome` | Creates a fully customized embed. Also accepts a Pastebin link. |
| **ecembed \<message id> \<channel> \<JSON>** | `!ecembed 31203123191 #welcome` | Edits any embed the bot has posted using the JSON or JSON source that follows the message ID and channel. |
| **embedsource \<message id> [channel]** | `!embedsource 9312838121123 #welcome` | Gets the raw JSON from an embed. |

<!-- tab:Slash Commands -->
| Name              | Example           | Usage                                                                         |
| ----------------- | ----------------- | ----------------------------------------------------------------------------- |
| **embed create \<color> \<text> [channel]** | `/embed create FF0000 Title \| Description #welcome` | Creates a simple embed with color, title and description. |
| **embed edit \<message id> \<text>** | `/embed edit 32538901190123 Title \| Description` | Edits an embed sent by the bot in a message. |
| **embed custom \<JSON> [channel]** | `/embed custom #welcome` | Creates a fully customized embed. Also accepts a Pastebin link. |
| **embed editcustom \<message id> \<JSON> \<channel>** | `/embed editcustom 31203123191 #welcome` | Edits any embed the bot has posted using the JSON or JSON source that follows the message ID and channel. |
| **embed source \<message id> [channel]** | `/embedsource 9312838121123 #welcome` | Gets the raw JSON from an embed. |

<!-- tabs:end -->


## Embed Builder

!["Embed Builder](_images/embed_builder.png ':size=75%')

> `I` = Icon URL
`T` = Thumbnail URL
`Image` = Image URL
`F` = Footer Icon

*Image URLs must be direct image links. This means the URL should contain the image's file extension, like `.jpg`, `.jpeg`, `.png`, or `.gif`.*


## Rules and Limits

- URL fields must be an HTTP/HTTPS formatted URL (begins with http:// or https://).
- All Title fields, the (Author's) Name field, and the Footer cannot properly display Discord mentions or named links, and have limited support of markdown formatting.
- If an additional field exists, neither the title nor the description can be empty.
- **Name** must have a value for **Name URL** to work.
- **Title** must have a value for **Title URL** to work.
- **Name** must have a value for **Icon URL** to display.
- **Footer** must have a value for the **Footer Icon** to display.
- In addition to the stated character limits for each field provided below the embed builder's text boxes, the sum of all characters in an embed must not exceed 6000 characters.
- Do not put values in the JSON "timestamp": field if you don't know the correct format for them. The correct format is ISO 8601: `yyyy-mm-ddTHH:MM:SS.000Z`.


## Editing an Embed

Editing complex embeds can be daunting to users unfamiliar with JSON. Follow these steps:

1. Use the `embedsource` command to obtain your embed's content and layout. Copy the JSON Carl-bot outputs.
2. Paste the JSON into the embed builder on the [Dashboard](https://carl.gg) (on the top-right where it says **Raw JSON**) then click **Apply**.
3. Make your edits in the embed builder.
4. Click the **Copy to clipboard** button on the right side of the builder to copy the JSON for your edited embed.
5. If the JSON is longer than what Discord allows you to put into the text box, paste the raw JSON into a site like [Pastebin](https://pastebin.com) or [Starbin](https://starb.in).
6. Use the `ecembed` command to update your embed by using the JSON, or Pastebin/Starb.in link.