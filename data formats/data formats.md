## Data Formats

### Multi-Item Newsvendor Problem

To generate a random instance in the newsvendor problem, it is sufficient to generate the four random variables as follows (where the notations are consistent with those in the paper):

1. $\boldsymbol{v}\in\mathbb{R}^{I\times 1}$: the unit selling prices of the  items.
1. $\boldsymbol{\mu}\in\mathbb{R}^{I\times 1}$: the mean demand.
1. $\boldsymbol{\sigma}\in\mathbb{R}^{I\times 1}$: the standard deviation of the demand.
1. $\boldsymbol{\Sigma}\in\mathbb{R}^{I\times I}$: the covariance matrix of the demand.

The files "v.xlsx", "mu.xlsx", "sd.xlsx" and "comat.xlsx" store the 100 instances of $\boldsymbol{v}$, $\boldsymbol{\mu}$, $\boldsymbol{\sigma}$ and $\boldsymbol{\Sigma}$, respectively. For example, the folder [delta000](ADRO/data/Newsvendor/Table 1/11 items/delta000) contains these four files for the results in Table 1 in the case of $I=11, \Delta=0$.


## Content

This repository includes

1. Instance data for the Multi-Item Newsvendor Problem and the Hospital Quota Allocation Problem.
1. Files containing sample results for the Multi-Item Newsvendor Problem, the Hospital Quota Allocation Problem and the Multi-Stage Inventory Control Problem.
1. Files describing the data format and results.

### Data files

Instance data files are located in the folder [data](data). 

### Data format
The folder [data formats](data formats) contains a .md file [newsvendor.md](data formats/newsvendor.md) that describes the format of the instance data files of the Multi-Item Newsvendor Problem, and a .md file [hospital.md](data formats/hospital.md) for the Hospital Quota Allocation Problem.

