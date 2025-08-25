# WhatsApp

* *Official Source :*
    * [A Share this on whatsapp](https://faq.whatsapp.com/5913398998672934/)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Description
WhatsApp's click to chat feature allows you to begin a chat with someone without having their phone number saved in your phone's address book. As long as you know this person’s phone number and they have an active WhatsApp account, you can create a link that will allow you to start a chat with them. By clicking the link, a chat with the person automatically opens. Click to chat works on both your phone and WhatsApp Web.

💡 The Chat on WhatsApp button is currently only available in English.  
To increase engagement using the Chat on WhatsApp button, follow these best practices:
- Use the button as is. Don't change the button.
- Use the latest version of the button. You can download the button designs here.
- Make sure the button is visible and easy to read.

You can use that Chat on WhatsApp button in many places, such as:
- landing pages on desktop browsers
- contact pages
- mobile apps
- mobile versions of your website
- templates from third-party developers

## URL Format
The URL format is `https://api.whatsapp.com/send` or `https://wa.me/`

## Supported Parameters
The click to chat flow supports the following query string parameters.

| Name       | Description                                                                                                                                                                                        |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| number     | A full phone number in international format (omit zeroes, brackets, or dashes). Used with `https://wa.me/<number>` to directly start a chat with that person. Example: `https://wa.me/1XXXXXXXXXX` |
| text       | A URL-encoded message that will appear pre-filled in the chat input box. Example: `https://wa.me/1XXXXXXXXXX?text=I'm%20interested%20in%20your%20car%20for%20sale`                                 |
| only\_text | You can create a link with just a pre-filled message (without specifying a number). Example: `https://wa.me/?text=I'm%20inquiring%20about%20the%20apartment%20listing`                             |

```
💡 Use https://wa.me/<number> where the <number> is a full phone number in international format. Omit any zeroes, brackets, or dashes when adding the phone number in international format.
Examples:
Use: https://wa.me/1XXXXXXXXXX
Don't use: https://wa.me/+001-(XXX)XXXXXXX
```

## 1️⃣ WhatsApp wa.me examples
| Parameter      | Description                                                             | Example                                                                          |
| -------------- | ----------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **number**     | Full phone number in international format. Opens chat with that person. | `https://wa.me/15551234567`                                                      |
| **text**       | Prefilled message + number.                                             | `https://wa.me/15551234567?text=I'm%20interested%20in%20your%20car%20for%20sale` |
| **only\_text** | Prefilled message only (no number).                                     | `https://wa.me/?text=I'm%20inquiring%20about%20the%20apartment%20listing`        |

## 2️⃣ WhatsApp api.whatsapp.com/send examples
| Parameter      | Description                                                             | Example                                                                                                |
| -------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **number**     | Full phone number in international format. Opens chat with that person. | `https://api.whatsapp.com/send?phone=15551234567`                                                      |
| **text**       | Prefilled message + number.                                             | `https://api.whatsapp.com/send?phone=15551234567&text=I'm%20interested%20in%20your%20car%20for%20sale` |
| **only\_text** | Prefilled message only (no number).                                     | `https://api.whatsapp.com/send?text=I'm%20inquiring%20about%20the%20apartment%20listing`               |
