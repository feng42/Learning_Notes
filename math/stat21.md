<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
**Statistical Thinking for the 21st Century**
* [简介](#简介)
* [Data](#Working with data)
	* [1 Data Type](#1-Data Type)
	* [2 Scales](#2-Scales)
	* [3 Measurement](#3-Measurement)
* [Probability](#Probability)
	* [1 Definition](#1-Definition)
	* [2 Determine Probabilities](#2-Determine Probabilities)
	* [3 Probability Distributions](#3-Probability Distributions)
	* [4 Independence](#4-Independence)
	* [5 Bayes's Rules](#5-Bayes's Rules)
	* [6 Learning from data](#6-Learning from data)
	* [7 Odds](#7-Odds)
* [Summarizing data](#Summarizing data)
	* [1 Summarizating tables](#1-Summarizating tables)
	* [2 Idealized representations](#2-Idealized representations)
* [Fitting models to data](#Fitting models to data)

<!-- markdown-toc end -->


# 简介
基于书《Statistical thinking for the 21st century》整理


# Working with data
## 1 Data Type
Bool / Integer / Real

## 2 Scales
1. values: Identity / Magnitude / Equal intervals / Up zero
2. scales: Nominal / Ordinal / Interval / Ratio
   opts:   
   Equal   x        x          x          x
   Greater          x          x          x
   Add                         x          x
   Mul/Div                                x 

## 3 Measurement
   constrcut -> with error
   reliability -> consistency of our measurement
   validity -> face / construct(convergent or divergent) / predictive


# Probability
## 1 Definition
1. Experiment: produces or observes an outcome
2. sample space: set of possible outcomes for an experiment
3. event: subset of the sample space
If P(Xi) is the probability of Xi:
- P(Xi)>=0
- Sum(P(Xi))|1~N = 1

## 2 Determine Probabilities
1. Pesonal opinion(all right...)
2. Emprical frequency
   many experiments -> count
   right ? law of large number
3. Classical probability
   P(OUTCOMEi) = 1 / number of possible outcomes
4. p(~A) = 1 - P(A)
	P(A ^ B) = P(A) * P(B) if A and B are independent
	P(A U B) = P(A) + P(B) - P(A ^ B)

## 3 Probability Distributions
1. Bernouli
	P(k;n,p) = P(X=k) = (n k)T * p^k * (1-p)^(n-k)
	(n k)T = n!/k! * (n-k)!
2. Cumulative
3. Condition
	P(A|B) = P(A^B) / p(B)

## 4 Independence
	P(A|B) = P(A)

## 5 Bayes's Rule
	P(B|A) = P(A|B) * P(B) / P(A)
	       = P(A|B) * P(B) / P(A|B) * P(B) + P(A|~B) * P(~B)

## 6 Learning from data
	P(A|B) --likehood
	P(A) --marginal likehood
	P(B|A) --posterior

## 7 Odds
	posterior odds = P(A|B) / P(~A|B)
	prior odds = P(A) / P(~A)
	odds ratio = posterior odds / prior odds


# Summarizing data

## 1 Summarizating tables
1. frequency distributions
2. cumulative

## 2 Idealized representations
1. normal(Gaussian) mean + standard deviation
2. skewness :: measure is non-negative
	right-skewed is common
3. long-tailed distributions


# Fitting models to data
