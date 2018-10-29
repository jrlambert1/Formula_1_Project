# Formula 1 Project

<img width="622" alt="screen shot 2018-10-16 at 1 47 18 pm" src="https://user-images.githubusercontent.com/34430819/47047205-cef95800-d14b-11e8-9e3f-532e9c6c61fb.png">

## James Lambert

## Predicting and Analyzing Race Results During a F1 Season

**Goal:** The primary goal of this project was to predict a Formula 1 race winner from that season's team and driver stats.  The ultimate ambition for this project is to use a predictive model as a starting point for insight as to racer and team success to provide a foundational foundation as to how well a team/driver will do based on those metrics.

## Define the Question

Are we able to predict which team and individual racer wins a Formula 1 race based on team statistics, and the racers past success?

## Supplementary background and interest in this Sport 

Formula 1 is broken down into two championships: a team championship where two drivers on the same team compete and pool one another's points together for the team.  The latter is an individual championship in which each driver is fighting for themselves.  

## So why is determining these two-metrics important?
1.  It can provide an estimate of which team and driver has the potential to win the championship at the end of the year.
2.  You could bet on it in a betting platform if you believe in your model
3.  I have a passion for the sport and wanted to dive more in the data for some new insight and knowledge to further my    interests involving the sport
  
## Data Gathering
The data was gathered from a project [on Kaggle](< https://www.kaggle.com/cjgdev/formula-1-race-data-19502017> ).

In addition, I researched what teams spend in a year and created a probability column indicating the likelihood of winning a race depending on the amount of money they spend in a year.

The following teams have a higher percentage of winning due to yearly budgetary expenses:
1. Ferrari
2. Red Bull
3. Mercedes AMG

<img width="385" alt="screen shot 2018-10-25 at 4 30 49 pm" src="https://user-images.githubusercontent.com/34430819/47536133-6dd03380-d873-11e8-9320-da39801c7965.png"> 

<img width="350" alt="screen shot 2018-10-26 at 11 06 58 am" src="https://user-images.githubusercontent.com/34430819/47584667-0ae0aa00-d910-11e8-8b73-adbdb95838d4.png">

<img width="188" alt="screen shot 2018-10-26 at 11 06 40 am" src="https://user-images.githubusercontent.com/34430819/47584820-86425b80-d910-11e8-9c97-f9d842aa14ce.png">

I didn't include McLaren or Renault into this calculation based on their lack of success in recent years.  
  
**Note:** The Reason I chose the 1991 season and onward as my training example is due to:

1. 1991 was Michael Schumacher's rookie season and the most winningest driver of all time in Formula 1

In the end the data looked like:
1. 1991 - 2016 as the training dataset
2. 2017 as the testing dataset
3. Numerous Engineered features(ex. creating probability based on budgetary spending of each team during the year)

## Explore Data
### Data Cleaning

Having the datasets come from Kaggle, the information is relatively clean and doesn't have many nulls.  The issue is relevant information is only available to certain periods of time such as qualifying lap times for every year.  (Qualifying information on Kaggle contained roughly a quarter of all races)

## Here is a snapshot description of model preparation including:
1. renamed columns to better describe column 
2. renamed misspelt names (ex. Finish Surnames needed to be changed for accuracy)

## Features

## Features

Used the highest correlated features using a threshold of at least 90 % correlation to my predicting variable, rank.

<img width="693" alt="screen shot 2018-10-29 at 11 17 18 am" src="https://user-images.githubusercontent.com/34430819/47671770-8d19da00-db6d-11e8-9439-c0a2e77c5bab.png">


## Model Data

Before running models to my dataset, I had to make sure I would pick efficient methods to create an accurate predictor using cross validation and other methods.  The biggest obstacle that I had to be cognoscente of is overfitting.  Hence the reason for the use of cross validation. 

Cross Validation was executed by:
1. Training set was taken from 18 years 
2. Validation set was taken from 5 years
3. Testing set was taken from 2 years

## Model Selection
Wanted to implement a real-world approach to my model selection for predicting a Formula 1 predictor ranking.  I decided the best avenue would be model stacking, seeing which models performed better than others.  

### Performance Metrics

**Random Forest Regressor**:
The concluding result I was able to achieve and 87% score.
Methods used during Random Forest Regressor:

1.	Samples multiple subsamples with replacement from the training data
2.	Train a decision tree for regression (splitting e.g. by maximizing reduction in variance ) on each subsample, where each leave node outputs the mean of all label values in the node.
3.	Predict by averaging over the predictions of all decision trees.

**NOTE** The reason as to why Random Forest Regressor achieved the highest results because it took the highest correlated features and used them in predicting the the outcomes of the race.  


## Conclusion
As expected for the 2018 Formula 1 season, Lewis Hamilton won the Drivers' Championship.  While writing this comment (10/29/2018) the team championship is still up for grabs between Mercedes and Ferrari with two races to go.  However, Mercedes is likely to win due to its reasonable lead.  This confirms the **bias** aspect of the sport.  2019 will be a fun year to come with the new changes coming next season.  Let's hope Daryl Morey cakes his pants.  

<img width="795" alt="screen shot 2018-10-29 at 10 53 10 am" src="https://user-images.githubusercontent.com/34430819/47669899-27c3ea00-db69-11e8-9bbc-4285f86959c8.png">


### Further Explorations

My further interest would be a way to calculate aerodynamic packages for specific race tracks. My analysis of a way to measure this would be to use neural networks to analyze certain components of a car and compare those aero concepts to other teams and see which has the most efficient way through the track.   






