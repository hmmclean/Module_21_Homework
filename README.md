# Module_21_Homework
Module 21 - Deep Learning Challenge

## Navigation
* Models 
    * AlphabetSoupCharity - HDF5 file output created by initial training code. 
    * AlphabetSoupCharity_Optimization - HDF5 file output created by optimization code. 
* AlphabetSoupCharity_Optimization - jupyter notebook file, created in Google Colab, that contains the code for optimizing the model.
* README - contains final analysis.
* Starter_Code_Colab - jupyter notebook file, created in Google Colab, that contains the initial code for training the model.


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
     * Initially, I used two layers, the first with 80 nodes and the second with 30 nodes. I used one activation function, relu, for both layers. Since we've transformed the data to binary outputs the relu activation function is the most appropriate choice. For the output layer, I chose 1 node as it is a binary classifier model with only one output, ie was the funding application successful yes or no? The output layer activation of sigmoid was used since the model output is a binary classification between 0 and 1. These achieved an accuracy score of 73%, rounded.
     * To boost this accuracy score, I optimized the model by adding an additional layer, adjusting the number of nodes, and leaving the name column as a feature. 
* Were you able to achieve the target model performance?
     * Yes, with the optimization changes I was able to generate an accuracy score of 79% (rounded), which is higher than the acceptable criteria of 75%. 
* What steps did you take in your attempts to increase model performance?
     * Initially, I added a third layer and changed the number of nodes for each layer to 80, 45, and 35 respectively. However, this did not seem to increase my accuracy score. So I reprocessed the data to include the name column, adding it as another feature, and then trained the model again, this time receiving an accuracy score of 79% (rounded). There are a few reasons that using the name as a feature would impact the model accuracy. The "name" column might contain valuable information related to the classification task that the model can learn from. For example, in certain contexts, names could be indicative of specific categories or classes. Or, the "name" column may be correlated with the target variable or other features in the dataset. Including correlated features can help the model capture more complex relationships within the data. Adding more features, especially those with meaningful information, can increase the model's complexity. Therefore, a more complex model may have the capacity to capture intricate patterns and nuances in the data, leading to improved performance.

# Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

In summary, the initial deep learning model achieved an accuracy score of 0.7284 with a loss of 0.5680, utilizing two layers with 80 and 30 nodes, respectively. The model excluded the name column from the original dataset. After optimization, the accuracy improved to 0.7896, and the loss decreased to 0.5509, employing three layers with 80, 45, and 35 nodes, respectively. The optimized model included the name column as a feature.

While the accuracy surpassed the target of 75%, there is room for improvement. To enhance the model further, I recommend utilizing an automated model optimizer. This tool would systematically explore various activation functions, layer architectures, and node combinations, allowing for a more exhaustive search of the hyperparameter space. Automation can save time and resources compared to manual tuning, providing a more comprehensive exploration and potentially yielding a more accurate classification model.

# References and Resources
* Chat GPT - https://chat.openai.com/
