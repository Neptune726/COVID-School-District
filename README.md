# COVID-School-District
## Overview
This repository is a statistical analysis of the impact of school district reopening methods on COVID Cases.

The data for used in this analysis was collected from numerous sources:

COVID Case data was downloaded from the Johns Hopkins CSSE COVID-19 Github Data Repository.

Information about how each of the school districts opens was downloaded from MCH Data.

Information about the population of each county was downloaded from the US Census.

Information about in which county each school district is located was scrapped from the US department for education. 

Most School districts choose to open reopen in one of three methods:
- Online Only, 2,827 school districts chose to do this approach.
- Hybrid, where students spend half their time learning in person and the other half learning online, 6,363 school districts chose to do this approach.
- In Person, where all the students go to school in person, 2,125 school districts chose to do this approach.
There are also 981 school districts whose open in another method or whose opening method is unknown. 

The number of school districts in each county and the number of students in each school district varies wildly, so I created a statistic called Total Students In Person (TSIP), for a county, its TSIP is defined as:

![equation](https://latex.codecogs.com/gif.latex?TSIP%3D%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%20w_%7Bi%7D%5Ccdot%20E_%7Bi%7D)

Where ![equation](https://latex.codecogs.com/gif.latex?E_%7Bi%7D) is the number of students enrolled in the ith school district in the county and ![equation](https://latex.codecogs.com/gif.latex?w_%7Bi%7D) is a weighting factor, that depends on the method which this school district is teaching its fall classes:
- if the school district teaches its classes entirely online, ![equation](https://latex.codecogs.com/gif.latex?w_%7Bi%7D%3D0).
- if the school district teaches its classes through a hybrid method ![equation](https://latex.codecogs.com/gif.latex?w_%7Bi%7D%3D0.5).
- if the school district teaches its classes entirely in person, ![equation](https://latex.codecogs.com/gif.latex?w_%7Bi%7D%3D1).

