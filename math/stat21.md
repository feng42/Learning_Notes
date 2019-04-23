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
	* [1 model](#1-model)
	* [2 modeling](#2-modeling)
	* [3 what makes a model "good"](#3-what makes a model good)
	* [4 some models](#4-some models)
	* [5 Variability](#5-Variability)
	* [6 Z-scores](#6-Z-scores)
* [Fitting models to data](#Fitting models to data)
	* [1 model](#1-model)
	* [2 modeling](#2-modeling)
	* [3 what makes a model "good"](#3-what makes a model good)
	* [4 some models](#4-some models)
	* [5 Variability](#5-Variability)
	* [6 Z-scores](#6-Z-scores)
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
## 1 model
"All models are wrong but some are useful."
	data = model + error

## 2 modeling
	mode : most common value
	average: arithmetic mean
	RMSE : root mean squared error
	parameter \ constant(intercept)

## 3 what makes a model good
error comes from:
	model is wrong
	measurement error or noise
sample : a set of data points selected

## 4 some models
mean : 
	minimize sum of sqaured errors
	highly sensitive to extreme values
medium:
	minimize sum of absolute errors
	representitive of the group
mode :
	most common value

## 5 Variability
"hat"==estimate
dispersion: how widely dispersed the data are
variance: mean squared error
degree of freedom: don't count==estimate will be biased

## 6 Z-score
	Z(x) = (x - mu) / sigma     //calculate distribution
		mean of zero (if not numerical precision)
		standard deviation
	Interpreting
		standrad normal distribution(mean of Zero)
	Standradlized scores
		mean: 100
		std deviation: 10 


# Data Visulization
## 1 Anatomy
	bar / bar with points / violin / box

## 2 Principles of good
	data/ink ratio = amount of ink used / total amount of ink

## 3 Avoid/Obey
	* chartjunk
	* distorting the data: axis scaling / zero
	* lie factor
	* perceptual limitations


# Sampling
## 1 how sampling
	goal:
		determine feature of interest, using subset
		representative
		compute bias
		with/without replacement

## 2 sampling error
	sampling error
		diffrence between sample and all data
		related to measurement
	sampling distribution
		estimate vary from sample to sample	

## 3 standard error of mean
	SEM = sigma / sqrt(n)
		n== size of sample
		sigma== standrad deviation
		sigma computed on the sample

## 4 Central limit theorem
	theorem
		size get larger, sampling distribution of mean will be normally
		even if data with each are not normally

## 5 Confidence interval
	definition
		uncertainty about how close the estimate is
	quantile
		find the start & end of interval of distribution
	compute
		CI(95%) = _X +- 1.96 * SEM	//normal
	explain
		if is about sampling and distribution, the real value of data is fixed


# Resampling and simulation
## 1 Monte Carlo Simulation
	performing:
		Define a domain of possible values
		Generate random numbers with that domain from a probability distribution
		Perform a computation using the random numbers
		Combine the results across many repetitions

## 2 randomness
	random process
		unpredictable
	preidolia / gambler's fallacy

## 3 Generating random numbers
	truly random is expensive to compute
	pseudo-random
		repeate after long time
	using quantile function
		generate from uniform distribution
		map into distribution of interest
	random seed

## 4 bootstrap
	idea
		repeatedly sample from the dataset
		sample with replacement
	often used to generate standrad error for estimates of unknown distribution


# Hypothesis testing
Describe / Decide / Predict

# 1 Null Hypothesis Statistical Testing
	steps
		Make predictions based on hypothesis
		Collect some data relevant to the hypothesis
		Specify null and alternative hypothesis
		Fit a model to the data that represents the alternative and compute statistic
		Compute the probability of the observed value of that statistic assuming that the null hypothesis is true
		Assess the "statistical significance" of the result

## 2 Process
	null hypothesis==involves equality
	alternative hypothesis==involve inequality
	directional / non-directional == with/without predicting direction
	t-statistic -- comparison of two independent groups
		t = hat(X1) - hat(X2) / sqt(S1^2/n1 + S2^2/n2)
		--hat(X) ==means of groups
		--S^2 ==estimate variance of groups
		--n ==size of groups
	binomial distribution:
		P(X<k) = Sum[ (N k)^T * p^i * (1-p)^(n-i) ]
		P(X>=k) = 1 - P(X<k)
	p-value
		a value of the t-statistic greater than or equal to observed value
		P(data|H0)

## 3 Determine
	statistical significance
		0.05 
		IS NOT practical significance
	Neyman-Person approach
		reject H0 if false (hit)
		fail to reject H0 if true (correct rejection)
		reject H0 while true (false alarm, Type I error)
		fail to reject H0 if false (miss, Type II error)
		P(Type I error) =alpha, set .05
		P(Type II error) =beta, set .2
	familywise error
		error across all of the tests
	

# Confidence intervals, effect sizes, and statistical power
## 1 Confidence intervals
	DESCRIBE an interval that contain the true parameter with a given probability on average	
	NOT statement about the parameters
	Computed as
		CI = point estimate +- critical value
	if normal distribution
		CI = hat(X) +- 1.96* SE  //95%
	if t-distribution
		CI = hat(X) +- t(crit)*SE

## 2 Effect sizes
	Cohen's D
		d = (hat(X1) - hat(X2)) / s
		s = sqrt( (n1-1)*s1^2 + (n2-1)*s2^2 / (n1+n2-2) )
		0.2==small, 0.5==medium, 0.8==large
	Pearson's r
		correlation coeffcient
		varies from -1 to 1
	Odds ratio
		pdds of A = P(A) / p(~A)

## 3 Statistical power
	power = 1 - beta
	affect power
		sample size:larger samples-> greater
		effect size:finding larger effects is easier
		Type I error rate:decrease -> decrease
