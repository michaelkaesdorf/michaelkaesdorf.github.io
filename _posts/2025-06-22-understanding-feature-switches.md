---
layout: post
title:  "Understanding The feature switches attribute model in .NET 9"
tags: [".NET 9", "feature switches", ".NET Runtime"]
---

In this blog post we will take a look at a new feature in the .NET Runtime that shipped with .NET 9: [Attribute model for feature switches with trimming support](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-9/runtime#attribute-model-for-feature-switches-with-trimming-support).

The idea behind this feature is so help specify parts of the .NET Framework to be _disabled_ for publishing, hence giving control to the author in order to strip off undesired features from the resulting artifact. This process is called _trimming_. Trimming removes unused code for smaller builds. And why should you want to do that? In order to save size. So, I thought: woah, that's pretty much code and configuration that you need to write in order to save some size. It feels absolutely overkill to do that in my huge enterprise application. 
## What's the big benefit?
Well, this feature obviously aims at other use cases. Use cases where size matters. This does not target traditional desktop environments, where all the users have a very high bandwith. This feature targets environments where size and/or bandwith is scarce. So, this is becoming largely more relevant in the world of mobile/handheld computing.
## Relevance to AOT
Another topic where that is relevant is with AOT compilation. Why? Because in JIT compilation, we do not care so much for carrying around "dead" code. As, if unused, it will not be loaded anyway. So, AOT on the other hand, at runtime, will not be able to "decide" what will be needed or not. That in fact is exactly the difference between JIT and AOT.

## Further Reading
[Trim self-contained applications | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/core/deploying/trimming/trim-self-contained)