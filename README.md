# [Lending Club Analysis](https://agiq.github.io/eda/)
Note: Below is a summary of our analysis.  You can find a full write up at my [Github Page](https://agiq.github.io/eda/).
Lending Club is a marketplace for personal loans that matches borrowers who are seeking a loan with investors looking to lend money and make a return.
When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:<br> <br>
1.If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company <br> <br>
2.If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company


## [General Information](https://agiq.github.io/eda/#problem-statement)
- Identifying the risky loan applications by using EDA on the provided dataset
- Data Cleansing
- Data Analysis
- Recommendations

## [Data Cleansing](https://agiq.github.io/eda/#data-cleaning)
- Drop the columns that are empty
- Drop the columns with more than 70% of empty values
- Drop the columns with same value repeated for all rows
- Drop the column that are not needed for this specific analysis e.g., Title, Description, URL etc.,
- Check and Update the right datatype for the column
- Create derived columns from existing columns for example, 'Day' column and 'Month' column from 'Date' column
- Fill the empty values of numerical columns with mean / median values of the column
- Fill the empty values of the categorical columns with mode of the column
- Remove the rows with more than 70% of empty values
- Do the box plot / histogram on all the numerical columns and find out the outliers present in the columns
- Try and keep as much as data and remove the outliers

## [Data Analysis](https://agiq.github.io/eda/#data-analysis)

### [Univariate Analysis](https://agiq.github.io/eda/#univariate-analysis)
Univariate analysis refers to a type of data analysis that looks at data in one variable. So, uni refers to “one”. It does not deal with causes or relationships (unlike regression) and its major purpose is to describe, summarize, and find patterns in the data. In univariate analysis, a variable is just a condition or subset that your data falls into. This is a concept that was developed by the National Weather Service. It provides a single number that represents how likely a particular storm is to occur in any given day, week, month, or year.

We try to find the strongest predictos for all categorical / Numerical variables compared to the target variable.

### [Bivariate Analysis](https://agiq.github.io/eda/#bivariate-analysis)
One of the simplest ways to analyze quantitative data is the bivariate analysis. A correlation study is an empirical research study that examines the relationship between two variables. Statistical analysis is used to determine if there is an association or relationship between the two variables. It determines if there’s a true effect that’s being tested. There are three important factors to consider when conducting a regression analysis. You need to identify the independent variable, the dependent variable, and the model that best fits the data. Bivariate analysis is a simple case of multivariate analysis. In fact, it’s just two variables.

### [Recommendations](https://agiq.github.io/eda/#recommendations)
Based on our analysis, we come up with the following recommendations. This is based on the limited dataset we have. As new data is gathered, we need to reevaluate the model due to both data and model drifting affect.

If the Loan Amount is greater than 20833 and the loan grade is C or D or E or F or G and the applicants salary is less than 34250 then do not approve.

When a new maximum interest rate is introduced in a year, minimize the approval of loan applications in this interest rate so as to minimize the number of loan defaults.

If the Loan grade is B or C or D or E with Interest rate between 5.403 and 7.797, then approve the loan. Do not approve loans with the following conditions:

Applicants reside in WA, VA, SC, NJ, MD, and AZ who request for loan amount of $16,666 and have annual income of $34,250.

Applicants reside in NC who request for loan amount of $20,833 and have annual income of $34,250.
Applicants reside in DC who request for loan amount of $12,500 have annual income of $34,250.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## [Conclusions](https://agiq.github.io/eda/#conclusion)
Making affective decision on when and when not to approve loan applications is paramount to the lending club. We use statistical, univariate, and bivariate analysis to identify strong predictive variables to guide our decision making process. To get there, we need to first load the data, perform exploratory data analysis, clean the data, and handle missing data with imputation or simply drop them if there no or very value from the columns. Next, we perform univariate and bivariate analysis. This includes performing data visualization to help us quickly see our data. This use case does not factor in local governance which includes personal identified information and demographic data that might be considered as “bias”.


## Contact
Created by [@vprasath1902](https://github.com/vprasath1902) & [@agiq](https://github.com/agiq)

Please find more details of this case study in https://agiq.github.io/eda/
