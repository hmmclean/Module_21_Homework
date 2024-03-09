# Module_21_Homework
Module 21 - Deep Learning Challenge

# Overview of the analysis: 
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. 

# Results: 
Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
-------------------
* What variable(s) are the target(s) for your model?
    * The targets are the successful applicants. Within the dataset, this column is labeled as IS_SUCCESSFUL. 
* What variable(s) are the features for your model?
    * The features are all the other columns in the dataset. This includes but is not limited to, application types, income, ask amount, affiliation, and classification. 
* What variable(s) should be removed from the input data because they are neither targets nor features?
    * EIN and NAME columns can be removed as they are neither targets nor features. 

Compiling, Training, and Evaluating the Model
---------------------------------------------
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
     * Initially, I used two layers, the first with 80 nodes and the second with 30 nodes. I used one activation function, relu, for both layers. Since we've transformed the data to binary outputs the relu activation function is the most appropriate choice. These achieved an accuracy score of 73%, rounded. To boost this accuracy score, I optimized the model by
* Were you able to achieve the target model performance?
     * Yes, with the optimization changes I was able to generate an accuracy score of 78%, which is higher than the acceptable criteria of 75%. 
* What steps did you take in your attempts to increase model performance?
     *

# Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.


# Resources and References
* Chat GPT - https://chat.openai.com/
