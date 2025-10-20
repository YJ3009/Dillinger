# Quantitative Methods
---
---
\*MATH Chart[https://www.desmos.com/calculator?lang=zh-CN]
## Lecture 01
> Different data types
Key data metrics
the middle and the spread
Visualising the data
Data outliers

#### 1. What is Quanitative Research?
* the process of collecting and analysing numerical data to describe, model, and predict variables of interest.

#### 2.Data Type
| Function  |Nominal|Ordinal|Interval|Ratio|
| ----------- | ----------- | ----------- | ----------- | ----------- |
|Categorizes and labels variables|✔  |✔ |✔  |✔  |
|Ranks categories in order|  |✔ |✔  |✔  |
|Has known, equal intervals| | |✔  |✔  |
|Has a true or meaningful zero|  | |  |✔  |

Nominal(categorical data): Differentiates items based only on names; no order between them.
> colour, gender, country names 



## Lecture 02
> Representative data
Normal distribution
Binomial distribution
Poisson distribution
Exponentials
Logarithms

Exploratory data analysis - the first step in the scientific method.
- How to understand the dataset
- What do the variables represent
- What statistical techniques should be used

Introducing statistical concepts
- Data science is about using ideas from statistics to describe large datasets
- Focus on numerical data
- Using probability distributions to characterise them
 
### Representative data
##### The dream vs reality
##### Approximating
we sample a subset of the data

## Lecture 03 Hypothesis Testing
> Representative data
Normal distribution
Binomial distribution
Poisson distribution
Exponentials

#### 1.Research question vs. hypothesis
- Research question: focuses on a ==specific problem==.
    \* In quantitative research, there are three main types of research questions: ==descriptive, comparative, and relational==.
- Hypothesis: A formal ==statement== that you will seek to prove or disprove.
    \* Research hypotheses are more focused and ==scientific and predictive==. They are to be proven or disproven, and they ==typically concern issues of cause and effect, nullification, direction, and non-direction==.

#### 2.Establishing and evaluating a hypothesis (in 5 steps)
2.1 Define the null and alternative hypothesis
- H~0~: the null hypothesis
    - this is the “status quo”
    - it is ==assumed to be true==
- H~1~: the alternative hypothesis
    - your hypothesis
    - it requires some evidence (i.e. data) to verify
    - it directly contradicts the null hypothesis

2.2 Set your significant level α 
The significance level is the threshold below which you reject the null hypothesis.
- Decide what “too unlikely” means (before you do the test.'HARKing': Hypothesising After the Results are Known)
- Common choice is 5% significance
    - ==α=0.05==
    - This means that if we see evidence that would have less than a 5% chance of occurring under the null hypothesis, then we reject the null hypothesis.

2.3 Identify the evidence
- This could mean collecting the data
- Or identifying a suitable existing dataset
    - Crucial that it’s suitable - think about biased/ unrepresentative data

2.4 Calculate the p-value
The ==p-value is the probability of seeing the evidence==, or something even more extreme, if the null hypothesis is true.

- Calculated according to the appropriate statistical test
- The choice of test is determined by the research question and the data

2.5 Compare p-value with significance level
- ==p-value >α==
    - Evidence not that unlikely.
    - Not enough evidence to reject H~0~
- ==p-value ≤α==
    - Evidence very unlikely.
    - Reject H~0~ and accept H~1~
.

#### 3. Types of error
3.1 ==Type I error==
The true null hypothesis is incorrectly rejected.==(Reject true H~0~)==
- The null hypothesis is true, but you get a false positive leading to you rejecting the null hypothesis.
- This is also called a false positive.

Example: In court a defendant is found guilty despite being innocent.
 - [] Analysis the case


3.2 ==Type II error==
The false null hypothesis is incorrectly accepted.==(Accept false H~0~)==

- The null hypothesis is false, but you get a false negative result, leading you to accepting the null hypothesis.
- This is also called a false negative.
 

Example: In court a defendant is found innocent despite being guilty.
- [] Analysis the case
 

3.3 Exmaple NHS digital
- [] Analysis the case

3.4 Matrix of errors
|   |Accept the H~0~|Reject the H~0~|
| ----------- | ----------- | ----------- |
|H~0~ == True|✔  |Type I error |
|H~0~ == False| Type II error  |✔ |

#### 4. A good hypothesis or a bad hypothesis?
4.1 Understanding the literature and the context
- The hypothesis should not come out of thin air.
- Should consider:
    - What do you know about the ==context==?
    - What ==research== have other people done?

4.2 Asking ethical hypothesis questions
It’s important to ==not make unethical assumptions== in choosing the hypothesis.

4.3 Correlation vs. Causation
- Correlation: Two variables are statistically related, ==as one changes so does the other==.
- Causation: One variable ==influences== the other variable ==to occur==.

4.4 Correlation IS NOT causation
You might not know whether events are correlated, or causing each other
BUT
you should use your contextual understanding to come up with plausible (and ethical) initial questions.


####  5. Example
Research question:
- Are male and female students similar heights?

Research hypothesis:
- Male and female students are different heights on average.

5.1 Define the null and alternative hypothesis

H~0~: The mean height of male and female students is the same.
H~1~: The mean height of male and female students is different.

5.2 Set your significance level

α=0.05

5.3 Identify the evidence

| Group  |Sample size|Mean(CM)|Standard deviation(CM)|
| ----------- | ----------- | ----------- |----------- |
|Female students|95  |170 |5|
|Male students| 103 II error  |180 |6|

5.4 ==Calculate the p-value==
5.4.1 We need to know what ==statistical test== to use!
- Numerically testing whether the data supports the hypothesis.

5.4.2 Parametric vs. Non-parametric tests

Parametric tests
- ==Assumptions about the distribution==:
    - ==Normal distribution==
    - Independent and unbiased samples
    - Equal/comparable variances
    - Continuous data

    .1 ==Comparison of means of normal distribution==：When the population distribution is assumed to be normal, the ==t-test or z-test== can be used to compare whether the two sample means are significantly different.
    
    .2 ==Variance comparison==: When the population ==distribution is assumed to be normal==, ==ANOVA== can be used to compare whether the variances of multiple samples are significantly different.
    
    .3 ==Coefficient test in regression analysis==: In linear regression analysis, the ==t-test== can be used to test whether the regression coefficient is ==significantly different from zero==.

Non-parametric tests
- Typically less assumptions on the distribution
- Continuous or discrete data

    .1 Sample distribution deviation test: When the shape of the ==population distribution is unknown or cannot be modeled==, the Kolmogorov-Smirnov test ==(KS test)== can be used to test whether the sample data conforms to a specific distribution.
    
    .2 Median comparison: When the sample data does ==not meet the normal distribution assumption==, the ==Wilcoxon signed-rank test== or the ==Mann-Whitney U test== can be used to compare whether the medians of two samples are significantly different.
    
    .3 Multiple sample comparison: When there are ==multiple samples and the distribution is skewed or unknown==, the ==Kruskal-Wallis test== can be used to compare whether the medians of multiple samples are significantly different.

5.4.3 Deciding on a test
It can be hard to figure out what test to use.
Helpeful llink:
[Flow Chart of Selecting Commonly Used Statistical Tests](https://www.brookes.ac.uk/getmedia/bede726d-771d-461f-900b-a3526fc7e199/stats-flow-chart.pdf)



5.4.3.1 Parametric tests
\* Student’s T-test (used to compare the mean of a dataset.)
- parametric statistical test
- assumes the data is normally distributed

steps:
- Calculate:
    - test statistic (**t**), is a number that summarises the data so as to determine whether to reject the null hypothesis.
    - degrees of freedom(**df**), is the number of values in the final calculation that are free to vary.
    - look up which types of t test
        - ==one sample t-test==: is there a difference between a group and the population
        t= [1]   df=n-1
        
        - ==Independent sample t-test==: is there a difference between two groups
          t= [2]   df=n~1~+n~2~−2

        - ==Paired sample t-test==: is there a difference in a group between two points in time
        t= [3]   df=n-1
        
    - How many tails?[4]
        - One tailed: if you only care is the mean is significant in one direction
        - Two tailed: if you care about the mean being different regardless of direction


5.4.3.2 Non-parametric tests
\* ==Kolmogorov-Smirnov==[5]
- Compares two probability distributions
- Can be used to test whether an observed sample came from a given distribution
- Or to test whether two samples both came from the same distribution

Procedure
-  one sample test[6]
    -  Tests if a sample dataset came from a known distribution.
-  empirical distribution function[7]
-  two sample test[8]
-  decision rule
    - H~0~: the distributions are the same
    - H~1~: the distributions differ
    - Larger values of the test statistic D
 is stronger evidence against H0

\* ==Kernel density estimate (KDE)==
- Used to generate a smooth probability density function for a random variable dataset
- Useful for understanding the underlying distribution of a sample
- Think of it as getting a smooth function to describe a histogram of data
- There are no assumptions about the prior distribution

KDE of simulated heights
```
import numpy as np
import pandas as pd 
from scipy.stats import gaussian_kde

# Supposing you have some data 
data = pd.read_csv('/path_to_data')

# Kernel Density Estimation
kde = gaussian_kde(data)
x_vals = np.linspace(100, 200, 100)
y_vals = kde(x_vals)
```
EXAMPLE of heights distribution[9]
KDE use case
- fit the KDE to two sample datasets
- compare visually
- carry out a non-parametric test - such as Kolmogorov-Smirnov

####  6.Example: students height[10]









[pict](https://huanfachen.github.io/QM/sessions/week2_lecture.html#/not-everything-is-normal)



[1]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/students-t-test-one-sample>
[2]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/students-t-test-two-sample>
[3]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/students-t-test-paired>
[4]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/how-many-tails>
[5]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/kolmogorov-smirnov>
[6]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/k-s-test-one-sample-test>
[7]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/k-s-empirical-distribution-function>
[8]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/k-s-test-two-sample-test>
[9]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/kde-of-simulated-heights-1>
[10]:<https://huanfachen.github.io/QM/sessions/week3_lecture.html#/example---step-1-2-3>