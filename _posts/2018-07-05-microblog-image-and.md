---
layout: post
title: "Micro.blog Image and Podcast Posting with Workflow and Drafts"
microblog: false
audio: 
date: 2018-07-05 13:44:43 -0500
guid: http://craigmcclellan.micro.blog/2018/07/05/microblog-image-and.html
---

While I use this site primarily for microposts, I host my blog and podcast, [@theclassnerd](https://micro.blog/theclassnerd), here on Micro.blog as well. There I post longer form content that includes multiple images which has never been easy with Micro.blog hosted sites, especially as an iOS only user.

I've finally put together something I've wanted to do for a long time, a combination of Drafts actions and workflows to upload images and mp3s to Micro.blog using the micropub API. The Drafts actions then insert the markdown for the image or html for the audio into my Draft right where the cursor is.

I've been posting everything I possibly can from Drafts since the Drafts 5 beta launched. Now, I really can do all of my posting there.

Special thanks to [@manton](https://micro.blog/manton) for adapting Micro.blog's implementation of the micropub API so that the URLs don't just come back through the response header (which Workflow can't see), but also in JSON so I can extract it.

You can get all of my actions and workflows here:

- [Image Drafts Action](https://actions.getdrafts.com/a/1Lz)
- [Image Workflow](https://workflow.is/workflows/e98fd23db7e34aa79f992830ae34e3cb)
- [Podcast Drafts Action](https://actions.getdrafts.com/a/1MA)
- [Podcast Workflow](https://workflow.is/workflows/2d1cb55f150440fc8879b60078c1ba72)

Note: To run the workflows, you will need an app token from your Micro.blog account.

