Title: Deep Reinforcement Learning
Date: 2018-05-13 00:00
Author: ankitrathi
Category: Uncategorized
Tags: Artificial Intelligence, Reinforcement Learning
Slug: deep-reinforcement-learning
Status: published

![Deep Reinforcement Learning](https://cdn-images-1.medium.com/max/800/0*0Nip07piZC-vdSJE.)

While neural networks are responsible for recent breakthroughs in problems like computer vision, machine translation and time series prediction — they can also combine with reinforcement learning algorithms to create something astounding like AlphaGo.

**What is Deep Reinforcement Learning?**

To understand deep reinforcement learning, lets first look at some definitions from Wikipedia:

*Reinforcement learning (RL) is an area of machine learning inspired by behaviourist psychology, concerned with how software agents ought to take actions in an environment so as to maximize some notion of cumulative reward.*

*Deep learning is loosely related to information processing and communication patterns in a biological nervous system, such as neural coding that attempts to define a relationship between various stimuli and associated neuronal responses in the brain.*

*Deep reinforcement learning (DRL) is a machine learning method that extends reinforcement learning approach using deep learning techniques.*

So by above definitions we can infer that the traditional Reinforcement learning aims to solve problems of how agents can learn to take the best actions on the environment to get the maximum cumulative reward over time. A major part of this process is carefully engineering feature representations. The advances in algorithms for Deep learning have brought up a new wave of successful applications in Reinforcement Learning, because it offers the opportunity to efficiently work with high dimensional input data (like images). In this context the trained deep neural network can be seen as a kind of Deep Reinforcement learning approach, where the agent can learn a state abstraction and a policy approximation directly from its input data.

**Why Deep Reinforcement Learning is required?**

In those kinds of situations where you use supervised & unsupervised learning , you already have a pretty good idea of the data you have, what’s going on and how to solve the problem. You’re using machine learning to find interesting patterns in that data to get to a better solution, accelerate the process and get to your solution faster. But what about those situations or problem spaces where you have partial data or no data, where an agent can only learn by trial and error. In these situations reinforcement learning comes handy, domain experts and organizations typically know what they want a system to do, but they want to automate or optimize a specific process. Recent advances in Deep learning area has also fueled in Reinforcement learning as it doesn’t need hand-engineered features any more because of this ability. After appropriate many backpropagations, deep neural network knows which information is important to do the task.

**How to use Deep Reinforcement Learning?**

Reinforcement learning is inspired by behavioral psychology.

Instead of providing the model with ‘correct’ actions, we provide it with rewards and punishments. The model receives information about the current state of the environment (e.g. the computer game screen). It then outputs an action, like a joystick movement. The environment reacts to this action and provides the next state, alongside with any rewards.

The model then learns to find actions that lead to maximum rewards.

*Q-learning intuition:*

Most modern RL algorithms are some adaptation of Q-Learning. A good way to understand Q-learning is to compare it with playing chess.

Q(S,A) = R + γ \* max Q(S’,A’)

The expected future reward Q(S,A) for a given a state S and action A is calculated as the immediate reward R, plus the expected future reward thereafter Q(S’,A’). We assume the next action A’ is optimal.

*As a regression problem:*

When playing a game, we generate lots of experiences. These experiences are our training data. We can frame the problem of estimating Q(S,A) as a regression problem. To solve this, we can use a neural network.

*Training the experiences:*

In training process, batch of experiences is trained on neural net using a loss function, where we calculate how far or near is predicted outcome from actual outcome.

*Building the model:*

In the next step, we build a model that will learn a Q-function for the game.

*Exploration:*

This is the final step of Q-Learning, where agent will choose some random option for exploration, which will not necessarily the best.

**References:**

[What is deep reinforcement learning, and how does it work?](https://www.quora.com/What-is-deep-reinforcement-learning-and-how-does-it-work)

[Welcome to Deep Reinforcement Learning](https://towardsdatascience.com/welcome-to-deep-reinforcement-learning-part-1-dqn-c3cab4d41b6b)

[Deep reinforcement learning: where to start](https://medium.freecodecamp.org/deep-reinforcement-learning-where-to-start-291fb0058c01)

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to connect on* [*Slideshare*](https://www.slideshare.net/ankitrathi)*.*

------------------------------------------------------------------------

*Originally published at* [*https://www.linkedin.com*](https://www.linkedin.com/pulse/deep-reinforcement-learning-ankit-rathi/) *on May 13, 2018.*
