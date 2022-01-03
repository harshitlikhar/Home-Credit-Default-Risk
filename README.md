# Home-Credit-Default-Risk

The course project is based on the Home Credit Default Risk (HCDR) (https://www.kaggle.com/c/home-credit-default-risk/). The objective of Home Credit Default Risk project is to correctly offer loans to individuals who can pay back and turn away those who cannot. In other words, the goal is to predict whether or not a client will repay a loan. In this phase of the project, we will perform analysis and modelling of the Home Credit default risk data currently hosted on Kaggle. The objective of this phase of the project is to perform exploratory data analysis on the data, which includes describing the data, calculating the summary statistics on the data to summarize its main characteristics, visualizing the results, finding missing items count for all the input variables , etc. This step tells us what the data can tell us before we start modeling the data and to perform initial investigations on data so as to discover patterns, to spot irregularities and biases, and to check assumptions with help of summary statistics. The EDA process also involved dropping the columns with the most missing value counts. Subsequently, we built correlation matrix to find and remove highly correlated variables which would render our model inefficient. To avoid any inaccuracy, we Split the dataframe into train and test subsets. Next, we create pipelines to separately impute numerical and categorical values.We use one-hot encoding to transform the categorical variable values. Finally, we have used Logistic Regression and Random Forest to predict our target variable according to our input variables.


<b> Some of the challenges </b>
1. Dataset size
    * (688 meg uncompressed) with millions of rows of data
    * 2.71 Gig of data uncompressed
* Dealing with missing data
* Imbalanced datasets
* Summarizing transaction data


## Home Credit Group
Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities.
While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.

## Background on the dataset
Home Credit is a non-banking financial institution, founded in 1997 in the Czech Republic.
The company operates in 14 countries (including United States, Russia, Kazahstan, Belarus, China, India) and focuses on lending primarily to people with little or no credit history which will either not obtain loans or became victims of untrustworthly lenders.
Home Credit group has over 29 million customers, total assests of 21 billions Euro, over 160 millions loans, with the majority in Asia and and almost half of them in China (as of 19-05-2018).
While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.

## Data files overview
There are 7 different sources of data:
* application_train/application_test: the main training and testing data with information about each loan application at Home Credit. Every loan has its own row and is identified by the feature SK_ID_CURR. The training application data comes with the TARGET indicating 0: the loan was repaid or 1: the loan was not repaid. The target variable defines if the client had payment difficulties meaning he/she had late payment more than X days on at least one of the first Y installments of the loan. Such case is marked as 1 while other all other cases as 0.
* bureau: data concerning client's previous credits from other financial institutions. Each previous credit has its own row in bureau, but one loan in the application data can have multiple previous credits.
* bureau_balance: monthly data about the previous credits in bureau. Each row is one month of a previous credit, and a single previous credit can have multiple rows, one for each month of the credit length.
* previous_application: previous applications for loans at Home Credit of clients who have loans in the application data. Each current loan in the application data can have multiple previous loans. Each previous application has one row and is identified by the feature SK_ID_PREV.
* POS_CASH_BALANCE: monthly data about previous point of sale or cash loans clients have had with Home Credit. Each row is one month of a previous point of sale or cash loan, and a single previous loan can have many rows.
* credit_card_balance: monthly data about previous credit cards clients have had with Home Credit. Each row is one month of a credit card balance, and a single credit card can have many rows.
* installments_payment: payment history for previous loans at Home Credit. There is one row for every made payment and one row for every missed payment.
