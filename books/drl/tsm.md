---
description: >-
  Core ideas of RL algorithms in their simplest forms - states and action spaces
  small enough - discussed in this part. In these cases methods can often find
  exact solutions, unlike approximate methods.
---

# I. Tabular Solution Methods

## 1. Multi-armed Bandits

The main difference of reinforcement learning from other learning methods is that it uses training information that **evaluates the actions** **taken** rather than **instructs** by giving **correct actions**. This is what creates the need for _active exploration_, for an explicit search for _good behavior_. 

Purely **evaluative feedback** indicates _how good the action taken was_, but not whether it was the best or the worst action possible. Purely **instructive feedback**, on the other hand, indicates the _correct action to take_, _independently of the action_ actually taken. The latter is the basis of **supervised learning**, which includes large parts of pattern classification, artificial neural networks, and system identification.

 In their pure forms, these two kinds of feedback are **quite distinct**: _evaluative feedback_ depends entirely on the action taken, while _instructive feedback_ is independent of the action taken.



## 2. Finite Markov Decision Processes

## 3. Dynamic Programming

## 4. Monte Carlo Methods

## 5. Temporal-Difference Learning

## 6. n-step Bootstrapping

## 7. Planning and Learning with Tabular Methods



