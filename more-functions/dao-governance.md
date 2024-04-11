# DAO Governance

Pido ecosystem community governance mechanism allows various user groups, including designers, artists, buyers, and consumers, to participate in the platform's decision-making process.

## Community Categories

* **PidoDAO**: Serving as the core of platform governance, PidoDAO focuses on platform development strategies, such as copyright procurement and major signings.
* **Designer/Artist DAO**: Established specifically for designers/artists issuing NFTs, it fosters collaboration and exchange among designers/artists.
* **Buyer DAO**: A governance organization for the buyer community, aimed at representing the interests of buyers and participating in related topic discussions.
* **Consumer DAO**: A governance organization composed of consumers, reflecting the voices and needs of consumers.
* **Project DAO**: For users holding specific NFTs, allowing them to vote and discuss the development direction of the related NFT projects.

## Selection Methods

1. PidoDAO consists of all community members.
2. DAO managers are elected by the votes of project users, with the top 10 by vote count becoming managers.
3. The voting rate must exceed 30%; otherwise, a re-vote is required.
4. DAO managers have a term of six months, and consecutive terms must not exceed one year.
5. All community members can serve as candidates or voters; candidates must submit an application.
6. Voting consumes PIC tokens, with the amount expended being $$\frac{1}{2}L(L+1)$$ PICs for $$L$$ votes.
7. The total number of PITs held and staked by a user is $$N$$ tokens.
8. The actual number of votes a user has is $$M=L(N+1)^{r_8}$$, where $$r_8$$ is a weight parameter ($$0<r_8<1$$).
9. Successful voting can earn PIT rewards, as detailed in

{% content-ref url="../pido-token-mechanism/pit/how-to-earn-pit/pit-or-vote-to-earn.md" %}
[pit-or-vote-to-earn.md](../pido-token-mechanism/pit/how-to-earn-pit/pit-or-vote-to-earn.md)
{% endcontent-ref %}

10. Voting uses the user's address; abstentions or splitting votes among multiple candidates are allowed.
11. The voting organizer is the current DAO manager.
12. DAO managers can resign voluntarily, with the next highest vote-getter taking their place.

## Management Methods

1. DAO managers have equal power among themselves, and discussion weight is not affected by the number of votes or the quantity of PIT held.
2. A manager's proposal requires a vote rate of over 90% for initial decision-making; if the vote rate is insufficient, the proposal is re-voted.
3. A proposal must receive over 60% approval to pass; voting options include approval, disapproval, or abstention.
4. Proposals passed by managers must be publicized and decided by a second vote from all users.
5. DAO managers can receive regular PIT or USDT rewards.
6. The Treasury Token pool accounts for 5%, totaling 50 million PIT, to reward managers.
7. PIT replenishment comes from additional issuance and Harberger taxes.
8. DAOs can decide on the use of fiat currency in projects and hire other functional staff.

## Voting Methods

1. DAO managers internally vote to decide on proposals.
2. Proposals affecting the interests of all members require a national vote after manager approval.
3. Voting consumption of PIC is calculated in the same manner as election methods.
4. The actual number of votes for users is calculated as $$L(N+1)^{r_8}$$, where $$r_8$$ is a weight parameter.
5. Voting can be split, abstained, and is carried out using the user's address.
6. For binary proposals, a 30% voting rate and 60% approval pass the proposal; for preferential proposals, the same applies, and if 60% is not reached, the votes are halved and re-voted.
7. Successful voting can earn PIT rewards, as detailed in

{% content-ref url="../pido-token-mechanism/pit/how-to-earn-pit/pit-or-vote-to-earn.md" %}
[pit-or-vote-to-earn.md](../pido-token-mechanism/pit/how-to-earn-pit/pit-or-vote-to-earn.md)
{% endcontent-ref %}
