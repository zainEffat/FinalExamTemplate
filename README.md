
#First Part: Data Joining and Geospatial figures
Given to you a collected data (hate_crimes.csv dataset) on key socioeconomic factors for each US state, including indicators for education (percent of adults 25 and older with at least a high school degree, as of 2009), diversity (percent nonwhite population and percent noncitizen population, 2015), geographic heterogeneity (percent population in metropolitan areas, 2015), economic health (median household income, 2016 seasonally adjusted unemployment, September 2016, percent poverty among white people. 2015, and income inequality as measured by the Gini index, 2015), and what percent of the population voted for Donald Trump.
Additionally, the shape file for all US states along with some additional data is given to you (States_shapefile.shp).

##Task 1 (3 Marks):
Join both data frames that you have (hate_crimes and us_states) by state name. In order to complete this task, you need to do the following:
1-	Rename the State_Name variable in us_states dataset to state using rename() function.
2-	Change the states' names in both datasets to lower case using mutate() and tolower() functions.
3-	Use left_join() function to merge both data sets into a new data tibble called state_crimes



##Task 2 (3 Marks):
Usin ggplot() and geom_sf(), draw the US states maps that shows the following:
1-	A map that shows US stats colored by hate_crimes_per_100k_splc variable.
2-	A map that shows US stats colored by share_non_white variable.
Do you see any relation between both maps?

##Task 3 (4 Marks):
Come up with a research question based on these data and write it down. Then, create an effective data visualization that answers the question and write a brief paragraph explaining how your visualization answers the question. 

 
#Second Part: Data Wrangling and Prediction Models
Here, you will be working with demographic data from counties in the Midwest from the midwest dataset in R. You can learn more about this dataset by typing ?midwest into the console.

##Task 1 (3 Marks):
Find out the most five counties with most number of children below poverty. In order to complete this task, you need to do the following:
1.	Mutate a new variable called popchild by subtracting popadults from poptotal.
2.	Mutate a new variable childwithpoverty describing who many children in each county are below poverty by multiplying popchild by percchildbelowpovert.
3.	Sort the data frame by childwithpoverty column and show the top 5 only.

##Task 2 (3 Marks):
Do Midwestern cities with a higher percentage of people with a college degree have a lower poverty rate? Using ggplot, make a scatterplot with percentage of people with a college degree as the explanatory variable and the percentage of the total population below the poverty line as the response variable. Make sure to label your axes and give the plot a title. Please discuss what your scatterplot shows and if a linear assumption is appropriate.

##Task 3 (3 marks):
Fit a linear model with percentage with a college degree as the explanatory variable and poverty rate as the response variable. Please write out the model and interpret both the intercept and slope coefficient for percentage with a college degree.
Hint: use lm() method that we had in lecture 9 (slide 34).


##Task 4 (4 Marks):
Can we really predict the poverty rate for adults (percbelowpoverty) using the variables given in this dataset? Train a machine learning model of your choice (Random Forest can work) and find the accuracy rate of that model?
Steps:
1-	Split the dataset to train and test data.
2-	Train the Machin Learning Model using train() method. Please note that training might take long time to be completed (it was less than 5 minutes for me). So, it is not necessary to complete the training process during the exam. I just want to make sure that you have correct logic in solving this question.
Hint: use caret methods that we did in lecture 14 (slides 8 and 34 to 37)

#Submission
Knit to PDF to create a PDF document. Stage and commit all remaining changes, and push your work to GitHub. Make sure all files are updated on your GitHub repo. Only upload your PDF document to Blackboard. Before you submit the uploaded document, mark where each answer is to the exercises.

