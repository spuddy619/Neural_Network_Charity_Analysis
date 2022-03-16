# Neural_Network_Charity_Analysis

## Purpose of Analysis:
The purpose of this endeavor is to use machine learning to inform the company in how they invest into charities. The executives want to be able to donate their money into charities that will be able to sucessfully use this money for their cause. We are going to employ deep learning models to gauge what qualities best predict successful use of this money and then use the findings to make future charity donations more successful.

## Results
### Data Preprocessing
- The target feature in this particular dataset is the "is_successful" column as we want to understand whether or not a donation led to a charity's success.
- The features, or the columns of data that we want the machine to consider, are:
  - APPLICATION_TYPE
  - AFFILIATION
  - CLASSIFICATION
  - USE_CASE
  - ORGANIZATION
  - INCOME_AMT
  - SPECIAL CONSIDERATIONS
- Removed features deemed extraneous:
  - EIN
  - NAME


### Compiling, Training, Evaluating the Model
![image](https://user-images.githubusercontent.com/72320203/158697890-5c326207-8633-4c13-a9c7-36d2d4a55400.png)<br/>

- The model has two hidden layers with 80 and 30 neurons.
- The activation functions for the two hidden layers was "relu" and the ouput later had an activation function of "sigmoid"
- The purpose for using the "sigmoid" function is so that we have a binary classification as we are looking for binary results (charity is successful/charity is not successful). The sigmoid outputs between either 1 or 0.
- The target model performance was set at 75% accuracy which this model failed to do as you can see from the photo:
![image](https://user-images.githubusercontent.com/72320203/158699115-160e60ef-56a1-40a0-8224-9cf8592f7643.png) <br/>
- Multiple attempts were made to optimize its performance:
  - the feature "ASK_AMT" was binned into ranges due to the large number of unique values; the 8,747 unique values were binned into features described by price range. Unfortunately, this alteration decreased the accuracy of the model with the accuracy percentage droppping to low 60 percent, at best. There were also issues with the losses. Oddly, there was over 100 percent loss in many.
  - We changed activation functions from the current "relu", "relu", "sigmoid" setup. These alterations decreased the accuracy of the model as we failed to manipulate these functions into improving our accuracy score.
  - The number of neurons were altered but we failed to manipulate the total neurons into improving our accuracy score.
  - The number of epochs were also altered but any significant changes we made to the epoch count resulted in negligible or negative changes for our accuracy score.

## Summary
Our model did not achieve the target of 75% accuracy so we have concluded that the model is underperforming. Supervised machine learning may lead to a better model  as the question being posed ("Is the charity successful or not successful?") is a binary classification. We recommend that we try different methods of machine learning considering this model failed to achieve 75% accuracy - not a particularly high bar for accuracy.
