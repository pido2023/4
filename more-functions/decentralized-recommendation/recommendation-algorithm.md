# Recommendation Algorithm

Define the following:

* $$V_i(t)$$: Effective votes received by work $$i$$ at time $$t$$.
* $$T$$: Current time.
* $$\lambda$$: Time decay rate, where $$0 < \lambda < 1$$.
* $$S_i(T)$$: Total score for work $$i$$ at the current time $$T$$.
* $${N_i}'$$: The number of PITs staked by each user.
* $$W_i$$: Initial recommendation weight for work $$i$$.
* $$R_i(T)$$: Comprehensive recommendation value for work $$i$$ at the current time $$T$$.

Calculate $$V_i$$ for each work $$i$$ based on the votes received that day using the formula

$$
V_i=m = l^{0.5}({N_i}' + 1)^{r_7}
$$

Users spend $$l$$ PIC tokens in a single work for voting. For the parameter $$r_7$$, it defines the influence of staked PIT on the voting power. A value closer to 0 reduces the impact of staked PIT, making the system more democratic, whereas a value closer to 1 increases the influence of users with more staked PIT, which could incentivize staking but might also centralize voting power.

The total score $$S_i(T)$$ for work $$i$$ at the current time $$T$$ can be calculated by summing all the effective votes it received at each time $$t$$, discounted by the time decay factor. This can be represented as:

$$
S_i(T) = \lambda^{T-t}\sum_{t=0}^{T} V_i(t)
$$

The parameter $$\lambda$$ will be chosen carefully to balance recency and popularity. A higher $$\lambda$$ (closer to 1) means that older votes retain their value longer, favoring works with sustained popularity over time. A lower $$\lambda$$ puts more emphasis on recent votes, thus favoring newer works.

If we want to simplify the calculation and consider the votes received each day, we can discretize the time variable and update the score daily:

$$
S_i(T+1) = \lambda S_i(T)+ V_i(T+1)
$$

This formula states that the score for the next day is the decayed previous score plus the new effective votes received on that day.

We denote this initial recommendation weight as $$W_i$$, where $$i$$ represents the user.

$$
W_i=\ln({N_i}'+1)
$$

Here, $$N_i$$ represents the staked token amount of user $$i$$. We add 1 to the staked amount so that even if the user hasn't staked any tokens $${N_i}' = 0$$, they can still get a basic initial weight of $$\ln1 = 0$$.

Then, we can combine this initial weight with the previous time-decayed total vote value to obtain a comprehensive recommendation value $$R_i$$.

$$
R_i(T)=\alpha S_i(T)+(1−\alpha)W_i
$$

Here, $$\alpha$$ is a balancing factor used to adjust the relative importance of the time-decayed total vote value $$S_i(T)$$ and the initial recommendation weight $$W_i$$. The value of $$\alpha$$ can be adjusted according to actual situations. We will set it to 0.8 initially, indicating more emphasis on the voting situation of the work itself.

Finally, we can sort and recommend new works based on this comprehensive recommendation value $$R_i$$.
