# Facebook

* *Official Source :*
    * [Sharing](https://developers.facebook.com/docs/sharing/)
    * [Sharing workplace](https://developers.facebook.com/docs/workplace/sharing/share-dialog#sharing-to-workplace)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Description
Sharing a post on Facebook using sharer.php involves directing users to Facebook's sharing interface with pre-filled content based on the provided URL. While sharer.php was a common method in the past, it is now recommended to use Facebook's official Share Button plugin or the Facebook Graph API for more robust and feature-rich sharing experiences.

## URL Format
The URL format is `http://www.facebook.com/sharer/sharer.php`

## Supported Parameters
The post intent flow supports the following query string parameters.

| Name      | Description |
|-----------|-------------|
| `u`   | The URL to be shared |

## Examples

```
http://www.facebook.com/sharer/sharer.php?u=https://developers.facebook.com
```