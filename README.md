# Formula 1 Project

<img width="622" alt="screen shot 2018-10-16 at 1 47 18 pm" src="https://user-images.githubusercontent.com/34430819/47047205-cef95800-d14b-11e8-9e3f-532e9c6c61fb.png">

## James Lambert

## Predicting and Analyzing Race Results During a F1 Season

**Goal:** The primary goal of this project was to predict a Formula 1 race winner from that season's team and driver stats.  The ultimate ambition for this project is to use a predictive model as a starting point for insight as to racer and team success to provide a foundational foundation as to how well a team/driver will do based on those metrics.

## Define the Question

Are we able to predict which team and individual racer wins a Formula 1 race based on team statistics, and the racers past success?

## Supplementary background and interest in this Sport 

Formula 1 is broken down into two championships: a team championship where two drivers on the same team compete and pool one another's points together for the team.  The latter is an individual championship in which each driver is fighting for themselves.  

### So why is determining these two-metrics important?
1.  It can provide an estimate of which team and driver has the potential to win the championship at the end of the year.
2.  You could bet on it in a betting platform if you believe in your model
3.  I have a passion for the sport and wanted to dive more in the data for some new insight and knowledge to further my    interests involving the sport
  
## Data Gathering
The data was gathered from a project on Kaggle.(< https://www.kaggle.com/cjgdev/formula-1-race-data-19502017> )

In addition, I researched what teams spend in a year and created a probability column indicating the likelihood of winning a race depending on the amount of money they spend in a year.

The following teams have a higher percentage of winning due to yearly budgetary expenses:
1. Ferrari
2. Red Bull
3. Mercedes AMG

I didn't include McLaren or Renault into this calculation based on their lack of success in recent years.  
  
**Note:** The Reason I chose the 1991 season and onward as my training example is due to:

1. 1991 was Michael Schumacher's rookie season and the most winningest driver of all time in Formula 1

In the end the data looked like:
1. 1991 - 2016 as the training dataset
2. 2017 as the testing dataset
3. Numerous Engineered features(ex. creating probability based on budgetary spending of each team during the year)
<img width="385" alt="screen shot 2018-10-25 at 4 30 49 pm" src="https://user-images.githubusercontent.com/34430819/47536133-6dd03380-d873-11e8-9320-da39801c7965.png">
## Explore Data
### Data Cleaning

Having the datasets come from Kaggle, the information is relatively clean and doesn't have many nulls.  The issue is relevant information is only available to certain periods of time such as qualifying lap times for every year.  (Qualifying information on Kaggle contained roughly a quarter of all races)


