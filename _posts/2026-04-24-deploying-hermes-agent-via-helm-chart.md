---
layout: post
title:  "Deploying Hermes Agent via Helm Chart"
tags: openclaw, hermes, hermes-agent, nousresearch, helm, helmchart, k8s, k3s, kubernetes
---

![Terminal output of helm tree](/assets/2026-04-24/helm-tree.png)

Now, after some experimentation with Hermes and OpenClaw, I thought the next smart step would be to think about how to deploy it more safely (and flexibly!).
You know what made me think that? The fact that the mental model of Hermes might not align so well with multi-agent thinking. So I thought: why not create a set-up where you can spin up a new Hermes agent quickly? And anyway, there's always something valuable to learn if you dive into kubernetes stuff (at least for me).

So, the current idea is so install `k3s` on my lenovo x230 minimal debian 13 server. Then install `helm` and create our own helmchart. So we simulate more of a production scenario. 

So, we create our own helm chart:

```
helm create hermes-agent
cd hermes-agent
```

And then we directly install it:
```
helm install hermes-test .
```

Verify if it landed:
```
kubectl get pods
```

![Terminal output of installing the helm chart successfully](/assets/2026-04-24/hermes-agent-helm-chart-deploy-successful.png)

Looking good! So let's remove it for now again:

```
helm uninstall hermes-test
```

That's enough for today. What we will do next is to fill the helm chart with life.