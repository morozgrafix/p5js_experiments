---
title: "randomGaussian experiments"
date: 2018-11-14T19:00:00-08:00
categories:
    - blog
tags:
    - p5.js
    - processing
    - tutorial
---

I recently started to play around with [Processing](https://processing.org/) and [P5.js](https://p5js.org/) and while I’m not an expert yet I find I enjoy it very much.

I came across a [Points Distribution dilemma](https://www.reddit.com/r/processing/comments/9wutfp/point_distribution_dilemma/) post on r/processing subreddit where [addictedtobiscuits](https://www.reddit.com/user/addictedtobiscuits) is trying to recreate following [image](https://imgur.com/a/RXJxFtO) with processing.

<figure>
  <img src="{{ site.baseurl }}/assets/images/randomguassian-fig1.png" alt="Figure 1. Source: https://imgur.com/a/RXJxFtO">
  <figcaption>Source: [https://imgur.com/a/RXJxFtO](https://imgur.com/a/RXJxFtO)</figcaption>
</figure>

I thought that it would be an interesting challenge. I quickly put together a small sketch to recreate this effect and wanted to document my thought process. I’m very certain that this can be done in many different ways, but here is my approach and solution. But before we get into explanations I wanted to share my end result, which is fairly close to the image above.

<figure>
    <img src="{{ site.baseurl }}/assets/images/randomguassian-fig1.png" alt="Figure 2. End result">
</figure>
