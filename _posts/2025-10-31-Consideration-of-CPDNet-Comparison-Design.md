---
layout: post
author: Zhang Wenyi
tags: [CPDNet, English, Consideration]
---

This is my consideration of the CPDNet comparison experiments design. These experiments will be shown in my master thesis charpter 3.

First, I have to know what algorithm looks like:
- Neural Network based algorithim
- The output of the algorithm is the probability of change point.
- Time sequence problem

Then, we can conclude how current researchers work on change point detection algorithm. Most of the researchs treat the CPD problem as a classification problem, that means they will seperate sequence into two or many sections, different section means different parameters. Below are some method base on this hyphasis:
- Bayesian Online Changepoint Detection <https://arxiv.org/abs/0710.3742v1>
- Support Vector Machine algorithm <https://arxiv.org/abs/1902.06361>
- ... and so on

For now, I don't this such methods can be goood benchmark for my thesis, because there is no doubt that, we actually treat CPD problem in different ways. However, I can change my algorithm to fit above methods, that is setting a threshold. As long as the probability over the threshold, we can set current time step is the moment where change point happend. But can we find a better way? Maybe we should check more algorithms about Neural Network.

There are many papers about NN based change point detection algorithm design, such as:
- A dual-LSTM framework combining change point detection and remaining useful life prediction<https://www.sciencedirect.com/science/article/pii/S0951832020307572>
    - In this paper, authors proposed a dual-LSTEM framework to handle change point problems. But this is only on LSTM will be used to predict change point detection, the other LSTM will use HI to predict RUL. 
    - And just like before algorithms, it just product which time step change point will happen.

**So**, I decide to inpose a threshold in my CPDNet, so it can compare with other aogorithm, and I want to use *BOCD* as the benchmark!