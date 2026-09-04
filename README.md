# CART POLE BALANCING

## AIM
To develop and fine tune the Monte Carlo algorithm to stabilize the Cart Pole.

## PROBLEM STATEMENT
The objective is to stabilize the CartPole system using a Monte Carlo Control algorithm. In the CartPole environment, the agent must control the movement of a cart by selecting one of two possible actions: moving the cart to the left or right. The goal is to keep the pole balanced in an upright position for as many time steps as possible. Since the CartPole state contains continuous values, the state space is discretized into bins and a Q-value table is used to learn the best action for each state. Monte Carlo Control updates the Q-values using the returns obtained from complete episodes. The algorithm is fine-tuned using learning-rate (alpha) and exploration-rate (epsilon) decay to improve the balancing performance.

## MONTE CARLO CONTROL ALGORITHM FOR CART POLE BALANCING
Step 1: Initialize environment
    
Step 2: Discretize state
    
Step 3: Initialize Q-values
    
Step 4: Select action using epsilon-greedy
    
Step 5: Generate trajectory
    
Step 6: Calculate return
    
Step 7: Update Q-values
    
Step 8: Decay alpha and epsilon

Step 9: Repeat episodes

## MONTE CARLO CONTROL FUNCTION
The mc_control() function implements the Monte Carlo Control algorithm for CartPole balancing. It accepts parameters such as the number of bins, discount factor (gamma), learning rate (alpha), exploration rate (epsilon), number of episodes, maximum steps, and an optional pretrained Q-table. If a pretrained Q-table is not supplied, the Q-values are initialized to zero. During every episode, a trajectory is generated using an epsilon-greedy policy. The return is calculated for each state-action pair and the corresponding Q-value is updated. Finally, the learned Q-table, value function and policy are returned.

## OUTPUT:
1. Specify the average number of steps achieved within two minutes when the Monte Carlo (MC) control algorithm is initiated with zero-initialized Q-values..
<img width="1483" height="241" alt="image" src="https://github.com/user-attachments/assets/a84533c6-0cb6-47aa-99a8-7197d0d2b72a" />

3. Mention the average number of steps maintained over a four-minute period when the Monte Carlo (MC) control algorithm is executed with pretrained Q-values.
 <img width="1576" height="393" alt="image" src="https://github.com/user-attachments/assets/88c5c34c-4a9f-4ef7-a691-7792bb6f444d" />


## RESULT:
The Monte Carlo Control algorithm was successfully implemented for CartPole balancing. The average number of balanced steps with zero-initialized Q-values was 88.04 steps, while the use of pretrained Q-values increased the average balanced steps to 134.63 steps. Thus, the pretrained Q-values improved the stabilization performance of the CartPole system.
