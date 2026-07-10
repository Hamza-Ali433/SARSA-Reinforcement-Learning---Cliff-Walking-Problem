# SARSA-Reinforcement-Learning---Cliff-Walking-Problem


## Overview

This project implements the **SARSA (State-Action-Reward-State-Action)** reinforcement learning algorithm using Python, NumPy, and Gymnasium. The agent learns an optimal policy by interacting with the **CliffWalking-v1** environment through trial and error.

The objective is to safely navigate from the start state to the goal while avoiding the cliff, which gives a large negative reward.

---

## Environment

**Environment:** CliffWalking-v1 (Gymnasium)

The environment consists of a grid world where:

- The agent starts from the bottom-left corner.
- The goal is located at the bottom-right corner.
- The cells between the start and goal contain a cliff.
- Falling into the cliff results in a large negative reward and resets the agent to the starting position.

---

## Algorithm

SARSA is an **on-policy Temporal Difference (TD) learning algorithm**.

The Q-value is updated using the following equation:

```
Q(S,A) = Q(S,A) + α [ R + γ Q(S',A') − Q(S,A) ]
```

where:

- **S** = Current State
- **A** = Current Action
- **R** = Reward
- **S'** = Next State
- **A'** = Next Action
- **α** = Learning Rate
- **γ** = Discount Factor

Unlike Q-Learning, SARSA updates the Q-table using the action that is actually selected by the current policy.

---

## Features

- SARSA algorithm implementation
- Epsilon-Greedy action selection
- Q-Table learning
- Cliff Walking environment
- Episode-wise training
- Reward tracking
- Episode length tracking
- Environment rendering during training

---

## Technologies Used

- Python
- NumPy
- Gymnasium
- Matplotlib (optional for visualization)

---

## Project Workflow

1. Initialize the environment
2. Create the Q-table
3. Select actions using the epsilon-greedy policy
4. Execute actions in the environment
5. Observe rewards and next states
6. Update the Q-table using the SARSA update rule
7. Repeat for multiple episodes
8. Evaluate the learned policy

---

## Hyperparameters

| Parameter | Description |
|-----------|-------------|
| Learning Rate (α) | Controls how quickly the agent learns |
| Discount Factor (γ) | Determines the importance of future rewards |
| Epsilon (ε) | Probability of selecting a random action |
| Episodes | Number of training iterations |

---

## Sample Output

```
Episode 1

Total Reward = -19
Episode Length = 19
```

The reward and episode length improve as training progresses, indicating that the agent is learning a better policy.

---

## Learning Outcomes

This project demonstrates:

- Reinforcement Learning fundamentals
- Temporal Difference Learning
- SARSA algorithm
- On-policy learning
- Q-table implementation
- Epsilon-Greedy exploration
- Environment interaction using Gymnasium
- Sequential decision making

---

## Future Improvements

Possible extensions include:

- Q-Learning implementation
- Deep Q Network (DQN)
- Double DQN
- Expected SARSA
- Policy Gradient methods
- Performance visualization using reward curves
- Hyperparameter tuning

---

## License

This project is created for educational purposes and to demonstrate the implementation of the SARSA reinforcement learning algorithm using Python and Gymnasium.
