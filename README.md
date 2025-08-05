# Social Share Urls

This project is intended to help you integrate sharing on social media within web environment.

It provides a collection of **social media share URLs** and corresponding **icons** to easily implement share functionality across popular platforms.

Why install a full library when you only need to support two share services?

You don’t need a massive library just to add simple social sharing!

Keep it light skip the heavy libraries and just use simple share URLs.

## 📱 Supported Social Networks

| Platform           | Share URL                                                                            | Details                         | Icons                          |
| ------------------ | ------------------------------------------------------------------------------------ | ------------------------------- | ------------------------------ |
| Threads            | [https://threads.net/intent/post](https://threads.net/intent/post)                   | [Link](./details/Threads.md)    | [Link](./icons/Threads)        |
| Twitter (X)        | [https://twitter.com/intent/tweet](https://twitter.com/intent/tweet)                 | [Link](./details/Twitter.md)    | [Link](./icons/Twitter%28X%29) |
| Reddit             | [https://www.reddit.com/submit](https://www.reddit.com/submit)                       | [Link](./details/Reddit.md)     | [Link](./icons/Reddit)         |
| Facebook           | [https://www.facebook.com/sharer.php](https://www.facebook.com/sharer.php)           | [Link](./details/Facebook.md)   | [Link](./icons/Facebook)       |
| Facebook Messenger | [https://www.facebook.com/dialog/send](https://www.facebook.com/dialog/send)         | [Link](./details/Messenger.md)  | [Link](./icons/Messenger)      |
| Telegram           | [https://t.me/share](https://t.me/share)                                             | [Link](./details/Telegram.md)   | [Link](./icons/Telegram)       |
| WhatsApp           | [https://api.whatsapp.com/send](https://api.whatsapp.com/send)                       | [Link](./details/WhatsApp.md)   | [Link](./icons/WhatsApp)       |
| Tumblr             | [https://www.tumblr.com/share/link](https://www.tumblr.com/share/link)               | [Link](./details/Tumblr.md)     | [Link](./icons/Tumblr)         |
| LinkedIn           | [https://www.linkedin.com/feed](https://www.linkedin.com/feed)                       | [Link](./details/LinkedIn.md)   | [Link](./icons/LinkedIn)       |
| VK (ВКонтакте)     | [https://vk.com/share.php](https://vk.com/share.php)                                 | [Link](./details/VK.md)         | [Link](./icons/VK)             |
| Pinterest          | [https://pinterest.com/pin/create/button/](https://pinterest.com/pin/create/button/) | [Link](./details/Pinterest.md)  | [Link](./icons/Pinterest)      |
| Instapaper         | [http://www.instapaper.com/hello2](http://www.instapaper.com/hello2)                 | [Link](./details/Instapaper.md) | [Link](./icons/Instapaper)     |
| Email              | mailto:                                                                              | [Link](./details/Email.md)      | [Link](./icons/Email)          |
| Instagram          | ❌                                                                                    |                                 |                                |
| TikTok             | ❌                                                                                    |                                 |                                |
| YouTube            | ❌                                                                                    |                                 |                                |

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
