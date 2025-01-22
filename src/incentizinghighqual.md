# Incentivizing High-Quality Content in Online Recommender Systems

> By Xinyan Hu, Meena Jagadeesan, Michael I. Jordan, and Jacob Steinhardt. Link [here](https://arxiv.org/abs/2306.07479). 

- Standard online algorithms (Hedge, EXP3) incentivize producers to create low-quality content  
    - If a platform's learning update is too slow, producers will put in low effort due to temporal discounting 
- Quality measured in terms of producer effort and user welfare 
- Platform's learning task is modelled using adversarial linear contextual bandits, since the platform is operating in non-stochastic environment (each arm's rewards can vary over time)
- This is a generalized Stackelberg game (platform is leader and each producer is a follower)
- Punishment threshold must be carefully chosen, so that the producer opts for higher production, not the punishment 