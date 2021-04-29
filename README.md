# German real estate modelling
Project created for *Advanced Econometrics II* (org. *Zaawansowana Ekonometria II*) classes at WNE UW

Language:
 - Polish - classes, report

Semester: III (MA studies)

## About
The main objective of this project was to practice econometric methods learned during classes. We've got 4 parts of the material and we had to perpare 3 models, each from different part. This repo is about second part named cross-sectional data and to be more specific, we estimated quantile regression for deciles 1-9 (5 decile is a median) and compared it to the OLS linear regression (expected value). This project is about house prices in 3 German Lands (North Westphalia, Hesse, Lower Saxony). Data was found on kaggle.com and as its author said, it was scrapped forom german real estate market. Inspiration for this research was found on the literature (Caglayan Ebru, Arikan Eban, 2011). We estimeated hedonic price model via OLS y~XBeta+epsilon, where y was price (to be more specific its logarithm - we found that it is better way - distribution properties and nice elastic or semi-elastic interpretations), x_i \in X was the regresors vector (matrix when many observations considered at once) and contained variables s.t. log(usable area), log(lot), log(age), #bathrooms (ordinal), #bedrooms (ordinal), heating type (nominal), condition (nominal) has garage (binary) and Land (nominal). But OLS is E[y|X], what seems to be not the best idea for real estate modelling, we also tested OLS model for homoscedasticity, residuals normality and outliers (via Cook's distance, standarized residuals and leverage) and we found that OLS assumptions was not met, that was the reason why we ran quantile regressions. Our models was estimated using STATA software with bootstrapped covariance matrix (999 replications). Next we plotted how estimations looks depending on quantile and tested it when it has sense.

Findings:
 - real estate characteristics are conditional dependend on price distribution => quantile regression was a good guess
 - Hesse is the most expensive Land among considered ones
 - higher quantiles => lower negative impact of age on the price
 - lot has nonlinear positive impact on price (middle class cares the least)
 - and more (can be found in the report :) I encourage you to read it, I like it a lot)

In this project I learnt more about econometric modelling and saw the power of quantile regression - really awesome model

## Repository description
 - Kuzma_Odziemczyk_minimodel_2.pdf - project report

## Technologies
 - STATA (quantile regressions and tests)
 - R (Plots, OLS, tests)
 - Python (data cleaning, analysis and preprocessing)
 - LaTeX (report)

## Authors
Bartek Kuźma
Maciej Odziemczyk

## Notes
Our analysis was performed using many softwares (Python, R, STATA), but we needed to send report only as an assignment thats why whe had not prepared good quality notebook with code
