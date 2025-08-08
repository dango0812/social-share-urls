# Reddit

* *Official Source :*
    * [API Submit](https://www.reddit.com/dev/api#POST_api_submit)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Description
can use the submit page with the text parameter (urlencoded).
which sets the displayed tab to the self post tab (although it's not required as that is inferred based off of the text parameter).

## URL Format
The URL format is `https://www.reddit.com/submit`

## Supported Parameters
The post intent flow supports the following query string parameters.

| Name      | Description |
|-----------|-------------|
| `title`   | Title of the post to submit |
| `url`     | URL to submit to |
| `text`    | Text of the self post |
| `selftext`| Whether to default to the self text tab (true to do so). If text is present, then it will default to displaying that tab anyways. |
| `resubmit`| Whether to resubmit the post (if not present and submitting a link post, and another post already links there, you will be taken to that post instead with an option to resubmit it). |

## Examples

| Example                          | URL |
|----------------------------------|-----|
| **Only text**                    | `https://www.reddit.com/submit?text=This+is+a+self+post+example` |
| **Only link attachment**         | `https://www.reddit.com/submit?url=https%3A%2F%2Fwww.example.com` |
| **Text and link attachment**     | `https://www.reddit.com/submit?url=https%3A%2F%2Fwww.example.com&text=Check+out+this+example+link` |
| **Title and text**               | `https://www.reddit.com/submit?title=Example+Post&text=This+is+a+self+post+with+a+title` |
| **Title and link**               | `https://www.reddit.com/submit?title=Example+Post&url=https%3A%2F%2Fwww.example.com` |
| **Selftext true**                | `https://www.reddit.com/submit?selftext=true&text=This+post+will+default+to+selftext+tab` |
| **Resubmit true**                 | `https://www.reddit.com/submit?resubmit=true&url=https%3A%2F%2Fwww.example.com` |