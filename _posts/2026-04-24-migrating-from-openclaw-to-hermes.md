---
layout: post
title:  "Migrating from OpenClaw to Hermes"
tags: openclaw, hermes, hermes-agent, nousresearch
---

![An image of the terminal process installing Hermes Agent of Nous Research](/assets/2026-04-24/hermes-install.png)

So after just a few days of experimentation I decided to move from OpenClaw to Hermes.

Trying to stay up to speed with the developments; OpenClaw seems to be what we in Germany call "the snow of yesterday". And I can relate:

*In OpenClaw, the division between Heartbeat and Cronjobs is not necessary, and annoying*

On top, in OpenClaw, there was just way too much stuff to do. Dreaming? I turned on Dreaming - and it seemed just a whole feature to feed into the hyped up narrative of the "sentient bot". You easily get lost in these features.

Things break, the agent misunderstands it; the configuration is cluttered...

I am curious to what this will be. I am not expecting too much of the "self-learning"-thing with Hermes, though.

## Things to take care of / Pitfalls

So, I saw that there is a command to migrate:
```hermes claw migrate```

Knowing this, I went into the install.
But the installer already has some migration capabilities:

![Hermes install process prompting: OpenClaw installation detected](/assets/2026-04-24/openclaw-installation-detected.png)

If you choose yes here, you will get conflicts in the migration process later on. So I advise against it.

So, let's go:

```
# Full migration including API keys, skip confirmation
hermes claw migrate --preset full --yes
```

![Hermes migration finished](/assets/2026-04-24/migration-finished.png)

Well... now we only still need to bring all the agents to hermes. I seem to notice: The Hermes mental model is more focused on one single orchestrator agent; not so much on parallel "main" agents? Hm, that's kind of a bummer. I still need some time to confirm that. For now I will leave it be and return later.
