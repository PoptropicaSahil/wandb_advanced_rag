---
slug: /guides/integrations/farama-gymnasium
description: How to integrate W&B with Farama Gymnasium.
displayed_sidebar: default
---

# Farama Gymnasium

If you're using [Farama Gymnasium](https://gymnasium.farama.org/#) we will automatically log videos of your environment generated by `gymnasium.wrappers.Monitor`. Just set the `monitor_gym` keyword argument to [`wandb.init`](../../../ref/python/init.md) to `True`.

Our gymnasium integration is very light. We simply [look at the name of the video file](https://github.com/wandb/wandb/blob/c5fe3d56b155655980611d32ef09df35cd336872/wandb/integration/gym/__init__.py#LL69C67-L69C67) being logged from `gymnasium` and name it after that or fall back to `"videos"` if we don't find a match. If you want more control, you can always just manually [log a video](../../track/log/media.md).

Check out this [report](https://wandb.ai/raph-test/cleanrltest/reports/Mario-Bros-but-with-AI-Gymnasium-and-CleanRL---Vmlldzo0NTcxNTcw) to learn more on how to use Gymnasium with the CleanRL library. 

![](/images/integrations/gymnasium.png)
