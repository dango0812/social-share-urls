# Threads

* *Official Source :*
    * [Web Intents](https://developers.facebook.com/docs/threads/threads-web-intents)
    * [Brand Resources](https://about.meta.com/brand/resources/instagram/threads/)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Post Intent
Post intents allow people to easily share their favorite content from your website directly to Threads, in order to increase your reach, spark conversations and drive traffic.

## URL Format
The URL format is `https://www.threads.net/intent/post`

## Supported Parameters
The post intent flow supports the following query string parameters.

| Name | Description |
|------|-------------|
| `text` | The text that the post dialog should be prefilled with. |
| `url`  | The URL for an optional link attachment. |

All parameter values should be encoded using [percent-encoding](https://datatracker.ietf.org/doc/html/rfc3986#section-2.1) ("URL encoding") so that the values can safely be passed via the URL.

## Examples

| Example        | URL |
|---------------------|-----|
| **Only text**       | `https://www.threads.net/intent/post?text=Say+more+with+Threads+%E2%80%94+Instagram%27s+new+text+app` |
| **Only link attachment** | `https://www.threads.net/intent/post?url=https%3A%2F%2Fabout.fb.com%2Fnews%2F2023%2F07%2Fintroducing-threads-new-app-text-sharing%2F` |
| **Text and link attachment** | `https://www.threads.net/intent/post?url=https%3A%2F%2Fabout.fb.com%2Fnews%2F2023%2F07%2Fintroducing-threads-new-app-text-sharing%2F&text=Introducing+Threads%3A+A+New+Way+to+Share+With+Text` |