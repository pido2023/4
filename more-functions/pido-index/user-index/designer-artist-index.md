# Designer/Artist Index

## **Variable Naming**

* $$h$$: Total turnover of the designer/artist
* $$l$$: Total number of limited design/art items listed by the designer/artist
* $$n$$: Total number of bids on the designer/artist's items
* $$m$$: Total number of transactions of the designer/artist's items
* $$N'$$: Total amount of PIT staked by the designer/artist

## **Designer/Artist Influence Index Formula**

The influence index $$g_1(h, l, n, m, N')$$ for each designer/artist is defined as:

$$
g_1(h, l, n, m, N') = L_1 h^{v_1} l^{v_2} n^{v_3} m^{v_4} \ln(N') = Y_1
$$

Where:

* $$v_1, v_2, v_3, v_4, L_1$$ are fixed constants.
* $$Y_1$$ is the value of the designer/artist influence index calculated using the above formula.

## **Average Influence Index and Designer/Artist Index**

* Calculate the influence index $$Y_1$$ for all designers/artists and find their average value $$\bar Y_1$$.
* The Designer/Artist Index $$J_D$$ for an designer/artist is calculated as follows:

$$
J_D = \frac{100}{1 + e^{-\alpha_3 (Y_1 - \bar Y_1)}}
$$

Where:

* $$\alpha_3=0.09$$ is a fixed constant used to adjust the sensitivity of the Designer/Artist Index.
* $$J_D$$ increases with the growth of $$h, l, n, m, N'$$.
* When $$Y_1 = \bar Y_1$$, i.e., when the designer/artist's influence index equals the average influence index of all designers/artists, $$J_D = 50$$.
