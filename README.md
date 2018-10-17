# reskill-at-dnb
Reskill at DNB in Norway
The project is a part of the ReSkillData Science Initiative at DNB.

I chose to use a subset of the Walmart data sets on stores and sales avalable at Kaggle;

Stores.csv - store data for all Walnmart stores
Features.csv - store descriptions (type, category etc)
Train.csv - mainly weekly sales at the stores over a timespan, with additional data (CPI, unemployment rate etc)

Libraries used, as shown by imports :
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import confusion_matrix, accuracy_score
import matplotlib.image as mpimg
from matplotlib import pyplot as PLT
from sklearn import preprocessing as p
from sklearn.cluster import KMeans
from sklearn.datasets.samples_generator import make_blobs
%matplotlib inline


My intention was to apply Unsupervised leaning skills on the data to find out if these could be of use to identify clustering patterns relevant for business questions. Specifically I used StandardScaler, pca analysis for component reduction and KMEans for clustering.
The Notebook contaons code for cleaning, modeling , joining data and then applying pca and kmeans clustering transformations. 

RESULTS
I omitted some columns and recioded date information for simplicity. The 3 datasets were joined to one.
Pca method identifyed 7 as a good value for reduction for next step. The Kmeans method showed 7 clusters as a good choice for clustering. Finally I retreieved the results and used these for evaluating the clusters. See resukts below for details.
Clusteirng was useful for handlng the data, but with my choices of data prep I did not obtain any completely unforeseen correletions. Store size is impiortant for sales, as is store type. Unemployment rates correlates with lower sales, and it seems higher temperatures do, too - maybe indicating lower financial level in southern areas. Fuel prices did not seem to have any impact.

The data is presented in a short Blog on Medium. 



The files used for the project are all here; datasets, ipynb and a html version of the Notebook 
Note that the project has been revised after feedback, the newest and final version is named with _V2



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
                

                
                
               
