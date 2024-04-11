# Pido Lending Mechanism

## **Lending Rules**

1. **Limited NFT Usage Provision**
   * Only limited NFTs issued through an auction can be used for lending purposes.&#x20;
   * Non-limited NFTs issued through crowdfunding are not eligible for lending.
2. **NFT Price Valuation and Taxation**
   * **NFT Holders:** Users must activate the NFTs they wish to use for borrowing and declare their assessed value on the platform.
   * **Harberger Tax:** Holders pay Harberger Tax based on the assessed value, which forms part of the borrowing cost, including taxes and interest in the repayment.
3. **Lending Mechanism**
   * **Loan Application:** Borrowers post loan applications on the platform, selecting the loan amount, interest rate, and loan term.
   * **NFT Freezing:** As collateral for the loan, the borrower's NFT is frozen in a smart contract until the loan is repaid.
4. **Automated Execution**
   * **Smart Contract:** Once the lending relationship is established, the smart contract automatically executes the freezing of the NFT, ensuring it cannot be transferred unless the loan is repaid.
   * **Interest and Principal Repayment:** Borrowers pay periodic interest in PIC and repay the principal PIT at maturity, executed automatically through smart contracts.
5. **Default Handling**
   * **Automatic Liquidation:** If the borrower fails to repay on time, the smart contract automatically executes the liquidation, auctioning the asset at 50% of the assessed value through the platform.
   * **Excess Value Distribution:** If the liquidation value exceeds the total debt, the surplus is returned to the borrower.
6. **Asset Purchase**
   * **Purchase Right:** Anyone can make a purchase request at the asset holder's declared valuation price.
   * **Priority Purchase Right:** Within the repayment period, the borrower has the right of first refusal to purchase the collateralized asset at the assessed value.
7. **Asset Purchase Rules**
   * During the loan period, if a third party is willing to pay a higher price to purchase the asset, a bidding process can be triggered.
   * If the borrower cannot match this new offer, the asset will be forced to sell.
   * Firstly, the asset will be sold to the highest bidder. The sales price of the asset is used to cover the borrower's Harberger Tax on the asset and any other fees associated with the asset.
   * Once the asset is liquidated, the proceeds are first used to repay the principal and interest related to the borrowed funds.
   * If there are funds remaining after the asset is sold, these funds will be returned to the borrower as compensation for their residual equity in the asset.
   * If the income from the sale of the asset is insufficient to cover the debt, the borrower will need to assume the remaining debt.&#x20;

## Interset Rate Calculation

1. **Interest Rate**: Different lending periods will have different interest rates. The specific interest rate structure needs to be further provided.

| Lending Period | Interest Rate |
| -------------- | ------------- |
| 1 week         | $$e_1$$       |
| 2 weeks        | $$e_2$$       |
| 1 month        | $$e_3$$       |
| 2 months       | $$e_4$$       |
| 3 months       | $$e_5$$       |
| 6 months       | $$e_6$$       |
| 1 year         | $$e_7$$       |

The specific numerical value of annual yield rates will be provided subsequently.

2. **PIC Interest:** Users pay PIC as interest on the loan.\
