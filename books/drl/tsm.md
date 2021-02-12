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

**k-armed bandit problem:** Consider a problem in which you are asked to make a repeated choice among _k-different_ options, or actions. Each choice yields a numerical reward chosen from a **stationary probability distribution** depending on the action selected. The goal is to maximize the expected total reward over same time period $$t=T$$.

In the _k-armed bandit problem_, each of the _k_ actions has an expected \(mean\) reward given that the action is selected, and let's call it the _value_ of that action. Notice, if we knew the _value_ of each action, then the trivial solution is to select the action with highest value repeatedly. However, we often do **not** know the action values with certainty but have may have estimates. Now, let us introduce some notation related to the above mentioned problem:

$$A_t := \text{Action selected on time step } t $$

$$R_t := \text{Corresponding reward on time step t to action } A_t$$ 

$$q{*}(a) := \mathbb{E}[R_t | A_t = a] := \text{ Expected reward given that } a \text{ is selected}$$

$$Q_t(a) := \text{The estimated value of an action } a \text{ at time step } t$$ 

If we have the estimates of the action values, then at each time step there is at least one action whose estimated value is greatest, called the **greedy** action. When we select one of these actions, it is called **exploiting** our current knowledge of the values of the actions. If we select one of the _non-greedy_ actions, then it is called _**exploring**_ as it enables us to improve our estimate of the non-greedy action's value. Exploiting is the right strategy to maximize the expected reward on the one step, however  exploration may produce greater total reward in _the long run,_ even though it will be lower in the short run. Since it is not possible to both to _explore_ and to _exploit_ with a single action selection, one often refers to the **conflict** between exploration and exploitation.

In this chapter several simple balancing methods for the k-armed bandit will be presented to show that they work much better than methods that always _exploit_. The need to balance exploration and exploitation is the main challenge in reinforcement learning.

### 1.1 Action-value Methods

\*\*\*\*

## 2. Finite Markov Decision Processes

## 3. Dynamic Programming

## 4. Monte Carlo Methods

## 5. Temporal-Difference Learning

## 6. n-step Bootstrapping

## 7. Planning and Learning with Tabular Methods



