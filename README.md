# German real estate modelling
Project created for *Advanced Econometrics II* (org. *Zaawansowana Ekonometria II*) classes at WNE UW

Language:
 - Polish - classes, report

Semester: III (MA studies)

## About
The main objective of this project was to practice econometric methods learned during classes. We've got 4 parts of the material and we had to perpare 3 models, each from different part. This repo is about second part named cross-sectional data and to be more specific, we estimated quantile regression for deciles 1-9 (5 decile is a median) and compared it to the OLS linear regression (expected value). This project is about house prices in 3 German Lands (North Westphalia, Hesse, Lower Saxony). Data was found on kaggle.com and as its author said, it was scrapped forom german real estate market. Inspiration for this research was found on the literature Caglayan Ebru, Arikan Eban (2011). We estimeated hedonic price model via OLS y~XBeta+epsilon, where y was price (to be more specific its logarithm - we found that it is better way - distribution properties and nice elastic or semi-elastic interpretations), x_i \in X was the regresors vector (matrix when many observations considered at once) and contained variables s.t. log(usable area), log(lot), log(age), #bathrooms (ordinal), #bedrooms (ordinal), heating type (nominal), condition (nominal) and Land (nominal). But OLS is E[y|X], what seems to be not the best idea for real estate modelling, that was the reason why we run quantile regression. Our model was estimated via STATA software with bootstrapped covariance matrix (999 replications). Next we plotted how estimations looks depending on quantile and tested it when it has sense
