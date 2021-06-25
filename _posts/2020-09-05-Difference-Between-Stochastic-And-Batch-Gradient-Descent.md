---
title: "Difference between Stochastic and Batch Gradient Descent"
last_modified_at: 2020-09-05T17:33:03-06:00

header:
  show_overlay_excerpt: false
  overlay_image: https://miro.medium.com/max/875/1*IVkEh-AVvcbcMUvEGmg3Ig.png

categories:
  - Machine Learning
  - Computer Science
tags:
  - Machine Learning
  - Optimisers
---

Gradient descent is how a neural network tweaks its weights. It can be visualised as a person moving down a hill. This hill is also a graph of weights vs the loss. The ultimate goal is to get as far down the hill as possible in order to minimise the loss for a given set of inputs.

The loss is measure of how bad your neural network is performing. This is why you want to minimise it. So if a neural network was given a picture of a cat and it classifies it as a dog then the loss is 1, the highest it can be. If the neural network correctly predicts the cat then the loss is 0.

The weights axis corresponds to a single weight in the neural network. So for instance if your neural network was just two neurons it would be the line connecting them together. Of course in practise your neural network contains millions of weights but they are ignored in order to visualise the concept better.

The inputs are the data instances going in to your neural network. There is an option of when to calculate the loss when feeding the data into the neural network. It can be done once per data instance (stochastic) or once per mini-batch or once per batch.

The loss function looks different for these different options.

Performing gradient descent per batch basis does not yield the lowest possible minimum. It super imposes a lot of the more nuanced losses which may have corresponded to important features in the dateset.

Whereas stochastic gradient descent is too jagged and has many local minimums where one can get stuck. If you imagine the person going down the hill he would find it very difficult to not get stuck in one of the many dips. It is so jagged because it is based on just a single data instance.
The mini-batch gradient descent is optimum because the loss function gets very low without too much extra jaggedness. Our imaginary friend would be able to reach the bottom of this hill.
