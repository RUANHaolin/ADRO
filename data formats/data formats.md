## Data Formats

### Multi-Item Newsvendor Problem

To generate a random instance in the Multi-Item Newsvendor Problem, it is sufficient to generate the four random variables as follows (where the notations are consistent with those in the paper):

1. $\boldsymbol{v}\in\mathbb{R}^{I}$: the unit selling prices of the  items.
1. $\boldsymbol{\mu}\in\mathbb{R}^{I}$: the mean demand.
1. $\boldsymbol{\sigma}\in\mathbb{R}^{I}$: the standard deviation of the demand.
1. $\boldsymbol{\Sigma}\in\mathbb{R}^{I\times I}$: the covariance matrix of the demand.

The files "v.xlsx", "mu.xlsx", "sd.xlsx" and "comat.xlsx" store the 100 instances of $\boldsymbol{v}$, $\boldsymbol{\mu}$, $\boldsymbol{\sigma}$ and $\boldsymbol{\Sigma}$, respectively. The instances for different settings are organized in different locations, and the settings are indicated by the folder names along the path; for example, the folder with the path "ADRO/data/Newsvendor/Table 1/11 items/delta025" contains these instances for the results in Table 1 in the case of $I=11, \Delta=0.25$, and the one "ADRO/data/Newsvendor/Table 2/7 items" contains the instances for the results in Table 2 in the case of $I=7$ (for both the continuous decision panel and the discrete decision panel).


### Hospital Quota Allocation Problem

A random instance in the Hospital Quota Allocation Problem consists of the following data:

1. $z_{k,l}, k \in \mathcal{T}^-, l\in[L]$: the number of EAIs
who start hospitalization on day $k$ and staying for at least $l$ days.
1. $\xi_{k,l}, k \in \mathcal{T}^-, l\in[L]$: the
number of EMIs who stay for at least $l$ days starting from day $k$.

The files "EAIs.xlsx" and "EMIs.xlsx" in "ADRO/data/Hospital" store the 50 instances of $z_{k,l}$ and $\xi_{k,l}, k \in \mathcal{T}^-, l\in[L]$, respectively. An instance is stored in the format of a $13\times 16$ table, where the first column is the index of day when the patients start hospitalization, the second column is the day of week (e.g., 3 for Wednesday, 7 for Sunday) of this day. The data at the $t$-th column $(t \in \{3,4,\cdots,16\})$ indicate the number of patients that will stay at least $17-t$ days. For example, in the sheet "Instance1" of the "EAIs.xlsx" file, the number at the $2$-nd row, $4$-th column means that in our first random instance, the number of EAIs that starts hospitalization on day $-12$ and will stay at least 13 days is 23.75. 




