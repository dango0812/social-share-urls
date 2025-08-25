# Tumblr

* *Official Source :*
    * [Share Button Documentation](https://help.tumblr.com/knowledge-base/share-button-documentation/)

* *Test Results :* Functionality tested and verified by SocialShare Dev's in `2025`.

## Overview
This documentation is for developers who want to control how their website content is displayed in Tumblr posts created by a share button widget installed on their page.

To get share buttons for your site, make one with our [share button generator](https://www.tumblr.com/buttons).

### Post content defaults
By default, the share button will create either a Photo Post or a Link Post depending on what Open Graph meta tags it finds on your page, but it can be configured to use whatever post type you want (see instructions below). These are the default options:

Photo Post. The share button will create a Photo Post if it finds an og:image tag with an image at least 500px wide, with an aspect ratio less than 3:1. It’ll use the og:description for the post caption.
Link Post. The share button will create a Link Post if it doesn’t find a suitable image for a Photo Post. og:title will be used for the title, og:description for the caption, and the canonical URL will be used as the link post URL.

## URL Format
The URL format is `http://tumblr.com/widgets/share`

## Supported Parameters
If you want the share button to create a particular type of post, you can do that with the following options. The options can be set as data attributes on the button anchor tag or as query string parameters in the URL in the button’s href attribute.

| Name       | Description                                                                                                                 | Example                                                                                |
| ---------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `posttype` | The Tumblr post type. Valid options are: `text`, `photo`, `link`, `quote`, `chat`, `video`.                                 | `posttype=photo`                                                                       |
| `tags`     | A comma-separated list of tags.                                                                                             | `tags=travel,photography,sunset`                                                       |
| `title`    | Used in **Text**, **Link**, and **Chat** post types as the post title.                                                      | `title=My+First+Post`                                                                  |
| `content`  | The main content of the post. Varies by post type:<br>• Text → post body<br>• Photo → image URL<br>• Quote → the quote text | `content=https%3A%2F%2Fexample.com%2Fimage.jpg` <br>or <br>`content=Life+is+beautiful` |
| `caption`  | Used in **Photo**, **Link**, **Video**, and **Quote** posts as a caption or description.                                    | `caption=Shot+this+amazing+sunset+yesterday`                                           |
| `show-via` | Whether or not to include attribution in the post body that reads “via …”. Typically `true` or `false`.                     | `show-via=true`                                                                        |

## Examples

| Post Type | Example URL |
| --------- | ----------- |
| Text      | `https://www.tumblr.com/share/link?posttype=text&title=My+First+Post&content=This+is+my+very+first+Tumblr+post!&tags=intro,hello` |
| Photo     | `https://www.tumblr.com/share/link?posttype=photo&content=https%3A%2F%2Fexample.com%2Fsunset.jpg&caption=Shot+this+amazing+sunset+yesterday&tags=travel,photography,sunset` |
| Link      | `https://www.tumblr.com/share/link?posttype=link&title=Check+out+this+site&content=https%3A%2F%2Fexample.com&caption=A+cool+website+I+found&tags=web,links` |
| Quote     | `https://www.tumblr.com/share/link?posttype=quote&content=Life+is+what+happens+when+you%27re+busy+making+other+plans.&caption=John+Lennon&tags=quotes,inspiration` |
| Chat      | `https://www.tumblr.com/share/link?posttype=chat&title=Funny+Conversation&content=Me%3A+Hello!%0AFriend%3A+Hey!+How+are+you%3F&tags=chat,funny` |
| Video     | `https://www.tumblr.com/share/link?posttype=video&content=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DdQw4w9WgXcQ&caption=Best+video+ever&tags=music,video` |