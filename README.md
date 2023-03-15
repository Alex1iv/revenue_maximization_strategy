# revenue_maximization_strategy


## Content

* [Summary](README.md#Summary)  
* [Project description](README.md#Project-description)  
* [Data and methods](README.md#Data-and-methods)                                
* [Project structure](README.md#Project-structure)                   


---

## Summary
It proposed a marketing strategy aimed on revenue maximization from a direct marketing campaign. The strategy can be \
used as a baseline for campaign budget computation. The strategy algorythm forecasts revenues form product purchases \
and selects the most prospective clients in terms of purchase. It also creates the marketing persona with the most \
significant features for a given product. 
  

## Project description
When a company manager is planning a new marketing campaign, he is interested to do it efficiently: targeting cusomers \
with the highest propensity to the product and decreasing expenditures. In addition, he/she needs to calculate minimum \
budget of the compaign. Form a marketing perspective, it is interesting to identify if any  changes have emergerd in \
client propensities. To fulfull these requirements it is possible to learn from purchases history, for instance, \
whether a client purchased the product or service in the past. 


## Data and methods
For this assignment the data was synthesized from a real dataset from the banking industry and covers from 3 products: \
consumer loans, mutual funds, and credit cards. 

The strategy algorythm is based on pairs of machine learnig models, which are trained on historical purchases of given \
products. In case the purchase rate to the number of clients is low, the algorythm synthetically increases the minority \
class to improve the model quality. The flow diagram below illustrates applied algorythm.

<div style="text-align: center;">
<img src="./figures/scheme.png" width="700">  </div>
<div style="text-align: center;"> Fig.1 - Algorythm flow diagram </div>

Pre-trained models compute expected revenues from purchases of a given product using following equation:

$${Revenue} = max \sum_{i,j=1}^{m,n}P(x_{ij})|_{purchased}*F_{i,j} $$
where:
* $P(x_{ij})|_{purchased}$ - probability that i-th customer will buy j-th product
* $F_{i,j}$ - forecasted revenue from j-th product bought by i-th customer

The mathematical model indicates that proposed marketing strategy is conservative since it prioretises clients by the \
purchase probablility. Therefore, it could be used as a benchmark while budgeting of a new direct marketing campaign. \ 

The most significant features, impacting the product purchase, could be used to compose the marketing persona as shown \
below.

<div style="text-align: center;">
<img src="./figures/fig_5_print.png" width="400">  </div>
<div style="text-align: center;"> Fig.2 - Most significant features example </div>


## Project structure

<details>
  <summary>display project structure </summary>

```Python
revenue_maximization_strategy
├── .gitignore
├── config
│   └── config.json     # configuration setings
├── data                # data archive
│  
├── figures
│   ├── fig_1.png
.....
│   └── fig_13.png
├── models              # models and weights
│   ├── gbr_cc_opt.pkl
.....
│   └── gb_opt_mf.pkl
├── notebooks           # notebooks
│   └── Project.ipynb

├── README.md
├── requirements.txt    
└── utils               # functions and data loaders
    └── reader_config.py
```
</details>