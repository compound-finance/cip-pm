# CIP-3: Compound V2 to V3 Migration


# Preamble

**CIP**: 3
**Type**: Protocol Enhancement
**Title**: Compound V2 to V3 Migration
**Description**: Community migration plan from V2 to V3
**Author**: Gauntlet
**References**: [Compound V2 -> V3 Migration Planning](https://www.comp.xyz/t/compound-v2-v3-migration-planning/3969)


# Abstract


# Specification and Rationale

Below is Gauntlet’s initial migration proposal for the Compound community. During the migration process, we can adjust the plan in response to changes in TVL, utilization rates, and general market conditions. Note these dates are tentative and subject to delay depending on how governance proceeds. The ~10 day buffer between the end date of one proposal and the start of the following proposal is to allow time to post in the forums, create the proposal, and wait for execution.

|  |  | 2023/02/20-2023/03/06 | 2023/03/17-2023/03/31 | 2023/04/11-2023/04/25 | 2023/05/07 |
| --- | --- | --- | --- | --- | --- |
| Levers |  |  |  |  |  |
|  | USDC Comp distribution migration (v2 → v3) | Transfer 50%  v2 2023/02/13 value to v3, for a total of 241.2 tokens per day. v2 supply and borrow incentives will drop to 120.6 per day. | Transfer 75% (+25%) v2 2023/02/13 value to v3, for a total of 361.8 tokens per day. v2 supply and borrow incentives will drop to 60.3 per day. | Transfer 90% (+15%) v2 2023/02/13 value to v3, for a total of 434.16 tokens per day. v2 supply and borrow incentives will drop to 24.12 per day. | Transfer 100% (+10%) v2 2023/02/13 value to v3, for a total of 484.4 tokens. v2 supply and borrow incentives will drop to 0 per day. |
|  | v2 USDC Reserve Factor (currently 7.5%) | 15% (+7.5%) | 17.5% (+2.5%) | 20% (+2.5%) | 22.5% (+2.5%) |
|  | V3 Supply caps | Increase current v3 supply cap for ETH to 350k tokens & WBTC to 12k tokens. No changes to COMP, UNI, & LINK. Will reassess if utilization increases | Increase if appropriate depending on supply cap utilization | Increase if appropriate depending on supply cap utilization | Increase if appropriate depending on supply cap utilization |
|  | Storefront Price Factor (currently 50%) | 60% (+10%) | 65% (+5%) | 62.5% (-2.5%) | 55% (-7.5%) |

Below we analyze the goals, execution plans, and mitigation strategies for each of the proposed parameter changes. We are using data from 2023-02-03.

## v2 & v3 net USDC supply & borrow APYs

To incentivize v2 USDC suppliers to migrate to v3, the net USDC supply rate (supply APY + supply COMP distributions) on v3 must be greater than that of v2. Similarly, to incentivize v2 USDC borrowers to migrate to v3, the net USDC borrow rate (borrow APY - borrow COMP distributions) on v3 must be less than that of v2.

Below are the supply APYs for v2 and v3 as of 2023-02-03:

|  | v2 | v3 |
| --- | --- | --- |
| USDC supply APY | 1.57% | 2.41% |
| USDC COMP supply distribution APY | 0.79% | 0% |
| USDC net supply APY | 2.36% | 2.41% |

The net v2 USDC supply APY is 2.36%, and the v3 USDC net supply APY is 2.41%. So USDC suppliers are currently only slightly incentivized to migrate to v3.

Below are the borrow APYs for v2 and v3 as of 2023-02-03:

|  | v2 | v3 |
| --- | --- | --- |
| USDC borrow APY | 3.30% | 4.10% |
| USDC COMP borrow distribution APY | 1.53% | 2.71% |
| USDC net borrow APY | 1.77% | 1.39% |

The net v2 USDC borrow APY is 1.77%, and the v3 USDC net borrow APY is 1.39%. So USDC borrowers are currently moderately incentivized to migrate to v3.

Updating the v2 & v3 USDC COMP distributions and v2 USDC reserve factor can further incentivize USDC suppliers and borrowers to migrate to v3. This is also motivated by the fact that v3 COMP APY would decrease if usages increase and we don’t migrate rewards.

## USDC COMP distribution migration

### Execution

We aim to migrate 100% of v2 USDC COMP distribution (supplies & borrows) to v3 by the end of the migration. This will increase the v3 USDC net supply APY and decrease the v3 USDC net borrows APY, thus incentivizing v2 USDC suppliers & borrowers to migrate to v3.

At first, we propose to migrate 50% of v2 USDC COMP distribution (supplies & borrows) to v3 to provide an initial impetus for users to migrate. We then propose to gradually migrate the remaining 50% USDC COMP distribution over in accordance with the above schedule.

### Mitigation plan

If we see a large swing in v2 and v3 utilization rates for an extended period of time, the community can adjust USDC COMP borrow & supply distributions accordingly to help balance the markets.

## USDC reserve factor increase on v2

### Execution

Increasing v2 USDC reserve factor decreases v2 USDC supply APY, thus further incentivizing USDC suppliers to migrate from v2 to v3.

The current USDC reserve factor is 7.5%. At first, we propose to moderately increase USDC reserve factor to 15% and then gradually increase it to 22.5% by the end of the migration in accordance with the above schedule.

Note that a small percentage of v2 USDC suppliers use their USDC borrowing power to borrow v2 assets, which may serve the new purpose of the v2 protocol. Therefore, it may be an acceptable outcome for these users to remain in the v2 protocol. Even though they will gain less net supply APY on their USDC as a result of our changes, their usage suggests that they will be less elastic to these changes, given they most likely value their USDC borrowing power more than net USDC supply APY.

### Mitigation plan

Similar to the COMP distribution plan, the community can adjust the v2 USDC RF accordingly to help drive the desired v2 utilization rate while monitoring how the intended v2 USDC suppliers respond to these changes. Also, the community can revert the v2 RF increases if we see users migrate from v2 to other protocols instead of v3 and shift focus to making v3 more appealing instead of making v2 less appealing.

## Supply cap increase

Below are the v3 supplies and supply caps for ETH and WBTC as of 2023-02-03:

|  | Supply | Supply cap | Supply cap utilization |
| --- | --- | --- | --- |
| ETH | 100,650 ($166.43M) | 150,000 ($248M) | 67.1% |
| WBTC | 3,588 ($83.47M) | 6,000 ($139.61M) | 59.8% |

### Goal

Increasing supply cap increases the protocol’s risk, but it’s necessary to grow the protocol.

We aim to accelerate the migration of assets with lower volatilities and larger liquidities from v2 to v3.

### Execution

We suggest initially increasing v3 supply caps for ETH and WBTC to 350k (~$580M) and 12,000 (~$279.22M), respectively. Note these caps are very close to the current v2 supplied amounts for each asset.

Assuming a successful migration in the first two weeks, we should see an increase in ETH and WBTC supply. Given current market conditions and similar user health factors, our simulations indicate the protocol should still be able to absorb the greater quantity of possible liquidations. Often, the insolvency risks we see in our simulations are due to users who supply lower-liquidity assets such as COMP at high borrow usage, which isn’t as much of a concern with ETH and WBTC.

As of 2023-02-01, WETH has 24h trading volume of $889,896,262 and +-2% market depth of ~$42m from trusted exchanges on Coingecko, and WBTC has $103,018,115 volume and ~$20m market depth. Based on the 24h volume and quote at 3% slippage, liquidators should be able to sell blocks of ~40m of WETH and blocks of ~20m WBTC with roughly 2% slippage, well-calibrated with a 5% liquidation bonus * 60% storefront price factor = 3% discount rate.

As the migration proceeds, we can assess increasing supply caps for lower-liquidity assets. These assets, however, generally pose greater insolvency risks, and we would perform further liquidity analysis first.

### Mitigation plan

If market conditions and/or user positions change such that our simulations indicate that these larger supply caps pose outsized risk, the community can decrease the supply caps. Additionally, the community can increase the storefront price factor to further incentivize healthy liquidations, as discussed in the next section.

## Storefront price factor

### Execution

We suggest initially increasing storefront price factor from 50% to 60% (+10%).

Assuming the migration is successful, we should see increased v3 asset inflow and a resulting increase in overall protocol risks. Increasing storefront price factor will further encourage turnover of absorbed assets from Comet to liquidators and help facilitate healthy liquidation cycles in the system. 

However, increasing storefront price factor does not monotonically decrease the system risk of the protocol. Although increasing it facilitates liquidations and prevents the protocol from holding non-stablecoin assets over time, large storefront price factor inhibits reserve growth. Therefore, assuming the initial migration plan is successful and the system is relatively stable, we aim to slowly decrease the storefront price factor to ensure healthy long-term reserve growth.

### Mitigation plan

If the protocol isn’t accumulating enough reserves as a result of our storefront price factor increase, the community can revert the changes.

## Next Steps and Timeline

We welcome the community’s feedback and plan on taking this to vote on 2023-02-13. We are targeting first round of proposals going live on 2023-02-20, but this is subject to delay depending on how governance proceeds.

*<sup>By approving this proposal, you agree that any services provided by Gauntlet shall be governed by the terms of service available at gauntlet.network/tos.<sup>*


