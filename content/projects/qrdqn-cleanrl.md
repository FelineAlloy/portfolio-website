---
title: "QR-DQN for CleanRL"
summary: "Single-file Quantile Regression DQN implementations for CleanRL, covering classic control and Atari."
date: 2026-05-15
tags: ["PyTorch", "Deep RL", "CleanRL"]
links:
  - name: Code
    url: https://github.com/FelineAlloy/cleanrl/tree/add-qrdqn
  - name: CleanRL
    url: https://github.com/vwxyzjn/cleanrl
---
[CleanRL](https://github.com/vwxyzjn/cleanrl) provides single-file, research-friendly implementations of deep RL algorithms, but it has no QR-DQN. This project adds one, following the library's conventions of one self-contained file per algorithm variant.

QR-DQN (Dabney et al., 2018) replaces DQN's single expected return with a fixed set of quantiles of the return distribution, trained with quantile regression.

> TODO: a short personal note, e.g. why this algorithm

## What's included

The work lives on the `add-qrdqn` branch of my fork:

- `cleanrl/qrdqn.py`: classic control environments
- `cleanrl/qrdqn_atari.py`: Atari, with a convolutional network
- `cleanrl_utils/evals/qrdqn_eval.py`, plus registry entries in `cleanrl_utils/evals/__init__.py`: model evaluation
- Tests for both variants and their evaluation, added to the existing classic control and Atari test files

## Results

TODO: learning curves or benchmark numbers, and how they compare with DQN and C51.

## Status

TODO: not yet merged upstream. Add whether a pull request to CleanRL is planned.
