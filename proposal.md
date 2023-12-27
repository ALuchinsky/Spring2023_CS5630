# Urban Crime Data Classification

Group 5, CS 5630, Final Project Proposal

Michael Boon, Xin Jin, Aleksei Luchinsky, Dan Mrachko

## Problem Statement

An emerging area of research focuses on criminal classification methods for crime forecasting. By studying and comparing well-known prediction algorithms, our main objective is to predict crime categories based on a given collection of geographical and time-based factors, such as the district and address of the city where the crime was committed, the latitude and longitude of the crime position, dates, and the day of the week on which the crime occurred. For security organizations to allocate resources effectively, it is both fascinating and important to study and understand the distribution of various crime types throughout the city based on their occurrence times and locations. Crime statistics can help officers share observations and enhance early warning systems to keep residents safe in their communities. 
 
There are 39 distinct crime types found in the San Francisco dataset. A response variable with an excessive number of classes will make exploratory data analysis (EDA) laborious and make it challenging to identify patterns and understand criminal trends. A possible solution is to combine many smaller classes of crimes to classify two significant crime types, such as violent crime and nonviolent crime. In such a way, our project would be a binary crime prediction task.
 
We will read the preceding article regarding prediction for the type of crimes, "Predicting and Preventing Crime: A Crime Prediction Model Using San Francisco Crime Data by Classification Techniques" [1], which clarifies an overview of crime category forecasting from a broader perspective, and the motivation and importance of our study in detail. In addition, the following two papers provide the context and background on the same research topic: "Comprehensive analysis of Classical Machine Learning models and Ensemble methods for predicting Crime in urban society" [2] and "Crime Prediction with Geo Hotspots and Heatmaps using Machine Learning" [3].

## The Dataset

Our first goal is to analyze the San-Francisco Crime data set, which can be found on Kaggle [https://www.kaggle.com/competitions/sf-crime/data]. In this dataset one can find information about approximately 2 million crimes, registered in San-Francisco between 2003-2015. For each case such features as crime category, date, location, etc., are specified (10 features in total). Using this dataset with classification machine learning methods, all variables besides crime category can be treated as predictors to predict the crime category.
In addition to this, one can also find on Kaggle similar data sets with information about crimes in Montreal [https://www.kaggle.com/datasets/stevieknox/montreal-crime-data], Denver [https://www.kaggle.com/datasets/paultimothymooney/denver-crime-data], and Philadelphia [https://www.kaggle.com/datasets/mchirico/philadelphiacrimedata]. These tables have similar sets of features, so we could easily include them into our analysis.

## Methodology and Approach

The first step of the data analysis will be cleaning and preparation of the data sets. After searching for missing, incorrect, and outlier values, we will decide which of the presented features could be useful in our analysis. Encoding will be necessary for categorical features, and performing calculations to create new metrics or statistics may enhance the dataset. If necessary, scaling and normalization will be applied at this stage to prepare the data for modeling.

Encoding methodology for categorical variables appears to have an impact on the results and accuracy for neural network-based approaches [4]. Since the research is murky in this domain, several different encoding techniques will be attempted prior to modeling with the additional goal of garnering evidence for preference of encoding technique for future projects.

After cleaning, wrangling, and performing exploratory analysis, the next step will be the development of machine learning models. After splitting the data into suitable training and testing sets, some of the methods we intend to compare include: 

*	Logistic Regression
*	Decision Tree
*	Support Vector Machine
*	Random Forest
*	Neural Networks
*	Naive Bayes
*	Gradient Boosting Decision Tree

Training will include tailoring each algorithm???s hyperparameters with cross-validation and iterative tuning to achieve maximum accuracy with regards to success statistics for each modelling approach. In the case of binary classification, the statistics we will compare are accuracy (overall prediction accuracy), sensitivity (impact of the negative class), and specificity (impact of the positive class). After modeling is complete, the results and method comparisons will be presented in a table for ease of reference, and conclusions from the project will be discussed. An analysis of variance will show which parameters were the most important classes in each model and potentially inform future research in the domain.

## References

[1] 	M. Khan, A. Ali and Y. Alharbi, "Predicting and Preventing Crime: A Crime Prediction Model Using San Francisco Crime Data by Classification Techniques," Complexity, p. 13, 2022. 

[2] 	S. R. Divyasri, R. Saranya and P. Kathiravan, "Comprehensive analysis of Classical Machine Learning models and Ensemble methods for predicting Crime in urban society," 07 February 2023. [Online]. Available: https://www.researchsquare.com/article/rs-2550707/v1. [Accessed 02 March 2023].

[3] 	S. Bhavana and T. P. Pushpavathi, "Crime Prediction with Geo Hotspots and Heatmaps using Machine Learning," Specialusis Ugdymas, vol. 2, no. 43, 2022. 

[4] 	K. Potdar, T. Pardawala and C. D. Pai, "A Comparative Study of Categorical Variable Encoding Techniques for Neural Network Classifiers," International Journal of Computer Applications, vol. 175, no. 4, 2017. 





