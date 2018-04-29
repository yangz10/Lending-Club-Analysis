# Lending Club Exploratory Analysis 

## 1.0 Perspective

Individual loans always been used to predict whether a certain loan will default and then calculate the **default rate**. According to the exposure, people can use all these data to estimate final net loss. Moreover, people can estimate certain losses under different scenarios - stress testing. This is a typical perspective from risk management - internal perspective.

**However**, one unique perspective is from competitor’s perspective. As major competitors of  Lending club, banks have natural advantages like security. As a consequence, I come up with the first question. 

## 2.0 Start From A Question

**Why people choose Lending Club rather than large banks when they apply for personal loans?**

[**Figure 1**] (https://www.lendingclub.com/info/statistics.action) : Data Overview

![](./images/overview.png)
From Lending Club Official Website

Considering low interest rate and loan purposes in Figure 1.0, I guess different  customer clusters may have different objectives:

- High Credit Score Applicants : Use low interest rate to **refinance** current loan or debt - debt consolidation. 
- Low Credit Score Applicants : Achieve short-term **consumption** objective or pay old loans (short-term liquidity).

High credit score applicants have good credit records and are willing to reduce current finance cost. Low credit score applicants generally have bad credit records and want to solve current liquidity problem.

### Objective :
Find insights about whether high credit score applicants do not choose large banks.

## 3.0 Data Explore


- Data Source : https://www.lendingclub.com/info/download-data.action 
- Time Period : 2017 Quarter 4
- Priority : High Score Applicants 

### 3.1 Home Improvement and Ownership

At first, I segment the whole dataset based on FICO score to test my original thought and better understand current data. FICO scores are split into intervals  (width 10).

**Figure 2** : FICO Bin's Purpose

![](./images/FICO_Purpose.png)

From Figure 2, my initial gusess is only partly correct. Although debt consolidation indeed is a main reason for borrowing, high score applicants concern more about home improvement. 

As a result, I check home ownership of each FICO bin using similar methods.

**Figure 3** : FICO Bin's House Ownership

![](./images/FICO_House.png)

#### New Guess :

High score applicants with mortgage loans want to improve their house. However, mortgage loans actually affect applicants' evaluating "scores". For example, people with mortage loans may have a high debt to income ratio. So, these factors set barriers for these applicants.  

### 3.2 Debt Consolidation 

High score applicants who want to consolidate their debt are very sensitive to interest rate. So, I first do research on what actually influence the interest rate.

**Figure 4** : Interest Rate For Each Grade

![](./images/Grade_int.png)

According to the Lending Club's prospectus, applicants will receive the pre-defined loan term and interest rate after Lending Club assessing their credit situation, and then pick up one. That is to say, even if applicants want to refinance their previous debts, this interest rate also should be lowerer than interest rate of previous debt.

From Figure 4, each loan's interest rate is determined by final grade evaluated by Lending Club. So, Grade is very important if we want to figure out the refinancing problem. Moreover, reasearch about grading algorithem actually helps us understand Lending Club's business model.


### 3.3 Advanced Exlorration About Grade

Driven by previous research, I check the relationship between FICO score and grade. From Figure 5, not all high FICO score applicant's loan can be graded by high loan grade.

**Figure 5** : FICO Bin and Grade

![](./images/Grade_FICO.png) 

To figure out more factors affecting grades, I check other variables. In Figure 6, different loan purpose may affect final grading, especially for different FIFO groups.  

**Figure 6** : Grade Bin and Purchase

![](./images/Grade_Purpose.png) 

**Figure 7** : Debt to Income 

![](./images/DTI.png) 




#### Next Step :

To better undersand current 



 
