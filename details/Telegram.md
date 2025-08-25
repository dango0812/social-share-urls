# Telegram

* *Official Source :*
    * [Sharing Button](https://core.telegram.org/widgets/share)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Description
A Telegram Sharing Button is an easy way to let users forward content from your website or app to their friends, Channels or Saved Messages on Telegram.
When a user presses the button, Telegram asks them to choose a chat, group or channel where your link will be shared. You can also add some text that describes the link – the user will be able to edit it before sending the message.
You are welcome to use the [Telegram Logos](https://telegram.org/press#telegram-logos) in your custom button design.

## URL Format
The URL format is `https://t.me/share`

## Supported Parameters
The post intent flow supports the following query string parameters.

| Name | Description |
|------|-------------|
| `url`  | The URL the user will be sharing. |
| `text` | An optional description that will be included with the link |

Feel free to create your own custom UI for the button. The only thing you need to make it work is to point the user to this URL on click:
`https://t.me/share/url?url={url}&text={text}`
where {url} is the URL the user will be sharing and {text} is an optional description that will be included with the link.
Both values should be [URL-encoded](https://en.wikipedia.org/wiki/Percent-encoding)

## Examples

| Example                      | URL                                                                                                                                                                          |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Only text**                | `https://t.me/share/url?text=Check+out+this+new+feature+on+Telegram%21`                                                                                                      |
| **Only link attachment**     | `https://t.me/share/url?url=https%3A%2F%2Fcore.telegram.org%2Fbots%2Ffeatures%23deep-linking`                                                                                |
| **Text and link attachment** | `https://t.me/share/url?url=https%3A%2F%2Fcore.telegram.org%2Fbots%2Ffeatures%23deep-linking&text=Learn+about+Telegram+Bot+Deep+Linking+Features`                            |
| **Emoji + link**             | `https://t.me/share/url?url=https%3A%2F%2Fwww.openai.com%2F&text=%F0%9F%9A%80+Check+this+out%21`                                                                             |
