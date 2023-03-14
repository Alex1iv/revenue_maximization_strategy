# revenue_maximization_strategy


## Content

* [Summary](README.md#Summary)  
* [Project description](README.md#Project-description)  
* [Data and methods](README.md#Data-and-methods)                                
* [Project structure](README.md#Project-structure)                   


---

## Summary
It was developed revenue maximization strategy aimed at revenue maximization. The strategy is based on machine learning learning models. Every model was tailored to predict purchase as well as expected revenue from 3 products: consumer loans, mutual funds, and credit cards.

## Project description

## Data and methods

The solution flow diagram is shown below
<p align="center"> 
<img src="./figures/Scheme.png" width="800"> </p>


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