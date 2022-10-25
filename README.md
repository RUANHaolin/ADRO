# ADRO

[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

This archive is distributed in association with the [INFORMS Journal on Computing](https://pubsonline.informs.org/journal/ijoc) under the under the [CC BY License](LICENSE).

This repository contains supporting material for the paper [Adjustable Distributionally Robust Optimization with Infinitely Constrained Ambiguity Sets](https://doi.org/????) by H. Ruan, Z. Chen and C. P. Ho.

## Cite

To cite this data, please cite the [research article](https://doi.org/) and the data itself, using the following DOI.

[![DOI](https://zenodo.org/badge/DOI/XX.XXXX/zenodo.XXXXXXX.svg)](https://doi.org/XX.XXXX/zenodo.XXXXXXX)

Below is the BibTex for citing the data.

```
@article{ruan2022adjustable,
  author =      {Ruan, Haolin and Chen, Zhi and Ho, Chin Pang},
  publisher =   {INFORMS Journal on Computing},
  title =       {Adjustable Distributionally Robust Optimization with Infinitely Constrained Ambiguity Sets},
  year =        {2022},
  doi =         {XX.XX/zenodo.XXXXXXX},
  url =         {https://github.com/INFORMSJoC/2022.XXXX},
}  
```

## Content

This repository includes

1. Instance data for the Multi-Item Newsvendor Problem and the Hospital Quota Allocation Problem.
1. Files containing sample results for the Multi-Item Newsvendor Problem, the Hospital Quota Allocation Problem and the Multi-Stage Inventory Control Problem.
<!--1. Files describing the data formats and results.-->

### Data files

Instance data files are located in the folder [data](data), where the random instances generated for the Multi-Item Newsvendor Problem and the Hospital Quota Allocation Problem are stored. 

<!--### Data formats
The folder [formats](formats) contains a [formats.md](formats/formats.md) file that describes the formats of the instance data files of the Multi-Item Newsvendor Problem and the Hospital Quota Allocation Problem.-->


### Results
The folder [results](results) contains the results of the experiments, as well as a [README.md](results/README.md) file that describes the results.


## Data Formats

### Multi-Item Newsvendor Problem

To generate a random instance in the Multi-Item Newsvendor Problem, it is sufficient to generate the four random variables as follows (where the notations are consistent with those in the paper):

1. $\boldsymbol{v}\in\mathbb{R}^{I}$: the unit selling prices of the  items.
1. $\boldsymbol{\mu}\in\mathbb{R}^{I}$: the mean demand.
1. $\boldsymbol{\sigma}\in\mathbb{R}^{I}$: the standard deviation of the demand.
1. $\boldsymbol{\Sigma}\in\mathbb{R}^{I\times I}$: the covariance matrix of the demand.

The instances for different settings are organized in different locations, and the settings are indicated by the folder names along the path; for example, the folder with the path **ADRO/data/newsvendor/table1/11_items/delta025** contains the $100$ instances for the results in Table $1$ in the case of $I=11, \Delta=0.25$, and the one **ADRO/data/newsvendor/table2/07_items** contains the $100$ instances for the results in Table $2$ in the case of $I=7$.


### Hospital Quota Allocation Problem

A random instance in the Hospital Quota Allocation Problem consists of the following data:

1. The number of EAIs
who start hospitalization on day $k$ and staying for at least $l$ days, for all $k\in\mathcal{T}^-$ and $l\in[L]$.
1. The
number of EMIs who stay for at least $l\in[L]$ days starting from day $k\in\mathcal{T}^-$, for all $k\in\mathcal{T}^-$ and $l\in[L]$.

The folders **ADRO/data/hospital/EAIs** and **ADRO/data/hospital/EMIs** store the 50 instances of numbers of EAIs and EMIs, respectively. An instance is stored in the format of a $13\times 16$ table, where the first column is the index of day when the patients start hospitalization and the second column is the day of week (e.g., $3$ for Wednesday, $7$ for Sunday) of this day. The number at the $t$-th column $(t = 3,4,\cdots,16)$ indicates the number of patients that will stay at least $17-t$ days. For example, in the file **ADRO/data/hospital/EAIs/instance03.csv**, the number at the $2$-nd row, $4$-th column means that in our $3$-rd random instance, the number of EAIs that starts hospitalization on day $-12$ and will stay at least $13$ days is $23.29$; while in the file **ADRO/data/hospital/EMIs/instance21.csv**, the number at the $5$-th row, $11$-th column means that in our $21$-st random instance, the number of EMIs that starts hospitalization on day $-9$ and will stay at least $6$ days is $22.93$.




