## **Objective**

The goal of this assignment is to train a Named Entity Recognition (NER) model using Conditional Random Fields (CRF) to extract key entities from recipe data. The model will classify words into predefined categories such as ingredients, quantities and units, enabling the creation of a structured database of recipes and ingredients that can be used to power advanced features in recipe management systems, dietary tracking apps, or e-commerce platforms.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Provide general information about your project here.
- What is the background of your project?
- What is the business problem that your project is trying to solve?
- What is the dataset that is being used?

## General Information

The goal of this assignment is to train a Named Entity Recognition (NER) model using Conditional Random Fields (CRF) to extract key entities from recipe data. The model will classify words into predefined categories such as ingredients, quantities and units, enabling the creation of a structured database of recipes and ingredients that can be used to power advanced features in recipe management systems, dietary tracking apps, or e-commerce platforms.

## Conclusions
**Model Training approach and Results**

###Insights from validation dataset
#####From the classification report we can draw the below insight:
- Model performance is excellent with an overall accuracy of 98.68% and macro F1-score of 97.79% indicates that your model is highly reliable across all three entity types
- Ingredient entity type performs the best with Precision: 0.9878, Recall: 0.9962, F1: 0.9920. The model is quite confident and accurate in recognizing the ingredients.
- Quantity entity also performs very well with F1-score of 0.9890.
- Unit has low score, still very strong performance, but relatively lower recall (0.9302). There are chances o mis-classifying the units compared to other entities.
#####From the confusion matrix we have the following insights
- Model accuracy is very high. The diagonal values (406, 333, 2099) represent correct predictions. 
- Almost all tokens are classified correctly across all three classes.
- Similar to classification report, here also ingredients perform best where out of 2107 (2+6+2099) only 9 are mis-classified.
- Quantity class is very clean where out of 411, only 5 misclassifications (2 as unit, 3 as ingredient).
- Unit has major mis-classification where 23 unit tokens misclassified as ingredients (most significant confusion).



###Recommendations
- No major recommendations, model looks very good. Units can be looked into a bit for further accuracy.

###Conclusion
- The given dataset was overall ok but few data quality issues were identified with 5 records where the input token and corresponding pos tag lengths were  not matching.
- The primary entities extracted were 'quantity', 'ingredient', and 'unit'.
- Generally, a very good model with more than 98.68% accuracy and weighted F1-score 98.67%.
- Model is not overfitted as it works very well on unseen data.
- Due to its high-accuracy, The CRF model can reliably replace manual tagging of recipe data, saving time and reducing error.


## Technologies Used
- numpy version: 1.26.4
- pandas version: 2.2.2
- seaborn version: 0.13.2
- matplotlib version: 3.10.0
- sklearn version: 1.6.1
- jar
- re
- sklearn_crfsuite
- joblib
- random
- spacy

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This is an assignment from upgrad.

## Contact
Created by [@chinmayajeet] - feel free to contact us!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->