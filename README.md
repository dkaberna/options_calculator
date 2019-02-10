# options_calculator

The objective for this code is to price Exact (closed) options.  This code was written while completing the Baruch C++ Financial Engineering course. 

## Software Features
The following features have been written in C++:

1.Exact Solutions of One-Factor Plain Options.
    This feature of code calculates plain (European) equity options (with zero dividends) and their sensitivies.  These options can be exercised at expiry time T only.

The parameters whose values that need to be initialized are:
• T (expiry time/maturity). This is a number, e.g. T = 1 means one year. K (strike price).
• sig (volatility).
• r (risk-free interest rate).
• S (current stock price where we wish to price the option).
• C = call option price, P = put option price

Finally, we note that n(x) is the normal (Gaussian) probability density function and N(x) is the cumulative
normaldistributionfunction,bothofwhicharesupportedin Boost Random.  I used Black-Scholes formula to calculate the price of a call (or put) option on some underlying asset. 

This code is capable of computing option prices as a function of i) expiry time, ii) volatility, or iii)
any of the option pricing parameters. The purpose here is to be able to input a matrix (vector of
vectors) of option parameters and receive a matrix of option prices as the result. 

2.) Option Sensitivities, aka the Greeks

Option sensitivities are the partial derivatives of the Black-Scholes option pricing formula with respect to one of
its parameters. Being a partial derivative, a given greek quantity is a measure of the sensitivity of the option
price to a small change in the formula’s parameter.  This code is able to calculate call/put: Delta, Rho, Vega, and Theta.  Additionally, it is capable of computing call/put delta prices for a monotonically increasing range of
underlying values of S, for example 10, 11, 12, …, 50. To this end, the output will be a vector and it entails
calling the above formula for a call delta for each value S and each computed option price will be store in a
std::vector<double> object.

This code is capable of using divided differences to approximate option sensitivities.

3.) Perpetual American Options

This code is capable of calculating Perpetual American Options.

## Installation

A makefile is provided to compile the code in Linux.

## Class Design
A detailed visualization of the class design can be found [here](https://github.com/dkaberna/options_calculator/tree/master/docs/Writeup.pdf).
