---
layout: post
title:  "My First Weekend With OpenClaw"
tags: openclaw
---

I spent the weekend getting into OpenClaw, and I want to share a few things I learned.

1. The OpenAI Plus subscription will get you quite far
1. Getting the mental model of OpenClaw's inner interaction-model straight is helpful
1. Hermes is the next hot stuff on the block and might be worth looking into
1. Something that I call "workspace-pollution" is real (today's topic)

From all the things, there's a lot to talk about. First, I will talk about "workspace-pollution".

## Workspace Pollution

The nice thing with OpenClaw is that you can tell it to note things down and remember them for future sessions. But I feel sometimes, due to the nature of the LLM, that the notes are being scattered too randomly. They will get picked up by the wrong agent, in the wrong context; they will be taken too literally, or they will be skipped completely. Then, a problem begins: you start asking "Why didn't you do XYZ like I told you? Do it, and note it down for next time." - and the LLM goes off to "note something down" somewhere, and the problem somehow convolutes. The workspace gets cluttered with desperate "rules" that might even reference each other (e.g. "look up TODO.md, and then use a specific SKILL.md, and then...), creating a "chain of context dependency" that grows bigger, gets more and more washed out and - this is the biggest problem - hard to remove. This workspace pollution really can act like some venom, slowly poisoning the agent.
**I really think a best practice would be to make daily snapshots of your agent's workspace (or the whole OpenClaw directory) so that you are able to revert it.** -> This makes me think, it would be a good idea to gather my personal best practices for agentic software engineering.

So yeah, I need to say that I really do not know (yet) how to avoid eventual workspace pollution! 
We will see how it goes

