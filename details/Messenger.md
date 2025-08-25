# Facebook Messenger

* *Official Source :*
    * [Send Dialog](https://developers.facebook.com/docs/sharing/reference/send-dialog/)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Description
With the Send Dialog people can privately send content to specific friends. They'll have the option to privately share a link as a Facebook message. The Send Dialog does not require any extended permissions.  
Facebook messages are a channel for person-to-person communication, and not meant for apps to send messages, or encourage people to spam their friends. In general, games on Facebook.com should use requests to communicate in-game status such as its your turn, or inviting people to use an app, or sending messages to multiple people.

You should offer the Send Dialog in situations when someone would otherwise send an email.

## URL Format
The URL format is `https://www.facebook.com/dialog/send`

## Supported Parameters

| Name     | Description |
|---------------|-------------|
| `app_id`      | Your app's unique identifier. Required. |
| `redirect_uri`| The URL to redirect to after a person clicks a button on the dialog. Required when using URL redirection. |
| `display`     | Determines how the dialog is rendered. In nearly all cases, you won't need to specify this and the default will work best.<br><br>If you use the URL redirect dialog, then this will be a full page display, shown in Facebook.com. This display type is called **page**.<br>If you are using the Facebook SDK for JavaScript, this will default to a modal iframe type for people logged into your app or async when using within a game on Facebook.com, and a popup window for everyone else. |
| `to`          | A user ID of a recipient. Once the dialog comes up, the sender can specify additional people as recipients. |
| `link`        | Required parameter. The URL that is being sent in the message. |


## Examples

```
http://www.facebook.com/dialog/send?
app_id=123456789
&amp;link=http://www.nytimes.com/interactive/2015/04/15/travel/europe-favorite-streets.html
&amp;redirect_uri=https://www.domain.com/
```