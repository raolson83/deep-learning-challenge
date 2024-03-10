Overview of the analysis: The purpose of this analysis is to identify the best funding opporutunities for the my company Alphabet Soup. The variables provided should help to predict the best opportunities. 

Results: 

Data Preprocessing

What variable(s) are the target(s) for your model: The target variable is the binary "IS_SUCCSESSFUL"
What variable(s) are the features for your model: The features of the model are application type, affiliation, classification, use case, organization, status, income amount, special considerations, and ask amount. 
What variable(s) should be removed from the input data because they are neither targets nor features: EIN and Name are neither targets nor features

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance? First, I changed the bin amount for application type to include one additional type. Then I increased the number of units in the first layer to 100 and the second layar to 50. I also added a third hidden layer at 15 units that did not do anything. I tried activation as tanh but that made it worse. Finally, not able to reach the goal of 75% accuracy, I ran keras_tuner. After 56 attempts it had not risen above 74%, so I kept my current model. 

 With 3 layers, there were 100 neurons in the first (relu), 50 in the second (relu), and 1 in the third (sigmoid).

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation. There was a lot of guesswork invovled in this approach. Keras_tuner should have been used from the beginning. Additionally, random forest may have been a good approach so as to identify the features that most contributed or did not contribute to the variability of the model so as to simplify.