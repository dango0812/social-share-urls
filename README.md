# Social Share Urls

This project is intended to help you integrate sharing on social media within web environment.

It provides a collection of **social media share URLs** and corresponding **icons** (`.png`, `.jpg`, `.svg`) to easily implement share functionality across popular platforms.

Why install a full library when you only need to support two share services?

You don’t need a massive library just to add simple social sharing!

Keep it light skip the heavy libraries and just use simple share URLs.

## 📱 Supported Social Networks

| Platform           | Share URL                                                                                                                                         | Details                           | Icons                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|----------------------------------|
| Threads            | https://threads.net/intent/post?url={url}&title={title}                                                                                           | [Link](./details/Threads.md)      | [Icon](./icons/Threads.md)      |
| Twitter (X)        | https://twitter.com/intent/tweet?url={url}&text={text}                                                                                            | [Link](./details/Twitter.md)      | [Icon](./icons/Twitter.md)      |
| Reddit             | https://www.reddit.com/submit?url={url}&type={type}&title={title}                                                                                 | [Link](./details/Reddit.md)       | [Icon](./icons/Reddit.md)       |
| Facebook           | https://www.facebook.com/sharer.php?u={url}                                                                                                       | [Link](./details/Facebook.md)     | [Icon](./icons/Facebook.md)     |
| Facebook Messenger | https://www.facebook.com/dialog/send?link={url}&redirect_url={url}&app_id={appId}&to={to}                                                         | [Link](./details/Messenger.md)    | [Icon](./icons/Messenger.md)    |
| Telegram           | https://t.me/share?url={url}                                                                                                                      | [Link](./details/Telegram.md)     | [Icon](./icons/Telegram.md)     |
| WhatsApp           | https://api.whatsapp.com/send?text={text}                                                                                                         | [Link](./details/WhatsApp.md)     | [Icon](./icons/WhatsApp.md)     |
| Tumblr             | https://www.tumblr.com/share/link                                                                                                                 | [Link](./details/Tumblr.md)       | [Icon](./icons/Tumblr.md)       |
| LinkedIn           | https://www.linkedin.com/feed?shareActive={shareActive}&text={text}                                                                               | [Link](./details/LinkedIn.md)     | [Icon](./icons/LinkedIn.md)     |
| VK (ВКонтакте)     | https://vk.com/share.php?url={url}&title={title}&image={image}&noParse={noParse}&noVkLinks={noVkLinks}                                            | [Link](./details/VK.md)           | [Icon](./icons/VK.md)           |
| Pinterest          | https://pinterest.com/pin/create/button/?url={url}&media={image}&description={description}<br>⚠️ video is only available to business account and has a capacity limit. | [Link](./details/Pinterest.md)    | [Icon](./icons/Pinterest.md)    |
| Instapaper         | http://www.instapaper.com/hello2?url={url}&title={title}&description={description}                                                                | [Link](./details/Instapaper.md)   | [Icon](./icons/Instapaper.md)   |
| Email              | mailto:?subject={subject}&body={body}                                                                                                             | [Link](./details/Email.md)        | [Icon](./icons/Email.md)        |
| Instagram          | ❌                                                                                                                                                |                                   |                                  |
| TikTok             | ❌                                                                                                                                                |                                   |                                  |
| YouTube            | ❌                                                                                                                                                |                                   |                                  |

## ✍️ How to use

### Embed example
```
const searchParams = new URLSearchParams({
    url: "https://github.com/dango0812", // share url
    text: "hello, world"
});
const shareUrl = `https://twitter.com/intent/tweet?${searchParams.toString()}`;

<a href={shareUrl} target="_blank" rel="noopener noreferrer">
    twitter share!
</a>
```
### Using a function example
```
const handleTwitterShare = () => {
    const searchParams = new URLSearchParams({
        url: "https://github.com/dango0812", // share url
        text: "hello, world"
    });
    const shareUrl = `https://twitter.com/intent/tweet?${searchParams.toString()}`;

    window.open(shareUrl, "_blank", "width=800,height=640,noopenner,noreferrer");
};

<button onClick={handleTwitterShare}>
    twitter share!
</button>
```

[![Hits](https://hits.sh/github.com/dango0812/social-share-urls.svg?label=thanks%20for%20visiting)](https://hits.sh/github.com/dango0812/social-share-urls/)
