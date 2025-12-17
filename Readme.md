# Cluster Sampling Design & Optimization Dashboard

## Project Overview
This repository contains an **R Shiny–based Interactive Statistical Tool** designed to demonstrate **Cluster Sampling Design for Population Mean Estimation**.

The application serves as an **educational and analytical dashboard** for understanding cluster sampling methodology. It allows users to compute the **required number of clusters** under specified **precision, cost, and time constraints**, and visually illustrates the cluster selection process.  
This approach is especially useful for geographically dispersed populations or when constructing a complete sampling frame is costly.

## Features

### Sampling Parameters
The dashboard allows users to specify key design inputs:
- Total population size (N)  
- Number of elements per cluster (M)  
- Population standard deviation (σ)  
- Confidence level (z-value)  
- Allowable margin of error (E)  
- Cost per cluster (Cc)  
- Time per cluster (tc)  

### Determination of Number of Clusters
The required number of clusters is calculated as:
n_clusters = ceiling((σ² × N) / (M × E²))

This ensures that the selected sample achieves the desired level of precision while remaining feasible within the population.

### Cluster Selection Procedure
- Clusters are selected using **Simple Random Sampling (SRS)**  
- All units within selected clusters are observed  
- The design corresponds to **one-stage cluster sampling**  

## Operational Constraints

### Cost Analysis
- Cost per cluster (`Cc`)  
- Total survey cost based on selected clusters  

### Time Analysis
- Time required per cluster (`tc`)  
- Total survey time for all selected clusters  

## Outputs

### Required Number of Clusters
Displays the **minimum number of clusters** required to achieve the desired level of precision.

### Cluster Sampling Summary Table
The summary table reports:
- Total number of clusters  
- Number of selected clusters  
- Units per cluster  
- Cost per cluster and total cost  
- Time per cluster and total time  

### Sampling Design Plot
- **Grey points** represent non-selected clusters  
- **Red points** represent selected clusters  

## System Architecture
- **Programming Language:** R  
- **Framework:** Shiny  
- **Visualization:** ggplot2  
- **Interface:** Interactive web-based dashboard  

## Applications
- Large-scale survey implementation  
- Cost-efficient survey planning  
- Teaching and learning sampling techniques  
- Demonstration of cluster sampling methodology  

## Limitations
- Assumes equal cluster sizes  
- Assumes known population standard deviation  
- Does not explicitly account for intra-cluster correlation  
- Non-response is not considered  

## Conclusion
This project provides a simple, interactive, and practical implementation of cluster sampling design. By linking sampling precision with cost and time considerations, the application helps users understand real-world trade-offs in survey planning and enhances conceptual clarity in sampling methodology.

