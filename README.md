# 19_Neural_Network_Charity_Analysis
## Relevant Folders and/or Files
-	Folder - Challenge
    -	AlphabetSoupCharity.ipynb
    -	AlphabetSoupCharity_Optimization.ipynb
    -	AlphabetSoupCharity.h5
    -	AlphabetSoupCharity_Optimization.h5
    -	charity_data.csv

## Project Overview
### Purpose
The purpose of this challenge was to explore Neural Networks machine learning to help 'Beks' from "Alphabet Soup Nonprofit Foundation” create a binary classifier that is capable of predicting whether grant applicants will be successful if funded by Alphabet Soup.

### Data Analyzed
-	Alphabet Soup Charity dataset (charity_data.csv)

### Deliverables 
The deliverables for this assignment were:
-	Deliverable 1: Preprocessing Data for a Neural Network Model 
-	Deliverable 2: Compile, Train, and Evaluate the Model 
-	Deliverable 3: Optimize the Model ## Results

## Results

### Data Preprocessing
**1) What variable(s) are considered the target(s) for your model?**
*For this dataset, I used the “IS_SUCCESSFUL” column as the target variable.*

**2) What variable(s) are considered to be the features for your model?**
*In the initial model, I used the following columns as features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION,  STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, & ASK_AMT.*  

*In later models, I dropped some of the features to help increase the accuracy and reduce loss in the models (see bullet below for more details).*

**3) What variable(s) are neither targets nor features, and should be removed from the input data?**
*Initially, columns EIN & NAME were dropped.*

*In subsequent attempts (Deliverable 3), I also dropped STATUS & ASK_AMT.  I chose to eliminate those columns because only I figured that only “active” nonprofits (STATUS) would be applying for grants, so reviewing non-active organizations was unneeded.  I chose to eliminate ASK_AMT because the density plot showed an overwhelming number of organizations (25,398) applied for an ask amount of $5,000, so I figured the column was not very useful.* 

### Compiling, Training, and Evaluating the Model
**How many neurons, layers, and activation functions did you select for your neural network model, and why?**
*I tried eight variations of neurons, layers, and activation functions in my model attempts.*  Screenshots of all eight attempts are below (Code Snippets section).

**Were you able to achieve the target model performance?**
*No, despite trying 8 variations, I was not able to get 75% or greater accuracy.  The best I was able to get was 72.70.*
- Attempt 1: Loss = 0.662, Accuracy = 0.559
- Attempt 2: Loss = 0.682, Accuracy = 0.601
- Attempt 3: Loss = 0.623, Accuracy = 0.693
- Attempt 4: Loss = 0.556, Accuracy = 0.724
- Attempt 5: Loss = 15.406, Accuracy = 0.640
- Attempt 6: Loss = 4.630, Accuracy = 0.605
- Attempt 7: Loss = 0.553, Accuracy = 0.727
- Attempt 8: Loss = 0.589, Accuracy = 0.718

**What steps did you take to try and increase model performance?** 
- I tried dropping additional columns.
- I tried changing the number of neurons and hidden layers.
- I tried changing the activation functions.
- I tried changing the number of epochs.  

### Code Snippets of Attempts

![image](https://user-images.githubusercontent.com/92705556/165880333-6be1bea2-a496-40bc-afa6-a3b0e85a870b.png)

![image](https://user-images.githubusercontent.com/92705556/165880420-0ff811d7-1953-41aa-bef1-17aa15443f61.png)

![image](https://user-images.githubusercontent.com/92705556/165880465-26151043-ca6b-4435-9840-1948340bbeb7.png)

![image](https://user-images.githubusercontent.com/92705556/165880516-718e40ba-f9b6-4ce7-a89f-77985d901799.png)

![image](https://user-images.githubusercontent.com/92705556/165880563-919b2248-18ca-4b3b-acbd-2c1be0ff9a98.png)

![image](https://user-images.githubusercontent.com/92705556/165880600-b0a0ecba-614a-4412-8555-33b7c28e44f7.png)

![image](https://user-images.githubusercontent.com/92705556/165880615-45fe3a2c-525f-4519-a29c-aacfb213470e.png)

![image](https://user-images.githubusercontent.com/92705556/165880651-458eb6f3-d796-4adc-a91e-df79dc3532f6.png)


## Summary Conclusions on Neural Networking
Deep Neural Networking is a very detailed and in-depth algorithmic / analytic process that can potentially tease out even the finest and most minute variability in data.  However, due to its complexity, it takes a long time to complete and can be difficult for people just beginning their analysis journey  to understand.  

Other supervised machine learning models, like Random Forest Classifier that combines multiple smaller models into a more robust and accurate model, are similar and  often return comparable performance and accuracy results.  These simpler models also run more quickly that neural network models and may be easier to understand.  

No model is perfect, but having the ability and knowledge to use different models is nice.  
