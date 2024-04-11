# Curator Index

## **Variable Naming**

* $$h$$: Total transaction volume of the curator, including bidding amount, auction transaction amount, and crowdfunding transaction amount
* $$n$$: Total number of design/art items listed by the curator
* $$m$$: Number of listed design/art items by the curator that have generated transactions
* $$N'$$: Total amount of PIT staked by the curator

## **Curator Influence Index Formula**

The influence index $$g_2(h, n, m, N')$$ for each curator is defined as:

$$
g_2(h, n, m, N') = L_2 h^{w_1} n^{w_2} m^{w_3} \ln(N') = Y_2
$$

Where:

* $$w_1, w_2, w_3,L_2$$ are fixed constants.
* $$Y_2$$ is the value of the curator influence index calculated using the above formula.

## **Average Influence Index and Curator Index**

* Calculate the influence index $$Y_2$$ for all curators and find their average value $$\bar Y_2$$.
* The Curator Index $$J_B$$ for a curator is calculated as follows:

$$
J_B = \frac{100}{1 + e^{-\alpha_4 (Y_2 - \bar Y_2)}}
$$

Where:

* $$\alpha_4=0.09$$ is a fixed constant used to adjust the sensitivity of the Curator Index.
* $$J_B$$ increases with the increase of $$h, n, m, N'$$.
* When $$Y_2 = \bar Y_2$$, i.e., when the curator's influence index equals the average influence index of all curators, $$J_B = 50$$.
