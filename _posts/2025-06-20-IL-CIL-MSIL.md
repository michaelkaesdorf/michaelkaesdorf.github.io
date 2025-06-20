---
layout: post
title:  "IL & CIL & MSIL"
---

## Interoperability of .NET
What makes .NET platform-agnostic is the fact that it uses _Intermediate Language_ (IL). The programming languages are getting compiled into IL. Downstream, all the steps are exactly the same, whether it's C# or something else - like F#.
One question that someone might ask you in the future is: okay, but... 
## What's CIL & MSIL then?
So, CIL stands for _Common Intermediate Language_ and MSIL for _Microsoft Intermediate Language_. 

**They all refer to the same thing.**

> Intermediate Language is sometimes also called Common Intermediate Language (CIL). 
Taken from: [Microsoft Learn: What is Manages Code?](https://learn.microsoft.com/en-us/dotnet/standard/managed-code) 

And MSIL - nowadays - is just the same. See the [Stackoverflow question "What is the difference between CIL and MSIL (IL)?"](https://stackoverflow.com/questions/293800/what-is-the-difference-between-cil-and-msil-il) 

## Which term should I use, then?
There's an [ECMA Standard (no. 335)](https://ecma-international.org/publications-and-standards/standards/ecma-335/) for the term CIL. So, it's advisable to stick with that.
