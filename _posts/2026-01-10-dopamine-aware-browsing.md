---
layout: post
title:  "Dopamine-Aware Browsing"
tags: dopamine
---

## Premise

In my life, I find myself often in a situation where I feel some special interest in my relation to media and my habits of consumption of media and my relationship with it. I always think back to "simpler" times when I actually managed and enjoyed to read books. Not only after reading [the book "Dopamine Nation" by Anna Lembke](https://www.annalembke.com/dopamine-nation) I think more than ever that nowadays, excessive engagement in "low-effort but high-dopamine"-activities (e.g. doomscrolling, video games) is the modern variant of "smoking in the seventies".

## The Problem

Living our life with the social media platforms around us, there's little agency that we can excert when it comes to the ways of their usage. The truth is that platforms like instagram are here to stay and while we - of course - could stay away of them completely (and thus "solve" the problem), we might want to look out for a more moderate approach that still enables us to take part in the society; or: where our sub-society of choice plays. And this might be on instagram. Or youtube. Or any other social media. Abstaining from these platforms can and will lead (in my experience) to social isolation. The problem is, that they are less of "neutral platforms" and more of designed environments.

In this post I want to talk about some little tricks that I have found to be very effective in helping me preserve my dopamine-level while browsing the internet.

What this post shows is how you can **disable videos in the instagram feed** as well as make youtube really only be a video-playing platform; removing **suggestions and comments from youtube videos**.

First an foremost we need to use the brave browser and/or any adblock extension that works with adblock/uBlock origin syntax.
Visit to the filter settings; you can do that via this url: [brave://settings/shields/filters](brave://settings/shields/filters).
There you can paste this [url to my dopamine-preserving-filter-list](https://raw.githubusercontent.com/michaelkaesdorf/dopamine-preserving-browsing/refs/heads/main/dopamine-preservation-filters.txt) as a custom filter list:

![Adding a custom filters list in the Brave browser](/assets/2026-01-10/custom_filter_list.png)


Or you set your filters manually:
Then, we will set a custom html filter. You can do that  and scrolling down to the custom filters section:

![The custom filters section in the Brave browser](/assets/2026-01-10/custom_filters.png)

There you can paste the following:

```
instagram.com##article video
youtube.com##div#dismissible
youtube.com##ytd-reel-shelf-renderer
youtube.com##ytd-watch-next-secondary-results-renderer
youtube.com##div.ytp-fullscreen-grid-stills-container
youtube.com##.ytd-comments
```

Enjoy!
