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
There's an [ECMA Standard (no. 335)](https://ecma-international.org/publications-and-standards/standards/ecma-335/) for the term CIL. Microsoft lists these definitions in their docs: [.NET-ECMA Standards](https://learn.microsoft.com/en-us/dotnet/fundamentals/standards) So, it's advisable to stick with CIL.

# Related Anki-Cards
### What does _IL_ stand for in the context of the CLR?
IL stands for Intermediate Language.
### What is the Intermediate Language in the context of the CLR and its function?
It describes the platform-agnostic intermediate code that is generated out of the .NET-languages like C# or F#. Later, the compiler uses it to generate the machine code.
### What does CIL stand for in the context of CLR and what's the difference with regards to the IL?
CIL stands for Common Intermediate Language, the official name of the .NET-Standard 
and ECMA specification.
### What's the importance of the term MSIL with regards to the term CIL?
It's the same.
MSIL reflects its original Microsoft-specific naming.
