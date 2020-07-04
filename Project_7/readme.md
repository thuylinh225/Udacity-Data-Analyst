# Loan Data from Prosper Exploration

## Dataset

This document explores a dataset containing 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, borrower employment status, borrower credit history, and the latest payment information.

## Summary of Findings

- Borrower APR is the Borrower's Annual Percentage Rate (APR) for the loan. The distribution of APR looks multimodal, with a lot of borrowers on the borrower APR from 0.1-0.3, and few on the high borrower APR end (over 0.4). A small peak centered at 0.1, a large peak centered at 0.2. There is also a small peak centered 0.3. Additionally, there is a very shape peak between 0.35 and 0.36.
- Loan Original Amount is the origination amount of the loan. The most popular Original Loan Amount are below 26k, especially there are some Original Loan Amounts that many borrowers chose such as below 5k, 10k, 15k, 20k, 25k. There are not too much original loan amounts over 26k.
- Stated Monthly Income has a long-tailed distribution, with a lot of borrowers have the low stated monthly income end, and few on the high stated monthly income end. When plotted on a log-scale, the Stated Monthly Income distribution looks with the peak between $4,000-$6,000.
- Income range is the income range of the borrower at the time the listing was created. The income range of the borrowers in the dataset is generally in range $25,000-49,999 and $50,000-74,999 , with most of them are employed and full-time. The most popular prosper rating (alpha) of borrowers is C, there is little the number of borrowers who has the prosper rating (alpha) is AA.
- Term is the length of the loan expressed in months. There are three kinds of term and the most popular term is 36 months, the least term is 12 months.
- Stated Monthly Income is the monthly income the borrower stated at the time the listing was created. Borrowers with better rating also have larger stated monthly income and loan original amount.

In the exploration, I found that the borrower APR is:
	+ negatively correlated with original loan amount: At different size of the loan amount, the APR has a large range, but the range of APR decrease with the increase of loan amount.
	+ negatively correlated with prosper rating (alpha): The borrower APR also decreases with the increasingly better prosper rating. Borrowers with the best Prosper ratings have the lowest APR. It means that the Prosper rating has a strong effect on borrower APR. Interestingly, the relationship between borrower APR and loan amount turns from negative to slightly positive when the Prosper ratings are increased from HR to A or better. This is may because people with A or AA ratings tend to borrow more money, increasting APR could prevent them borrow even more and maximize the profit. But people with lower ratings tend to borrow less money, decreasing APR could encourage them to borrow more.
	+ negatively correlated with borrow term: the borrower APR decrease with the increase of borrow term for people with HR-C raings. But for people with B-AA ratings, the APR increase with the increase of borrow term.
	
## Key Insights for Presentation

For the presentation, I just focus on features that could affect the borrower APR, which are original loan amount, Prosper rating, Borrow Term. I started by showing the distribution of borrower APR and loan amount variable. Then, I showed the relationship between Borrower APR vs. loan original amount, as well as Borrower APR vs. prosper rating (alpha). I also explored how the three categorical variables play into the relationship between borrower APR and Loan Amount. After that, I found how Borrower APR was by Prosper Rating and Term, as well as how Loan Original Amount was by Prosper Rating and Term. I also investigated the effect of Income Range on relationship between Borrower APR and Term, as well as the effect of Prosper Rating on Relationship between Borrower APR and Term.