# Final-CSCI-166
Deep Q-Network Implementation for Atari Breakout

DELIVERABLES:

  I chose to work on ALE Breakout-v5 because it’s a really common starting point for deep reinforcement learning with pixel inputs, and I knew it would push me to handle more complicated tasks like processing high-dimensional image data. When I look at my results, the biggest improvement I saw was the mean episodic reward climbing from almost zero to around 3.4 in under 20,000 training steps. To me, that showed the agent was actually learning the basics of the game — like reliably hitting the ball and breaking bricks — which is exactly what I was hoping for.The hardest part was definitely dealing with sparse rewards. Since the agent only gets points when it breaks a block, it’s tough for the model to figure out which actions were helpful. Because of that, I needed a pretty solid setup to handle credit assignment properly.

One of the main things that helped my training stay stable was using Double DQN. Regular DQN can overestimate Q-values and cause the policy to go in the wrong direction, but Double DQN avoids that by using one network to pick the action and another to estimate the value. Once I switched to that approach, the learning curve smoothed out a lot, and the model converged more consistently.

If I keep working on this, I want to try adding Prioritized Experience Replay so the agent learns more from the important experiences. I’m also planning to slow down the epsilon decay so the agent keeps exploring longer. I think both of those changes could help push performance past where it leveled off this time and maybe lead to more advanced strategies.

Random Agent (Early Exploration) Video

https://github.com/user-attachments/assets/dc508fbf-6d8d-4c68-ac56-231113d82c33

Learned Agent (Later Exploitation) Video

https://github.com/user-attachments/assets/1ff9cee8-fca8-4799-b51a-15030b89b92b
