# Life_Expectancy_Analytics

### Selected Topic:
Longevity, and influencing factors, in New York State

### Question for this analysis:
Which of the investigated factors, exhibit the greatest influence on longevity, on a county basis ?


### Reason For Topic Selection:
The topic for this analysis was an interesting one to apply a machine learning model to investigate clustering and corelated factors that affect lifespan in different areas.

### Data Source Description:
Data was sourced from this location:
https://www.countyhealthrankings.org/app/new-york/2022/downloads

The dataset contains data for each county in New York State, and provides annual data for a variety of factors linked to longevity (e.g. obesity rate, food environment index etc..). Datasets are available from 2011 to 2022,

Of the listed data, the following variables are to be analyzed:

* Deaths 	
* % Poor Health 
* % Low Birthweight 
* Food Environment Index 
* Number of Driving Deaths 
* Number of Uninsured People 
* Mental Health Provider Ratio 


### Question We Hope To Answer With The Data:
The above items shall be analyzed, across the New York State dataset, to determine if these factors are correlate to the YPLL figures (Years Potential Life Lost).


_*Duties of each role are as follows:*_

**Square:** The team member in the square role will be responsible for the repository

**Triangle:** The member in the triangle role will create a mockup of a machine learning model. This can even be a diagram that explains how it will work concurrently with the rest of the project steps.

**Circle:** The member in the circle role will create a mockup of a database with a set of sample data, or even fabricated data. This will ensure the database will work seamlessly with the rest of the project.

**X:** The member in the X role will decide which technologies will be used for each step of the project.
 
The group shall meet each Monday and Wednesday during class hours with an additional meeting at 12 p.m. each Saturday. There shall be continuous communication within the dedicated slack channel and additional zoom meetings shall be scheduled as required.

### Data Exploration Phase:
A variety of machine learning models were tested against the available data to assess the best model fit.
Supervised Learning and Unsupervised Learning were both explored as candidates; the final selection and classification was completed using Primary Component Analysis and Hierarchical Clustering

### Machine Learning Model:
#### Pre-processing Data
* For our data pre-processing we had to do some cleaning before using in any ML model so it could run without error. We first join all the data collected from the web into one CSV file and then clean up the columns and rows with null or zero values. Finally we grouped data by county and took the mean to then scale out the data.

#### Feature engineering and Selection
* Our preliminary feature are the factors that may affect a premature deaths, we want to find out which of the features (factors) has a higher effect on the cause of premature deaths. The data collected broke down by NYS county's, we were curious to analyze which feature had a stronger correlation with the death rate. We wanted to analyze over the years but data would not work well with any machine learning models. We applied a linear and logistic regression model,that didn't not give us much information about the data and the accuracy on the model was 0%. After applying the LR model we grouped the data by county with the mean, then scaled data points to ratios. We then ran a PCA and applied the K-mean model.

#### Spliting and Training data
* For the our ML model selection the linear regression didnt call for a split. When we applied a Logistic regression model we applied a split  by making "X: Food environment index"" and "y: death total." We stratified the data to 60 training 40 test.

#### Machine Learning Model Decision
* We originally thought the linear regression model would work with our data set but it didn't work well with out data. There was no correlation or patterns observed with this model. The data point were all scattered and the linear regression was almost flat for all input labels. This led us to applied a PCA and then do a K-mean model to instead cluster our data point for each feature. After applying this model we did observed patterns among our data points.

* When we reference our question "Which of the investigated factors, exhibit the greatest influence on longevity, on a county basis ?" the ML model does indeed answer it. We can see per county which of the factors affects the most on the death ratio.


**Output fearture:** 
- death ratio

**Input features:** 
- Fair or Poor Health %; 
- Low birthweight %; 
- Food Environment Index; 
- Driving Deaths ratio;
- Uninsured ratio; 
- Mental Health Provider ratio



### Database

After cleaning and merging the County Health Ranking of NY from past 10 years on Jupyter Notebook, we used the data to calculate the ratios as comparing the health factors to the census population of 2020. These dataset and tables are stored on PostgreSQL and connected with Machine Learning model via SQLAlchemy.

![Life_Expectancy_ERD.png](/database/Life_Expectancy_ERD.png)

![health_factors.png](/database/health_factors.png)

![Census_Population.png](/database/Census_Population.png)

![pop_factors_ratio.png](/database/pop_factors_ratio.png)

![Combined_census_ratios_table.png](/database/Combined_census_ratios_table.png)


### Dashboard and Visualizations:

Tableau shall be used for visualizations, this may be used in a standalone manner or embedded in a webpage, pending final design. This may read from the DB or via results files generated.

Additionally, excel may be used for initial data exploration

### Technology Flow:

![Figure 1](https://github.com/Kevin-C3923/Life_Expectancy_Analytics/blob/main/resource/fig1.png)

**_Figure 1_:** Technology Flow.


### Dashboard

Dashboard visuals will be provided by Tableau, final presenetation will be via google slides.

The google slides early draft presentation is located at below link. This is an early draft, and will be completed in coming weeks.

[Google Slides](https://docs.google.com/presentation/d/1FHdNYXm0XzGTU72ifNadUf7fz4tBam6r3sGRI6Vt-FI/edit?usp=sharing)


The Visualizations from Tableau are located at this link:
[Tableau Visualizations] (https://public.tableau.com/app/profile/christopher.ryan4533/viz/ML_VIZ_Week3_Story/Story1?publish=yes)


