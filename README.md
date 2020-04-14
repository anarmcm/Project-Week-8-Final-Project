<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# TMDB 5000 Movie Dataset
*Ana Recio de Mur*

*[Data Analytics, Ironhack, 2019]*

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
In this project I analyse the TMDB Movie Dataset, with the objective of predicting a movie's success, before it has been released. I considered movie's success could be explained both by the revenue generated and its rating. I also wanted to see if the popularity was related to its success.  

## Hypotheses / Questions
* Can we build a model to predict a movie's success?

## Dataset
* The data comes from the TMDB API. From this API I downloaded a csv. from Kaggle.
* The dataset contains 5000 movies with the following columns:
    - Movie Title
    - Budget 
    - Revenue
    - Runtime
    - Release Date 
    - Popularity 
    - Vote Average 
    - Vote Count (amount of people that voted)
    - Genres 
    - Production Companies 
    - Production Countries 
    - Cast 
    - Crew
    - Original Languages 
    - Spoken Languages 

## Cleaning

It is a popular quote in Data Science that 80% of the work accounts for the cleaning. In my case it was a 90%. 
    - A problem I encountered was that the columns "cast", "crew", "genres", "production companies", "production countries", "original languages" and "spoken languages" were in JSON format, so I had to parse the JSON string using json.loads.
    - Another problem I faced was that there was missing data for revenue and budget, around 30% of missing values, so I had to drop the missing values, however, I saved two datasets, one dropping the missing values of these columns, and another one dropping the two columns completely. I used the first dataset to predict the revenue, since I needed the budget and the revenue in order to train the data, and the second one to predict the score, since I found out it wasn't very correlated with budget and revenue.

## Analysis
* My main objective was to clean the data in order to improve the accuracy of the machine learning model.
* I looked at the correlations between the variables, both numerical and categorical, in order to see which features to include. 
* When creating dummies, I had to filter the cast and crew, since there were loads of actors and directors per movie. I looked at the correlations between actors/directors and revenue, and actors/directors and vote average, to see which directors and actors to include as features in the machine learning model. With this selection I could reduce the amount of columns to 158. However, this was still too much, so I used PCA to reduce the amount of features to 2. 

## Model Training and Evaluation
* Describe how you trained your model, the results you obtained, and how you evaluated those results.

## Conclusion
* An interesting conclusion from the project is that when using PCA the accuracy of the model was lower. 

## Future Work
Future improvements would be to have more data.

## Workflow
Outline the workflow you used in your project. What were the steps?
How did you test the accuracy of your analysis and/or machine learning algorithm?

## Organization
How did you organize your work? Did you use any tools like a trello or kanban board?

What does your repository look like? Explain your folder and file structure.

## Links
Include links to your repository, slides and trello/kanban board. Feel free to include any other links associated with your project.


[Repository](https://github.com/)  
[Slides](https://slides.com/)  
[Trello](https://trello.com/b/PmEjwQ7m/final-project)  
