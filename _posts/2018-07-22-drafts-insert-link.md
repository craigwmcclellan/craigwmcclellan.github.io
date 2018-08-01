---
layout: post
title: "Drafts Insert Link from Safari View Controller Action"
microblog: false
audio: 
date: 2018-07-22 12:33:30 -0500
guid: http://craigmcclellan.micro.blog/2018/07/22/drafts-insert-link.html
---

One of my favorite features of [Editorial](https://itunes.apple.com/us/app/id673907758?at=1l3vwJx&ct=microblog) when I used it was the ability to open its internal web browser, find a website, and insert a link into the editor. This saved me so much time, and I wanted to recreate it in Drafts. This feature wasn't possible in the exact same way, but I managed to make something that works well for me.

You can get the script from the [Drafts Action Directory](https://actions.getdrafts.com/a/1My).

There's a lot happening in it, but essentially when you run the action, you will be prompted to select a website you want to search and the term you want to search for. Drafts will then use DuckDuckGo's URL parameters to search for the term you entered on the website you select. This is really handy if you have particular websites you like to reference. For instance, here I often link back to other posts I've written here.

To customize this, you just have to change what websites are entered in the sites object at the top. Replace the sites I have in there (like my own) with yours or another. Put the title to the left of the : (this is what will be displayed in the prompt) and the url (sans [www.](http://www.)) to the right. If you're not sure what any of that means, look at the script comments, and they should show you what to do.

I have also created on selection box that will search DuckDuckGo on the whole and one where you can enter a URL you haven't already programmed in.

The final thing to notice is toward the bottom of the script.

Once I find the site or article I want to link to, I tap where the URL bar would be in normal Safari and hold. This will present you with a dialog to copy the URL to your clipboard.

```javascript
var mdLink = Action.find("Markdown Link");
app.queueAction(mdLink, draft);
```

The little bit of JavaScript queues up the [Markdown Link action](https://actions.getdrafts.com/a/1J2) which will turn the selected text in the Drafts editor into a Markdown link using a URL in your clipboard. These two actions tie together really well and make creating links to other articles super easy.

As someone who creates links in show notes and blog posts all the time, this is going to save me a ton of time, and I hope it does for you as well.
