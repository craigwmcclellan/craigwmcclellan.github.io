---
title: Microblogging with GitHub Pages from iOS
layout: post
categories: posts
date: 2017-06-09 09:12:41 -0500
---


I've been using Manton Reece's [Micro.blog](http://micro.blog/) platform for the last month to post short content onto craigmcclellan.com and cross post it to Twitter. I do this so I control my own content and don't have to worry about what happens to posts if/when something happens to Twitter.

After looking around, I decided to host my microblog posts on [GitHub Pages](https://pages.github.com) which runs on Jekyll. In order to post content to GitHub from iOS, I'm using the app [Working Copy](https://itunes.apple.com/us/app/working-copy-powerful-git-client/id896694807?mt=8&uo=4&at=1l3vwJx&ct=blog). I have spent the last month or so perfecting the automation of posting. For anyone interested in using micro.blog from iOS, I wanted to share my workflows.

The three apps I use are Working Copy, [Drafts](https://itunes.apple.com/us/app/drafts-quickly-capture-notes-share-anywhere/id905337691?mt=8&uo=4&at=1l3vwJx&ct=blog), and [Workflow](https://itunes.apple.com/us/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=1l3vwJx&ct=blog).

If the microblog post is only text, I will write the post in drafts, then run [this Workflow](https://workflow.is/workflows/8ffea99f7ef34448998a9013578ec7ca) directly from Drafts. When you import the Workflow, it will ask you for the name of the repository, and your Working Copy x-callback key[^1]. There is also a regular expression in this workflow that looks for the HTML of the image and removes it from the YAML front matter for the post excerpt. This will have to be edited to match the file path where images are stored in your repository, but I left mine in the workflow as an example for anyone not comfortable with RegEx. 

For image posts, [I have a second workflow I run from the Photos app](https://workflow.is/workflows/9fbf26780fd5446da638e082656a1ae2). With GitHub pages having a size limit for pages, I want my images to be as small as possible. I adapted a workflow from the Workflow Gallery which sends an image to TinyPNG for quick compression. The updated image is then saved to Working Copy, and the HTML for the image is added to a new Draft where I can add text, then run the first microblog workflow.

Upon import, this Workflow will ask for your TinyPNG API key as well as your Working Copy x-callback key.

With both workflows, there are comments along the way with things you should change to fit your URL, but for those not familiar with Workflow of x-callback, I left them with my original content so you could more easily see what it needs to look like in the end. 

I hope this is helpful for people, especially those who prefer to work on iOS, and encourages the use of [micro.blog](http://micro.blog/).

[^1]:	This is not automatically synced between your devices, but you can manually type in the key from one iOS device to another.