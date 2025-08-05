# Twitter

* *Official Source :*
    * [Web Intents](https://developer.x.com/docs/x-for-websites/tweet-button/guides/web-intent)
    * [Web Intents Overview](https://developer.x.com/docs/x-for-websites/web-intents/overview)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Tweet
A Tweet Web Intent makes it easy for your site visitors to compose and post a Tweet to their audience from a link on your webpage. Sites may configure Tweet text and hashtags, pass a URL, and identify Twitter accounts related to the page.

## URL Format
The URL format is `https://twitter.com/intent/tweet`

## Supported Parameters
The post intent flow supports the following query string parameters.

| Name          | Description                                                                         |
| ------------- | -------------------------------------------------------------------------- |
| text          | Pre-populated UTF-8 and URL-encoded Tweet text. The passed text will appear pre-selected for a Twitter user to delete or edit before posting. The length of your passed Tweet text should not exceed 280 characters when combined with any passed hashtags, via, or url parameters. Passed Tweet text which causes the Tweet to exceed 280 characters in length will require additional editing by a Twitter user before he or she can successfully post. |
| url           | A fully-qualified URL with a HTTP or HTTPS scheme, [URL-encoded.](https://en.wikipedia.org/wiki/Percent-encoding) The provided URL will be shortened by Twitter’s t.co to the number of characters specified by short_url_length.                      |
| hashtags      | Allow easy discovery of Tweets by topic by including a comma-separated list of hashtag values without the preceding # character.                                                 |
| via           | A Twitter username to associate with the Tweet, such as your site’s Twitter account. The provided username will be appended to the end of the Tweet with the text “via @username”. A logged-out Twitter user will be encouraged to sign-in or join Twitter to engage with the via account’s Tweets. The account may be suggested as an account to follow after the user posts a Tweet.                       |
| related       | Suggest additional Twitter usernames related to the Tweet as comma-separated values. Twitter may suggest these accounts to follow after the user posts their Tweet. You may provide a brief description of how the account relates to the Tweet with a URL-encoded comma and text after the username.                            |
| in_reply_to | The Tweet ID of a parent Tweet in a conversation, such as the initial Tweet from your site or author account.                                                        |


## Examples

```
https://twitter.com/intent/tweet?text=Hello%20World&url=https%3A%2F%2Fexample.com%2F&hashtags=nature,sunset&via=twitterdev
```