# reskill-at-dnb
Reskill at DNB in Norway
The project is a part of the ReSkillData Science Initiative at DNB.

I chose to use a subset of the Walmart data sets on stores and sales avalable at Kaggle;

Stores.csv - store data for all Walnmart stores
Features.csv - store descriptions (type, category etc)
Train.csv - mainly weekly sales at the stores over a timespan, with additional data (CPI, unemployment rate etc)

My intention was to apply Unsupervised leaning skills on the data to find out if these could be of use to identify clustering patterns relevant for business questions. 

The data is presented in a short Blog on Medium. 
...................................................................

The files used for the project are all here; datasets, ipynb and a html version of the Notebook 
..................................................................
Answering my initial Business questions:
1) Can Unsupervised Learning methods be used for clustering data from the Kaggle Walmart dataset? (The dataset is originally posted for predicting sales, using time dimensions and other techniques)
- Answer : Yes, the data can be used with Unsupervised Learning methods, 
    but it requires several choices and data cleaning/changing.  

2) Can I by using the pca method reduce dimensions on this dataset with acceptable results, and will I be able to establish clear and sensible clusters for the dataset, to provide basis for business analysis?
- Answer : Yes, the data (after transformation) shows that dimensions can be reduced and clusters established.
    If ha had spent more time polishing the data I think the value could be even better for these purposes 

3) Do the clusters provide me with valuable insight about the Walmart stores by grouping them differently than we do by only using geography and store size?
- Answer : Not so sure. The clusters clearly lean on the store types and sizes and their coreelation with weekly sales,
    which is not an eye-opener, I assume.

    I did see some correlation with Unemployment rates and (weakly) on temperature, which makes me curious as to the
    coonnection with geographical differences and related sociodemographical info where the stores reside. 

4) Can we identify variables that have a significant impact on the stores with outstanding high or low weekly sales?
- Answer : Yes, we can see from the clusters that 
                - stores with low weekly sales are the smallest stores, type C, in areas with high unemployment rates
                - stores with high weekly sales are large stores of type A with low unemployment areas. 
                 - genarally, the high-weekly-sale stores are in areas with lwoer temperatures, indicating northern areas
                
.......................................................................................................
                
                
               
