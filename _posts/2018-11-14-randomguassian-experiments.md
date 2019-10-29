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
  <figcaption>Source: <a href="https://imgur.com/a/RXJxFtO">https://imgur.com/a/RXJxFtO</a></figcaption>
</figure>

I thought that it would be an interesting challenge. I quickly put together a small sketch to recreate this effect and wanted to document my thought process. I’m very certain that this can be done in many different ways, but here is my approach and solution. But before we get into explanations I wanted to share my end result, which is fairly close to the image above.

<figure>
    <img src="{{ site.baseurl }}/assets/images/randomguassian-fig2.png" alt="Figure 2. End result">
</figure>

I wrote my sketch in JavaScript using P5.js, but it can easily be converted into Java for Processing. There is a great primer on how Gaussian distribution works by [Daniel Shiffman](https://shiffman.net/). If you haven’t seen his Coding Train videos I highly recommend it.

{% include video id="8uyR-YU_0dg" provider="youtube" %}

* * *

Here is my thought process and approach. For the sake of easier calculations I’m going to use 1000x1000px canvas.

*Step 1*: Let’s start with placing an imaginary rectangle on our canvas and adding random pixels to it.

<figure>
    <img src="{{ site.baseurl }}/assets/images/randomguassian-fig3.png" alt="Figure 3.">
</figure>

From the drawing above we can see that we our randomly placed points need to be placed between *300px* and *700px* on *X* axis and *200px* and *800px* on *Y* axis. We can translate that into code that looks something like this:

~~~javascript
function setup() {
  createCanvas(1000, 1000);
  background(10);
}
function draw() {
  stroke(245);
  var xloc = random(300, 700);
  var yloc = random(200, 800);
  point(xloc, yloc);
}
~~~

and after running this for some time we should see something similar to the image below:

<figure>
    <img src="{{ site.baseurl }}/assets/images/randomguassian-fig4.png" alt="Figure 4.">
    <figcaption>Step 1 is done. We have randomly located points constrained in a rectangle.</figcaption>
</figure>