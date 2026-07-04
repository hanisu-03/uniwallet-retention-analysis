UniWallet Post-Competition Validation: 
## Does Feature Breadth or Engagement Drive Retention?
A data-backed follow-up to Team Catalyst Crew's ProduScope submission

## Context

During ProduScope (IIT Guwahati), our team built UniWallet, a student-first fintech MVP, and used RICE/MoSCoW to prioritize a lean core (Financial Literacy Nuggets, Allowance Mode) over feature-heavy additions (Smart Price Comparison, Brand Tie-Ups). This was a judgment call made under competition time constraints, without external data to confirm it. This project tests that judgment against real usage data.

## Related Work
Original competition submission: [UniWallet — ProduScope Deck](Catalyst_Crew_.pdf)

## Question

Does having more financial products/features increase customer retention, or does a focused core retain users better? And does active engagement matter more than product breadth?

## Method

Analyzed a public 10,000-customer bank dataset (Kaggle) as a behavioral proxy, since no UniWallet usage data exists yet. Defined a proxy activation funnel (signed up → has product → actively engaged → funded account → retained) since the dataset lacks timestamped events — noted as directional, not exact. Queried churn rate segmented by number of products and by active-membership status using SQL.

## Findings 


**Churn by number of products:**

| Products | Customers | Churn Rate |
|---|---|---|
| 1 | 5,084 | 27.7% |
| 2 | 4,590 | 7.6% |
| 3 | 266 | 82.7% |
| 4 | 60 | 100% |

**Churn by active status:**

| Active? | Customers | Churn Rate |
|---|---|---|
| No | 4,849 | 26.9% |
| Yes | 5,151 | 14.3% |

Retention peaks at 2 products, then collapses sharply at 3+ (small sample size at 3-4 products — 266 and 60 customers respectively — so directional, not statistically definitive). Active engagement independently cuts churn roughly in half, regardless of product count.


## Connection to UniWallet

This pattern supports our original RICE ranking: Financial Literacy Nuggets (18.00) and Allowance Mode (10.13) scored highest, ahead of Smart Price Comparison (5.67) and Brand Tie-Ups (3.15). The data suggests feature-stacking past a lean core correlates with worse, not better, retention — while engagement mechanics (which our gamification bets target) show a clear, independent retention benefit.

## Revised recommendation

Move Brand Tie-Ups from "Should-have" to "Won't-have for Phase 1" on the MoSCoW board. Prioritize deepening the Allowance Mode + gamification loop before adding product surface area. Reintroduce Brand Tie-Ups only after 90-day active-engagement benchmarks are met.

## Limitations

This is a proxy analysis using an unrelated bank dataset, not real UniWallet user data. The 3-4 product churn figures come from small sample sizes. Findings are directional signals to sanity-check product strategy, not conclusive proof.

