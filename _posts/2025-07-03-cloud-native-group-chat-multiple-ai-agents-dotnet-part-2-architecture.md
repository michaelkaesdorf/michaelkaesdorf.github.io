---
layout: post
title:  "Cloud-native group chat with multiple AI Agents in .NET - Part 2: Architecture"
tags: [".NET AI Template", "AI Agents"]
---

This post is part two in the series "Cloud-native group chat with multiple AI Agents in .NET".
We already set up the .NET AI Template project. So now we will take a step back and think about what we want to build, and how we will go on about it.

## Approach 1: One Stream per Agent

One way that I can think about is that we have one chat stream per agent:

![A diagram depicting the one stream per agent approach: four boxes with the label "Agent". Each box contains another box with the label "Chat Stream"](/assets/2025-07-03/one_stream_per_agent_architecture.png)

This which gives us the following pros:
* model flexibility per agent (e.g. cheaper models for simpler roles)
* A closer resemblance to the reality of a group chat
* true agend independence
* non-overlapping characteristics
The following cons
* This could get more pricy in the end
* We could loose some context between the agents
* We need to coordinate them

## Approach 2: One Stream for all Agents

On the other side of the spectrum, I have this idea: we can just keep one single connection to the llm and inside of that stream we prompt the llm to think "as if" it would be different people:

![A diagram depicting the one stream for all agents approach: one box with the label "Chat Stream: GPT-4o". The box contains four boxes. Each of these boxes is labeled "Agent".](/assets/2025-07-03/one_stream_for_all_agents.png)

The advantages here are:
* saving resources
* sharing the context

Disadvantages:
* more unnatural
* more sophisticated prompts necessary
* the silhouettes of the characters could weaken over time
* no flexibility

## Deciding for Approach 1

So... I am coming to the conclusion that approach 1 is better. Working around the disadvantaged of approach 2 still required quite some work, and it feels a bit dirty. I don't think there's so much interesting to learn among that road. Furthermore, regarding approach 1: I really like thinking about how to create a more sophisticated, hybrid approach. What I am thinking about, is some form intermediate agent that handles the coordination. This coordinator agent could device which specialst agent(s) should respond and only activate relevant agents based on message content. And so many more things.

### Starting Slowly

So, I think a good first milestone would be to have another random joining the room and display this properly to the user.
For this we will need to:
* define agent profiles
* implement random agent selection
* diplay agent name in message header

This is what we will cover in the part three of this blog series.