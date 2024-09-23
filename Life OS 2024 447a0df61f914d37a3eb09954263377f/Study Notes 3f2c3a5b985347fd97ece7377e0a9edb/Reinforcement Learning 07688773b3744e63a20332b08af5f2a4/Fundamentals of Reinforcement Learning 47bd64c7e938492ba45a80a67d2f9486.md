# Fundamentals of Reinforcement Learning

## Module 1

- Learning Objectives
    
    **Lesson 1: The K-Armed Bandit Problem**
    
    - Define reward
    - Understand the temporal nature of the bandit problem
    - Define k-armed bandit
    - Define action-values
    
    **Lesson 2: What to Learn? Estimating Action
    Values**
    
    - Define action-value estimation methods
    - Define exploration and exploitation
    - Select actions greedily using an action-value function
    - Define online learning
    - Understand a simple online sample-average action-value estimation
    method
    - Define the general online update equation
    - Understand why we might use a constant step-size in the case of
    non-stationarity
    
    **Lesson 3: Exploration vs. Exploitation Tradeoff**
    
    - Define epsilon-greedy
    - Compare the short-term benefits of exploitation and the long-term
    benefits of exploration
    - Understand optimistic initial values
    - Describe the benefits of optimistic initial values for early
    exploration
    - Explain the criticisms of optimistic initial values
    - Describe the upper confidence bound action selection method
    - Define optimism in the face of uncertainty
- Weekly Reading: Chapter 2 - 2.7 (Pages 25 - 36)
    
    [https://wpi0-my.sharepoint.com/:b:/g/personal/pbpatel_wpi_edu/Ee2VG6qKFTdGlJH5auSFaV8BYmfeMEIF-YAaHS_yih-lYA?e=KUm0S8](https://wpi0-my.sharepoint.com/:b:/g/personal/pbpatel_wpi_edu/Ee2VG6qKFTdGlJH5auSFaV8BYmfeMEIF-YAaHS_yih-lYA?e=KUm0S8)
    

### Introduction

In reinforcement learning, the agent generates it own training data
by interacting with the world where it learns the consequences of it’s
action by trial and error. It is not supervised and no outside agent
generally tells the agent if it is right or wrong.

### K-Armed Bandits Problem

Imagine a scenario of a doctor that is experimenting 3 different
drugs (A, B and C) for an illness and tries to test it out on patients
by injecting them with this medication. He observers during his initial
results that drug C works well for his patients with negative or
unsatisfactory results for drug A and B.

He can now decide to either stop providing drug A and B which will
stop the study and save patients lives but will remain in question
whether they were actually bad or just the test patients were compatible
with them. Other scenario can be where he can keep on experimenting for
more results but it can result in death or severe condition of the
patients. This scenario is know as K-Armed Bandits Problem.

**Definition**: We have an **agent** who
chooses between **k** *actions* and recieved a
**reward** based on the action it chooses.

In our scenario:

- Agent → Doctor
- k actions → Drugs
- Reward → Treated Patients

### Action-Values

The **value** of an action is the **expected
reward**: when the action is taken

$$
q_{*}(a)\dot{=}\in[R_{t}|A_{t}=a]\> \forall a\in\{1,....,k\}
$$

q*(a) is defined as expection of R_t given we selected action A, for
each possible action 1 → k.

= ∑*rp*(*r*|*a*)*r*

This conditional expectation is defined as sum over all possible
rewards. Inside the sum, we have multiplied the possible reward by the
probability of observing that reward. This could be extended to the
continuous reward case by switching the summation to an integral.

The goal of the agent is to **maximize** the
**expected reward**. If the agent selects the action that
has the highest value, it achieves that goal. This procedure is called
as ***argmax*** or argument which maximizes our
function q star better.

*argmax* *q**(*a*)

Assume in our scenario we measure the blood pressure of the patient.
We calculate the mean of each dataset of patients to measure the q* for
our situation.

### Sample Average Method

Sample average is a method to estimate q* by Total reward for each
action by number of times the action has been selected.

$$
Q_{t}(a)\dot{=}\frac{\sum_{i=1}^{t-1}R_{i}}{t-1}
$$

Where the numerator is the **Sum of rewards when *a*
taken prior to *t***

Where the denominator is the **Number of times *a* taken
prior to *t***

When the action chooses the action which has had the highest q* for
the purpose of having higher surity of achieving results and reducing
the chance of failure. This method increases probability of success but
fails to consider other methods which might yield better results in
particular situation.

**Non-Greedy Action**

The Agent keeps on doing experimentation to improve its dataset while
trying to solve the problem which can help assign better solution to the
particular scenario. But this results in choosing the outcome which
might bot result in positive reward for the scenario at the moment.

### Action Approaches

**Greedy Action**

### **Ways to Update Q_t**

**Incremental Update Rule**

**Decaying Past Rewards**