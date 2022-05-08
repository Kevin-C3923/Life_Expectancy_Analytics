
### Selected Topic:
Longevity, and influencing factors, in New York State

### Reason For Topic Selection:
[to be inserted]

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

### Communications Protocols:
The team for consists of four members, each with a designated role:

* Kevin Camarillo (Square)
* Krystal Cheng (Circle)
* Silvania Roche (Triangle)
* Christopher Ryan (X)

_*Duties of each role are as follows:*_

**Square:** The team member in the square role will be responsible for the repository

**Triangle:** The member in the triangle role will create a mockup of a machine learning model. This can even be a diagram that explains how it will work concurrently with the rest of the project steps.

**Circle:** The member in the circle role will create a mockup of a database with a set of sample data, or even fabricated data. This will ensure the database will work seamlessly with the rest of the project.

**X:** The member in the X role will decide which technologies will be used for each step of the project.
 
The group shall meet each Monday and Wednesday during class hours with an additional meeting at 12 p.m. each Saturday. There shall be continuous communication within the dedicated slack channel and additional zoom meetings shall be scheduled as required.

### Machine Learning Model:

Our machine learning model will help us find strong or weak correlation to lifespan.Since our datasets are labeled and we are looking for a linear regression correlation we will use a supervised machine learning model and or a deep learning.It is expected to use the SciKit-Learn library for this model,however this aspect is pending final design. For this analysis we will look data from 2011 to 2022. Data will be group by NYS counties. We will create multiple data frames with Pandas to extract the only needed features for this analysis.

**Output label:** 

- No. of death in each NYS county 

**Input labels:** 

- % Fair or Poor Health; 
- % Low birthweight; 
- Food Environment Index; 
- No. Driving Deaths;
- No. Uninsured; 
- Mental Health Provider Ratio

_*See Figure 1 for full technology flow*_

### Database

The new dataset wil be generated the original dataset with the specific characteristic, which will be used to create a databased in PostgreSQL and hosted in Amazon Web Services.  PG Admin shall be used for editing and connection to the DB. 

![SchemaUpdated](/resource/SchemaUpdated.png)

