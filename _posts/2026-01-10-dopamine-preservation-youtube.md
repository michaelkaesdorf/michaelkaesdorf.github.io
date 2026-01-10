---
layout: post
title:  "Dopamine-preserving Browsing"
tags: dopamine
---

In this post I want to show the way I have found in order to make the whole experience on the internet a little bit "safer" in terms to our dopamine reservoir. 
What this post shows is how you can disable videos in the instagram feed as well as make youtube really only be a video-playing platform; removing suggestions and comments.

First an foremost we need to use the brave browser and/or any adblock extension that works with adblock/uBlock origin syntax.
Visit to the filter settings; you can do that via this url: [brave://settings/shields/filters](brave://settings/shields/filters).
There you can paste this [url to my dopamine-preserving-filter-list](https://raw.githubusercontent.com/michaelkaesdorf/dopamine-preserving-browsing/refs/heads/main/dopamine-preservation-filters.txt) as a custom filter list:
![Adding a custom filters list in the Brave browser](/assets/2026-01-10/custom_filters_list.png)


Or you set your filters manually:
Then, we will set a custom html filter. You can do that  and scrolling down to the custom filters section:
![The custom filters section in the Brave browser](/assets/2026-01-10/custom_filters.png)

There you can paste the following:

```
youtube.com##div#dismissible
youtube.com##div#contents
youtube.com##ytd-reel-shelf-renderer
youtube.com##ytd-watch-next-secondary-results-renderer
youtube.com##div.ytp-fullscreen-grid-stills-container
```

Enjoy!