# Canonical Correlation Analysis of a real-world problem

### 1. Introduction
Canonical Correlation Analysis (CCA) is a powerful statistical technique that is used to measure the linear relationship between two multivariate sets. By identifying linear combinations within each set that are maximally correlated with each other while being orthogonal to the linear combinations in the other set, CCA provides insights into hidden connections and dependencies. Widely used in various disciplines, CCA is a valuable tool for uncovering intricate patterns and associations within complex datasets. Canonical correlation analysis allows us to summarize the relationships in to lesser number of statistics while preserving the main facets of relationships. So, Canonical correlation analysis also a dimension reduction technique.

### 2. Methodology

#### 2.1 Dataset Description
Body performance Data
This is data that confirmed the grade of performance with age and some exercise performance data. This data is collected by Korean Sports promotion Foundation.
source: Kaggle
link: https://www.kaggle.com/datasets/kukuroo3/body-performance-data

##### 2.2.1 Variable Description
- age – Age of an individual (in years [20 – 64])
- gender - Gender of an individual (F, M)
- height_cm – Height of an individual (in cm)
- weight_kg - Weight of an individual (in kg)
- body fat_% - Body fat percentage of an individual
- diastolic - diastolic blood pressure of an individual (min)
- systolic - systolic blood pressure of an individual (min)
- gripForce - exercise 1
- sit and bend forward_cm - exercise 2
- sit-ups counts - exercise 3
- broad jump_cm – exercise 4
- class : A,B,C,D ( A: best) / stratified

### 2.2 Key Steps
- STEP 1: Data Preprocessing
    - In this step we import the data set, look for the types and structure of the data, handle the missing values and find summary details about the dataset.
    - And also we partition data in to two sets in this step.
    - Four physiological and Four exercise variables are partitioned in to two sets.
        - Physiological variables (Y) : Age , Height , Weight , Body fat percentage
        - Exercise variables (X) : Grip Force, Sit and bend forward , Sit-ups , Broad jump
    - Standardizing the data.
- STEP 2: Multivariate Normality Assumption Checking
    - In this step we check the multivariate normality assumption and univariate variable normality of each variable using mardia’s test and Henze-Zirkler's test.
- STEP 3: Perform Canonical Correlation
    - In this step we perform canonical correlation using R statistical software.
- STEP 4: Obtain Normalized Canonical Correlations
    - Canonical variates are normalized to have Var(U) = 1 and Var(V) = 1.
- STEP 5: Test the Significance of Canonical Correlations
    - In this step we calculate p-values using the F-approximations of different test statistics such as ‘Wilks’, ‘Hotelling’, ‘Pillai’ and ‘Roy’ and find significant canonical correlations.
    - Plot the significant canonical correlations.
- STEP 6: Find the Canonical Loadings Matrix
    - In this step we find the potential coefficients on the canonical linear relationships.
- STEP 7: Find the Canonical Variates