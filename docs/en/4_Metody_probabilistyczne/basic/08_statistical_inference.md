# Task List 08 — Statistical Inference Through Simulation

## General Philosophy

This task list closes the course by moving from probability and descriptive statistics to statistical inference.

The purpose is not to apply formulas mechanically.

The purpose is to investigate, simulate, visualize, compare, and explain how statistical inference works.

In every problem, students should treat formulas as summaries of observed behavior, not as black-box rules. Whenever a theoretical formula is used, it should be supported by simulation and visual evidence.

Students are encouraged to use Python, R, JavaScript, notebooks, dashboards, HTML applications, or any other suitable computational tool.

Interactive applications are especially welcome. In many problems it is useful to include sliders or input fields for parameters such as:

* number of trials,
* sample size,
* number of repeated samples,
* probability of success,
* distribution parameters,
* random seed,
* number of Monte Carlo repetitions.

The expected result is not only code and numerical output.
Each solution should include interpretation, plots, observations, and conclusions written in words.

Students may use AI tools to generate code, improve visualizations, or help design simulations. However, they must study, run, modify, and explain the results themselves.

The central question of this list is:

> How can we move from random data to careful conclusions under uncertainty?

---

# Problem 1 — Frequency Stabilization and the Law of Large Numbers

## Aim

Investigate how empirical frequencies behave when the number of trials increases.

This problem should make the Law of Large Numbers visible through simulation.

## Suggested experiments

Simulate repeated trials for:

* a fair coin,
* a biased coin,
* a fair die,
* a biased die,
* any other simple discrete experiment chosen by the student.

## Parameters to control

The simulation should allow changing:

* the number of trials $n$,
* the probability of success $p$, for coin-like experiments,
* probabilities of outcomes, for die-like experiments,
* the random seed,
* the number of repeated simulation runs.

## Investigation

Students should:

1. Simulate one long sequence of trials.
2. Plot the relative frequency of selected events as a function of the number of trials.
3. Repeat the experiment many times with different seeds.
4. Compare how different simulation paths fluctuate.
5. Observe what happens when $n$ is small, medium, and very large.
6. Compare empirical frequencies with theoretical probabilities.
7. Explain why empirical frequency is not exactly equal to theoretical probability.
8. Explain in their own words what stabilizes as $n$ increases.

## Required visualizations

At least:

* one line plot of relative frequency versus number of trials,
* one comparison of several simulation paths,
* one plot showing empirical probabilities against theoretical probabilities.

## Conceptual conclusion

Students should explain the Law of Large Numbers as an observed phenomenon:

> With many independent repetitions, empirical frequencies tend to stabilize near the theoretical probabilities, although random fluctuations never disappear completely.

---

# Problem 2 — Sample Size and Number of Samples Are Different

## Aim

Understand the difference between:

* increasing the size of one sample,
* increasing the number of repeated samples.

This distinction is crucial for understanding statistical inference.

## Simulation

Choose a simple random experiment, for example:

$$
X \sim Bernoulli(p)
$$

or

$$
X \sim N(\mu,\sigma^2).
$$

Generate many samples.

## Parameters to control

The simulation should allow changing:

* sample size $n$,
* number of samples $R$,
* parameter values such as $p$, $\mu$, or $\sigma$,
* random seed.

## Investigation

Students should:

1. Generate one sample and compute a statistic, for example $\hat p$ or $\bar x$.
2. Generate many samples of the same size.
3. Compute the same statistic for every sample.
4. Draw the distribution of the statistic.
5. Change $n$ while keeping $R$ fixed.
6. Change $R$ while keeping $n$ fixed.
7. Explain what changes when $n$ increases.
8. Explain what changes when $R$ increases.
9. Explain why a single sample gives only one possible value of a statistic.
10. Explain why many repeated samples reveal the behavior of the estimator.

## Required visualizations

At least:

* histograms of the estimator for different sample sizes,
* comparison of results for different numbers of repeated samples,
* a plot showing how the spread of the estimator changes with $n$.

## Conceptual conclusion

Students should understand that:

> The sample size controls how much information is in one sample.
> The number of repeated samples controls how well we can observe the behavior of the estimator in a simulation.

---

# Problem 3 — Sampling Distribution of a Proportion

## Aim

Investigate the behavior of the sample proportion:

$$
\hat p = \frac{X}{n}.
$$

This problem prepares students for confidence intervals and hypothesis tests for proportions.

## Simulation

Choose a Bernoulli model:

$$
X_i \sim Bernoulli(p).
$$

Generate many samples and compute $\hat p$ for each sample.

## Parameters to control

The simulation should allow changing:

* true probability $p$,
* sample size $n$,
* number of repeated samples $R$,
* random seed.

## Investigation

Students should:

1. Generate many samples for a fixed $p$ and $n$.
2. Compute $\hat p$ for each sample.
3. Draw the histogram of simulated $\hat p$ values.
4. Change $n$ and observe how the histogram changes.
5. Change $p$ and observe how the center and spread change.
6. Compute the empirical mean of the simulated $\hat p$ values.
7. Compare it with the true value $p$.
8. Compute the empirical standard deviation of the simulated $\hat p$ values.
9. Compare it with the theoretical standard error:

$$
\sqrt{\frac{p(1-p)}{n}}.
$$

10. Explain why $\hat p$ is an estimator and also a random variable.

## Required visualizations

At least:

* histograms of $\hat p$ for several values of $n$,
* a plot of empirical standard deviation versus theoretical standard error,
* a visualization showing the true value $p$ as a reference line.

## Conceptual conclusion

Students should explain that:

> The sample proportion fluctuates from sample to sample, but for large samples it usually stays closer to the true probability.

---

# Problem 4 — Sampling Distribution of the Mean and the Central Limit Effect

## Aim

Investigate why averages are more stable than individual observations and why normal-shaped distributions appear in statistics.

## Simulation

Use several different data-generating distributions, for example:

* uniform distribution,
* exponential distribution,
* lognormal distribution,
* die rolls,
* Bernoulli trials,
* normal distribution.

For each distribution, generate many samples and compute their means.

## Parameters to control

The simulation should allow changing:

* distribution type,
* distribution parameters,
* sample size $n$,
* number of repeated samples $R$,
* random seed.

## Investigation

Students should:

1. Plot the original distribution of individual observations.
2. Generate many samples of size $n$.
3. Compute the sample mean for each sample.
4. Plot the histogram of sample means.
5. Repeat for increasing values of $n$.
6. Observe how the distribution of sample means changes.
7. Standardize the sample means:

$$
Z=\frac{\bar X-\mu}{\sigma/\sqrt n}.
$$

8. Compare the standardized histogram with the standard normal distribution.
9. Explain why the original distribution and the distribution of sample means are different.
10. Explain the intuition behind the Central Limit Theorem.

## Required visualizations

At least:

* histogram of the original data-generating distribution,
* histograms of sample means for several $n$,
* comparison with a normal curve,
* visualization of how the spread decreases as $n$ increases.

## Conceptual conclusion

Students should understand that:

> The normal distribution appears because sums and averages of many independent random variables often have an approximately normal shape, even when the original observations are not normally distributed.

---

# Problem 5 — Confidence Intervals for a Proportion by Simulation

## Aim

Understand confidence intervals through repeated sampling, not only through a formula.

## Simulation

Choose a true probability $p$.
Generate many samples.
For each sample compute $\hat p$ and construct a confidence interval.

For example:

$$
\hat p \pm 1.96\sqrt{\frac{\hat p(1-\hat p)}{n}}.
$$

## Parameters to control

The simulation should allow changing:

* true probability $p$,
* sample size $n$,
* confidence level,
* number of repeated samples $R$,
* random seed.

## Investigation

Students should:

1. Generate many samples from the same Bernoulli model.
2. Construct a confidence interval for each sample.
3. Check whether each interval contains the true value $p$.
4. Estimate the empirical coverage probability.
5. Compare empirical coverage with the chosen confidence level.
6. Visualize many intervals on one plot.
7. Mark intervals that contain $p$ differently from intervals that miss $p$.
8. Change $n$ and observe how the interval width changes.
9. Change the confidence level and observe how the interval width changes.
10. Explain what a 95% confidence interval means and what it does not mean.

## Required visualizations

At least:

* plot of many confidence intervals,
* coverage rate as a function of sample size,
* interval width as a function of sample size,
* comparison of different confidence levels.

## Conceptual conclusion

Students should explain that:

> The confidence level describes the long-run behavior of the interval-building procedure over many repeated samples.

---

# Problem 6 — Confidence Intervals for a Mean by Simulation

## Aim

Understand uncertainty in estimating a population mean.

## Simulation

Generate data from a distribution with known mean.
Use both symmetric and skewed distributions.

Examples:

$$
X \sim N(\mu,\sigma^2)
$$

and a lognormal distribution.

## Parameters to control

The simulation should allow changing:

* distribution type,
* distribution parameters,
* sample size $n$,
* confidence level,
* number of repeated samples $R$,
* random seed.

## Investigation

Students should:

1. Generate many samples from a known population.
2. Compute $\bar x$ and $s$ for each sample.
3. Construct confidence intervals for the population mean.
4. Check how often the intervals contain the true mean.
5. Compare performance for normal and skewed distributions.
6. Compare small, medium, and large sample sizes.
7. Investigate when the normal approximation works well.
8. Investigate when the interval procedure becomes unreliable.
9. Explain why the sample standard deviation $s$ replaces the unknown $\sigma$.
10. Interpret one interval in a real context.

## Required visualizations

At least:

* intervals plotted across repeated samples,
* histogram of sample means,
* comparison of interval width for different $n$,
* coverage rate for different distributions and sample sizes.

## Conceptual conclusion

Students should understand that:

> A sample mean is only one estimate of the population mean.
> A confidence interval describes the uncertainty of that estimate.

---

# Problem 7 — Hypothesis Testing as a Simulation Under the Null Hypothesis

## Aim

Understand a hypothesis test as a comparison between observed data and simulated data under a reference assumption.

## Situation

Use a coin experiment.

Suppose we observe $h$ heads in $n$ tosses.

We test:

$$
H_0:p=0.5
$$

against an alternative such as:

$$
H_1:p\neq 0.5.
$$

## Parameters to control

The simulation should allow changing:

* observed number of heads $h$,
* number of tosses $n$,
* null hypothesis value $p_0$,
* number of Monte Carlo repetitions $R$,
* one-sided or two-sided alternative.

## Investigation

Students should:

1. Treat the observed result as fixed.
2. Simulate many experiments assuming $H_0$ is true.
3. Plot the distribution of the number of heads under $H_0$.
4. Mark the observed result on the plot.
5. Decide whether the observed result looks typical or unusual.
6. Estimate the p-value by simulation.
7. Compare the simulated p-value with an exact binomial calculation if possible.
8. Change $n$ and observe how the interpretation changes.
9. Explain why a small deviation may matter for large $n$ but not for small $n$.
10. Write a careful statistical conclusion.

## Required visualizations

At least:

* histogram of simulated results under $H_0$,
* observed result marked on the histogram,
* visualization of tail areas,
* p-value as a function of observed deviation or sample size.

## Conceptual conclusion

Students should explain that:

> A p-value measures how unusual the observed data would be if the null hypothesis were true.
> It is not the probability that the null hypothesis is true.

---

# Problem 8 — Goodness of Fit: Is This Die Fair?

## Aim

Understand the chi-square goodness-of-fit test through simulation.

The formula should appear as a way to measure discrepancy between observed and expected counts.

## Situation

A die is rolled many times.
The observed counts are:

$$
O_1,\ldots,O_6.
$$

Under the fair-die hypothesis, the expected counts are:

$$
E_i = \frac{n}{6}.
$$

Define the discrepancy statistic:

$$
D=\sum_{i=1}^{6}\frac{(O_i-E_i)^2}{E_i}.
$$

## Parameters to control

The simulation should allow changing:

* number of rolls $n$,
* probabilities of die outcomes,
* number of Monte Carlo repetitions $R$,
* random seed.

## Investigation

Students should:

1. Generate observed die-roll data.
2. Compute observed frequencies.
3. Compute expected frequencies under the fair-die model.
4. Compute the discrepancy statistic $D$.
5. Simulate many fair-die experiments with the same $n$.
6. Compute $D$ for each simulated experiment.
7. Plot the simulated distribution of $D$ under fairness.
8. Mark the observed $D$ on the plot.
9. Estimate the p-value by simulation.
10. Compare the simulation result with the chi-square approximation.

## Required visualizations

At least:

* observed versus expected bar chart,
* histogram of simulated discrepancy statistics,
* observed discrepancy marked on the histogram,
* comparison of fair and biased dice.

## Conceptual conclusion

Students should understand that:

> A goodness-of-fit test checks whether the observed frequency table is unusually far from what the model predicts.

---

# Problem 9 — Comparing Two Groups by Randomization and Simulation

## Aim

Move from descriptive comparison to inferential comparison.

The main question is:

> Is the observed difference large compared with differences that could appear by random variation alone?

## Situations

Use at least two contexts:

* exam scores in two groups,
* pass rates in two groups,
* customer renewal rates by channel,
* machine measurements,
* delivery times by zone.

## Parameters to control

The simulation should allow changing:

* group sizes,
* group means or proportions,
* standard deviations,
* number of randomization or Monte Carlo repetitions,
* random seed.

## Investigation

Students should:

1. Compute the observed difference between two groups.
2. Use plots to describe both groups.
3. Simulate data under a no-difference assumption.
4. Generate the null distribution of differences.
5. Mark the observed difference on the null distribution.
6. Estimate a simulation-based p-value.
7. Construct a confidence interval for the difference.
8. Compare statistical significance with practical importance.
9. Investigate the role of sample size.
10. Explain why comparing only sample means or sample proportions may be misleading.

## Required visualizations

At least:

* side-by-side histograms or boxplots,
* distribution of simulated differences under the null hypothesis,
* observed difference marked on the plot,
* confidence interval for the difference.

## Conceptual conclusion

Students should understand that:

> A difference observed in one dataset must be compared with the amount of random variation expected under repeated sampling.

---

# Problem 10 — Final Simulation-Based Statistical Investigation

## Aim

Prepare a complete statistical investigation combining the whole course.

This is an open final project.

## Task

Choose or generate a dataset related to one of the following contexts:

* coin tosses,
* die rolls,
* defective products,
* exam scores,
* customer renewals,
* delivery times,
* machine measurements,
* call center requests,
* web service errors,
* another approved context.

The investigation must contain both descriptive statistics and statistical inference.

## Required components

The final report or application must include:

1. description of the random experiment or data-generating mechanism,
2. definition of variables and observed outcomes,
3. exploratory visualizations,
4. descriptive statistics,
5. empirical probabilities or conditional frequencies,
6. at least one estimator,
7. visualization of sampling variability,
8. at least one confidence interval,
9. at least one hypothesis test,
10. at least one Monte Carlo simulation supporting the inference.

## Interactive or computational component

Students should prepare one of the following:

* a notebook,
* a dashboard,
* a small HTML/JavaScript application,
* a Python application,
* another interactive computational tool.

The tool should allow changing at least two important parameters, for example:

* sample size,
* number of repeated samples,
* true probability,
* mean,
* standard deviation,
* number of Monte Carlo repetitions,
* confidence level,
* significance level.

## Required interpretation

The final explanation should answer:

1. What is random in this problem?
2. What is fixed but unknown?
3. What is observed in one sample?
4. What changes across repeated samples?
5. What does the simulation show?
6. What does the formula summarize?
7. What conclusion is justified?
8. What conclusion would be too strong?
9. What are the limitations of the analysis?
10. How does this problem connect probability theory with statistical inference?

## Conceptual conclusion

The final project should show that:

> Statistical inference is not the mechanical use of formulas.
> It is the process of using probability, simulation, and data to make careful conclusions under uncertainty.
