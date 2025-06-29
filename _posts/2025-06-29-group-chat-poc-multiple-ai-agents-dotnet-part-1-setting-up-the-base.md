---
layout: post
title:  "Cloud-native group chat PoC with multiple AI Agents - Part 1 - Setting up the base"
tags: [".NET AI Template", "AI Agents"]
---

In April 2025, the [.NET AI Template](https://devblogs.microsoft.com/dotnet/announcing-dotnet-ai-template-preview2/) went into preview phase two: 

I thought this could be a fantastic possibility to try the idea of a group chat with multiple AI agents.

Let's get started by bootstrapping the template exactly as shipped first.

After installing the template, we walk through the wizard. We create a project called MultiAgentChatPoC with the following configuration:

```bash
dotnet new aichatweb --output MultiAgentChatPoC --provider githubmodels --vector-store local --aspire true
```
Notice that we are adding Aspire Orchestration support. This is what will enable our project to run "cloud-native". It's a good practice to use Aspire.

Now we create a new repo and push our code.

We will be using Github Models along the way. For this, we first need to create a personal access token (PAT) in github. So, after navigating to github and authenticating, we access Settings -> Developer Settings -> Personal Access Tokens -> Fine-grained Tokens. 
Here we limit the scope of the PAT to the freshly created repo that we just created:

![Screenshot of the repository access settings in github](/assets/2025-06-29-group-chat-poc-multiple-ai-agents-dotnet-part-1-setting-up-the-base/pat_repo_access.png)

There, we scroll down and add read-only access to "Models":

![Screenshot of PAT access scope](/assets/2025-06-29-group-chat-poc-multiple-ai-agents-dotnet-part-1-setting-up-the-base/pat_scope.png)

Now we will need to add the PAT to the secrets of the AppHost-project like that:


   ```bash
  cd ModernDotNetShowChat.AppHost
  dotnet user-secrets set ConnectionStrings:openai "Endpoint=https://models.inference.ai.azure.com;Key=YOUR-API-KEY"
   ```

Ok, let's hit start!

![Screenshot of the running app](/assets/2025-06-29-group-chat-poc-multiple-ai-agents-dotnet-part-1-setting-up-the-base/working_app.png)

Great, as we can see, the app starts and we are presented with a chat-like interface. Let's test it by typing something.
And here is a proof that it is working:

![Screenshot of a working prompt](/assets/2025-06-29-group-chat-poc-multiple-ai-agents-dotnet-part-1-setting-up-the-base/successful_prompt.png)

Alright. Now we are set up and ready to go. Here we will end part one. The next step will be to locate the relevant parts in the code and think about how to implement our idea.