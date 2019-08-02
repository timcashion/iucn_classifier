# iucn_classifier
Prediction and classification of species to IUCN status. 


**Disclaimer: This analysis has not been peer-reviewed and is not meant to replace the process of species assessment and prioritization undertaken by the IUCN Red List.**

An analysis to aid in predicted classification and thus triage of IUCN Red List species currently 'Not Evalauted' or 'Data Deficient'. 

Problem Description: 
The rate of extinction at present is high above historical levels. Conservation has limited resources to allocate to both the assessment of species and their protection. The main international organization that evaluates the population status of species is the IUCN. They assess species into several categories of risk, and a category of 'Data Deficient' when there is not enough information to judge the risk status of a species. 

![IUCN_Categories](../images/iucn_categories.png)

Data sources:  
IUCN API - Current Threat Status, taxonomy, max depth, habitat type, threats, etc.   
https://apiv3.iucnredlist.org/api/v3/docs
Fishbase - Length Data, Price category, Vulnerability Index, habitat range? Age at sexual maturity? Max Age?   
www.fishbase.org
Aquamaps - Area size (sum of cell area where occurence is predicted)  
www.aquamaps.org 

Proposed Solution: 
To properly allocate resources for conservation we need to know which species are most threatened. Species classified as 'Data Deficient' could be of high concern (e.g., Threatened) or they could be of a low prioirty (Least Concern or Near Threatened). An improvement to this process would be to predict which species are most likely of high conservation concern within the Data Deficient category as well as of species not assessed by the IUCN at present. 

After some review, I believe it is more important not to predict the exact species category, but to predict whether the species is likely to be 'Threatened' (e.g., Vulnerable, Endangered, or Critically Endangered), or of a lesser concern ('Not Threatened', i.e., Least Concern or Near Threatened). 

Therefore, I am to train a machine learning or statistical model on available data that will predict the IUCN category or their general level of cosnervation concern of species currently listed as Data Deficient or species not currently included on the IUCN Red List. 

Based on my current knowledge, I begin with a focus on aquatic species, and especially fishes. 

ML Methods:
Logarithmic regression, Decision Tree, Random Forest, Naive Bayes, kNN
I can attempt these with regression based on a linear-scoring method of the IUCN status (0-1), or on a more classical classificaiton on the threat categories, or large over-arching categories (Not Threatened vs. Threatened). 

