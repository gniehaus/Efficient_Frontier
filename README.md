Determining Optimal Equity Portfolio via Simulation and Optimization

Harry Markowitz won the nobel prize in 1990 for his theory on optimizing portfolios for risk-averse investors. The idea is to create a portfolio of different securities and weights in order to maximizie the Sharpe Ratio (Expected Portfolio Return - Risk Free Rate) / Standard Deviation of Portfolio. For this exercise, our focus is on an equity only portfolio.

In our analysis we look at 11 years of annual returns with 810 unique stocks. Data was pulled from a Bloomberg Terminal using an academic license. Stocks filtered by "EQS" Bloomberg command based on market cap, security type (common stock) and date of IPO. During our analysis we remove stocks with greater than 75% annual return (outliers).

To find our optimal portfolio, we used two different techniques: stochastic simulation and optimization. Assuming a .5% risk free rate (50 basis points), we find different portfolios and sharpe ratio's for simulation vs. optimization. Since optimization is guaranteed to find the constrained optimal solution (convex problem), the higher sharpe ratio (3.77 vs 2.50) comes from the optimization solution.

By changing the number of stocks and number of iterations, we could potentially make our simulation converge to the optimal solution. However, with 408 securities there exists 11,236,456 408c3 combinations. The amount of combinations grows significantly as the portfolio increases from 3..5..10..15.. stocks. The computational power would need to be much higher in order to simulate every random selection and weighting. Our simulation has 6M+ different portfolios and we plot the max sharpe, max return, and min risk portfolios.

We constrain our optimization problem with return, weighting, and std dev parameters, but by relaxing our constraints we increase the feasible region, and likely our objective value (Sharpe Ratio). Creating a portfolio using optimization is much easier to manipulate compared to simulation.
