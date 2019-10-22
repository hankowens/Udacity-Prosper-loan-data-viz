# Assessing inputs and outcomes in the lending process at Prosper
## by Henry Owens


## Dataset


> I started out with data covering 81 columns of variables for over 100,000 loans made by Prosper from November 2005 to March 2014. The majority are loans made to individuals for debt consolodation. Most of the loans are 15000 dollars or less.

> Some of the columns I was interested in (Prosper Rating, debt to income) were not populated in all rows, so after omitting those columns I was left with about 77,000 rows each on a unique loan. 


## Summary of Findings

>The vast majority of people borrow from Prosper to consolidate existing debt.

>Aside from the overwhelming spike at the mode of 36%, the distribution of APR is centered on 20% with moderate right skew.
I got curious about why 36% is so common, and discovered that is the highest APR you can charge for consumer loans in 15 states.
See: "Why 36%? The History, Use, and Purpose of the 36% Interest Rate Cap," Lauren K. Saunders, National Consumer Law Center. https://www.nclc.org/images/pdf/pr-reports/why36pct.pdf

> The most common loan amount for Prosper borrowers is 4000 dollars (pretty small!). 

> It's not obvious that Prosper is doing a signifincantly better job at credit assessment with its special rating than the credit bureaus, since over 10 percent of all bad loans that were charged off had 'AA', 'A,' or 'B' ratings. If the Prosper Ratings had more left skew then you could conclude that they were doing better, but it is hard to say if one is better based on this comparison. But they still do at least as good a job based on my assessment.

> The strongest correlation among numerical variables is the negative relationship between credit score and APR which is intuitive but nontrivial. Higher credit score means lower credit risk and lower interest rate for the borrower.

> Some other relationships I thought would be more pronounced, but do not appear to be here are income to APR and debt-to-income to APR. I guess I thought that DTI was a big factor in the lending decision, meaning that DTI and APR would be more positively correlated. R squared of 0.2 is pretty low though.

> I also thought that the lowest income people usually carried pretty low debt*, but among this population of borrowers, there is a strong relationship the other way. I guess since most borrowers are using their loans for debt consolidation this is a more highly debt burdened sub-population than the wider population.
this is true for student loans, https://www.urban.org/urban-wire/which-households-hold-most-student-debt

> Relationship between APR and Prosper Rating shows clearly that riskier borrowers as measured by Prosper pay higher rates. 

> Prosper Rating and Debt to Income shows a more subtle relationship than I expected. It is there, but there must be many more factors in the rating process. I expected this to be a stronger relationship.

> Low DTI will not prevent Prosper from charging a high rate, but it does seem like a prerequisite for a good Prosper Rating: most of the 'AA' borrowers have DTI below 0.25. But then again so do many of the other borrowers. 


## Key Insights for Presentation

> I was impressed by how closely the Prosper Rating and Credit Scores mapped onto the 'bad' loan groups. The whole business of lending rests on the foundation of credit analysis, and Prosper seems to have come up with a relatively good model in its short-ish existence, compared to the credit bureaus which have been working with FICO scores since the 1970s (I think). 

> I am very curious about what factors go into the ratings after realizing that debt to income is not that instructive on its own. I wish I had more time to look into other potential input variables in the data set that could help reconstruct the Prosper Score.