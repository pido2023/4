# Regular Dividends

Pido will convert 60% of Pido's net fiat profit into USDT and distribute it as dividends to users who stake PIT on the platform at the end of each quarter.

To execute this dividend strategy fairly, we have developed a transparent and easy-to-understand dividend algorithm. Here, we define $$P$$ as the total profit generated by Pido in a quarter, in US dollars (USD). The number of PITs staked by each user is represented by $$N'$$. Then, the USDT dividend $$D_i$$ for the $$i$$th user can be calculated as follows:

$$
D_i=60\%P\frac{N'^{r}_{i}}{\sum N'^{r}_{i}}
$$

In this formula, $$N'_i$$ is the number of PITs staked by the $$i$$th user, $$r$$ is an exponent used to adjust the weighting of the stakes, and the denominator $$\sum{N'_i}^r$$ is the sum of the $$r$$th power of the number of PITs staked by all users. This weighted dividend mechanism ensures that the dividends match each user's contribution to the platform; the more PITs staked, the more dividends the user receives.

Furthermore, using the $$r$$th power adjusts the concentration of dividends, if $$r<1$$, the dividends will be more evenly distributed among all users. We will set $$r=0.8$$ initially and regularly review then adjust the value of $$r$$ to ensure that the dividend strategy is in line with the platform's development strategy and remains fair to all users.

Through this approach, we hope to create a sustainable ecosystem where user participation is not only recognized but also materially rewarded. We believe this will help build a stronger and more united community, laying a solid foundation for the long-term development of Pido.
