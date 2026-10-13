# econ3916-lab05-monte-carlo
# Monte Carlo Engine -- Probability & Simulation

## Objective
I used random simulation to estimate probabilities and financial risk measures, then checked how the accuracy of those estimates improves as the number of trials grows.

## Methodology
- I simulated 10,000 fair coin flips and plotted the running share of heads to watch it settle toward 0.5 as the number of flips increased.
- I simulated 10,000 games of the Monty Hall problem and counted how often switching doors won compared with staying.
- I simulated a disease screening test on 100,000 people, using a prevalence of 1%, a sensitivity of 95%, and a specificity of 90%. I then counted what share of the people who tested positive were actually sick.
- I simulated returns for a $1M portfolio and used the simulated losses to compute the 95% Value at Risk (VaR) and the 95% Expected Shortfall (ES).
- I estimated pi with Monte Carlo sampling at several sample sizes and checked that the estimation error shrinks at a rate of about 1/sqrt(n).

### Key Findings
- **Coin flips:** The running share of heads moved around a lot early on and got closer to 0.5 as more flips were added.
- **Monty Hall:** Switching won 6,694 of the 10,000 games.
- **Disease screening:** Only 9.2% of positive tests came from people who were actually sick. Because the disease is rare, most positive results were false positives, even though the test is fairly accurate.
- **Portfolio risk:** The 95% VaR was $19,494 and the 95% ES was $24,230. VaR is the loss I would not expect to exceed on 95% of days. ES is the average loss on the worst 5% of days, so it says more about how bad the tail can get.
- **Convergence:** The error in my pi estimate fell at a rate of about 1/sqrt(n). This means that to cut the error in half, I need about four times as many samples.
