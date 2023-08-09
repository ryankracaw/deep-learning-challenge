1. Overview of the analysis:

2. Results:

* Data Preprocessing
  * What variable(s) are the target(s) for your model?
    * The target variable is the 'IS_SUCCESSFUL' column from application_df.
  * What variable(s) are the features for your model?
    * The feature variables are every other column from application_df. This was defined by dropping the 'IS_SUCCESSFUL' column from the original dataframe.
  * What variable(s) should be removed from the input data because they are neither targets nor features?
    * Both 'EIN' and 'NAME'(I kept this column later for better accuracy) columns were dropped/removed, because they were neither targets nor features for the dataset.

* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
     * In the first attempt, I used 5 hidden_nodes_layer_1 and 2 hidden_nodes_layer_2 -- these were just random guesses from which to iterate upon in the second try. This gave me a low accuracy of about 50%. In my second attempt I tried 8 for layer 1 and 5 for layer 2. This gave me an accuracy of about 70%. I knew I could do a little better, so I tried 10 for layer 1 and 8 for layer 2. This gave me about 73%. I think this is the best result for just two layers. I then added a third layer. I also only dropped the 'EIN' column and kept the 'NAME' column. So layer1 = 10, layer2 = 8, layer3 = 6. Success! I hit 75% accuracy!
  * Were you able to achieve the target model performance?
     * I was able to get to 75%!
  * What steps did you take in your attempts to increase model performance?
     * I added more layers and added additional hidden nodes in an attempt to achieve higher model accuracy. I also kept the 'NAME' column.

3. Summary:
