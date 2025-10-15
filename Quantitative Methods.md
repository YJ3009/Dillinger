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
3.1 Type I error
The true null hypothesis is incorrectly rejected.(true H~0~ denied)
- The null hypothesis is true, but you get a false positive leading to you rejecting the null hypothesis.
- This is also called a false positive.

Example: In court a defendant is found guilty despite being innocent.
 - [] Analysis the case


3.2 Type II error
The false null hypothesis is incorrectly accepted.(false H~0~ approved)

- The null hypothesis is false, but you get a false negative result, leading you to accepting the null hypothesis.
- This is also called a false negative.
 

Example: In court a defendant is found innocent despite being guilty.
- [] Analysis the case
 

3.3 Exmaple NHS digital



A good hypothesis or a bad hypothesis?









[pict](https://huanfachen.github.io/QM/sessions/week2_lecture.html#/not-everything-is-normal)