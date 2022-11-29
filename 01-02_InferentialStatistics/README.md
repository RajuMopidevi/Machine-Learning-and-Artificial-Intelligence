### Inferential Statistics
2. Inferential Statistics
    1. Basics of Probability
        1. Introduction: Inferential Statistics
            - Process of “inferring” insights from sample data is called “Inferential Statistics”.
        2. Random Variables
            - The **random variable X** basically converts outcomes of experiments to something measurable
        3. Probability Distributions - I
            - The three-step process for this is:
                1. Find all the possible combinations
                2. Find the probability of each combination
                3. Use the probabilities to estimate the profit/loss per player
            - Probability = $\frac{Favourable Outcomes}{Total Outcomes}$
        4. Probability Distributions - II
            - A **probability distribution** is ANY form of representation that tells us the probability for all possible values of X
        5. Expected Value - I
            - The **expected value** for a variable X is the value of X we would “expect” to get after performing the experiment once. It is also called **the expectation**, **average**, and **mean value**
            - The **expected value** should be interpreted as the **average value** you get after the experiment has been conducted an **infinite number of times**.
            - The expected value (EV) is given by: $EV(X) = x_1 * P(X=x_1) + x_2 * P(X=x_2) + x_3 * P(X=x_3) + . . . . . + x_n * P(X=x_n) $
        6. Expected Value - II
            - $$E[X] = \sum_{i=1}^{i=n} x_i P(X=x_i)$$
            - If Expected Value comes out to be negative, we can say that the project is not worth investing in
    2. Discrete Probability Distributions
        1. Probability Without Experiment
            - Theoretical (calculated) values of probability are actually quite close to the experimental values.
            - The small differences can be noticed if the experiments are low in number.
        2. Binomial Distribution
            - The binomial distribution can be used if, for an experiment:
                * The total number of trials is fixed
                * Each trial is binary, i.e. has only two possible outcomes, success and failure
                * The probability of success is the same for all the trials
            - The formula for finding binomial probability is given by 
                - $$P(X=r) = {}^n C_r (p)^r (1-p)^{n-r} $$ Where n is no. of trials, p is probability of success and r is no. of successes after n trials.
                - Few examples to understand binomial distribution
                   | Binomial Distribution Applicable |	Binomial Distribution Not Applicable |
                   |----------------------------------|----------------------------------------|
                   |Tossing a coin 20 times to see how many tails occur	| Tossing a coin until a heads occurs |
                   |Asking 200 randomly selected people if they are older than 21 or not |	Asking 200 randomly selected people how old they are |
                   | Drawing 4 red balls from a bag, putting each ball back after drawing it| Drawing 4 red balls from a bag, not putting each ball back after drawing it |
        3. Cumulative Probability
            - **cumulative probability of X**, denoted by F(x), is defined as **the probability of the variable being less than or equal to x**.
            - $$F(x) = P(X{\leq}x)$$
    3. Continuous Probability Distributions
        1. Probability Density Functions - I
            - **CDF**, or a **cumulative distribution function**, is a distribution which plots the cumulative probability of X against X.
            - **PDF**, or **Probability Density Function**, however, is a function in which the area under the curve, gives you the cumulative probability
            - PDFs are more commonly used in real life. The reason is that it is much easier to see patterns in PDFs as compared to CDFs
            - _The PDF clearly shows uniformity_, as the probability density’s value remains constant for all possible values. However, the _CDF does not show any trends_ that help you identify quickly that the variable is uniformly distributed
        2. Normal Distribution
            - All data that is normally distributed follows the 1-2-3 rule. This rule states that there is a -
                * 68% probability of the variable lying within 1 standard deviation of the mean
                * 95% probability of the variable lying within 2 standard deviations of the mean
                * 99.7% probability of the variable lying within 3 standard deviations of the mean
        3. Standard Normal Distribution
            - standardised random variable   $$Z = \frac{x - \mu }{ \sigma }$$
            - cumulative probability    
                 $$ F(Z) = \frac{1}{\sqrt{2 \pi}} $$
    4. Central Limit Theorem
        1. Introduction: Central Limit Theorem
        2. Samples
        3. Sampling Distributions
        4. Properties of Sampling Distributions
        5. Central Limit Theorem
        6. Summary
        7. Estimating Mean using CLT
        8. Confident Interval - Example
        9. Summary
    5. Applications of Sampling Methods
        1. Introduction
        2. Types f Sampling Methods
        3. Uses of Sampling in Market Research
        4. Uses of Sampling in Marketing Campaigns
        5. Uses of Sampling in Pilot Testing
        6. Uses of Sampling in Quality Control
