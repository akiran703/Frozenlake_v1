implemented Q-Learning, a off-value-based algorithm, that uses temporal differences to train the action value function that controls the agent, specifically we trained the agent in navigating the frozen lake environment.




My understanding of Q-Learning

As I mentioned before, Q-learning is an off-policy value based algo that uses TD to train the action value function. Off-policy refers to using two different policies for acting (inference) and updating (training). An example of this would be using epsilon-greedy policy during acting and the greedy policy to select the best next-state action value to update our Q-value (updating policy). Value-based method refers to finding the optimal policy by training an action-value function that will tell us the value of the state-action pair. Temporal difference is the way we update the action-value function by updating at the end of each step. 


The idea behind Q-learning is that all possible actions and states are mapped into a table. The flow of implementing is like the following

1) Initialize the Q-table
2) use epsilon-greedy policy to determine which action we will take
3) perform the action and get the reward and next state
4) update the Q-table Q(action,state) with the following equation Q(A,S)  =  Q(A,S) + alpha * (Rewardt+1  +  gamma * max(Q(A,St+1)) - Q(A,S)


This algo isn't very optimal as with more actions and states, the table will grow thus becoming inefficient. 



