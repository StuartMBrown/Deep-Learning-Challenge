#NEURAL NETWORK REPORT

###**Overview**  

This deep learning model, intended for the nonprofit Alphabet Soup, is designed to see if their fund applicants were successful in their ventures. Alphabet Soup provided me with records of over 34,000 businesses, organizations, etc. to prepare my model. These records included data on how much money these applicants had, how much Alphabet Soup gave them, and more. In essence, my model is designed to predict if Alphabet Soup's expenditures actually will assist their applicants in thriving. Despite Alphabet Soup's enthusiasm, they gave me a caveat; the model must achieve 75% accuracy before they can deploy it for themselves.

Results: Using bulleted lists and images to support your answers, address the following questions:

###**Data Preprocessing**

"IS_SUCCESSFUL" is our model's target. Alphabet Soup tasked us with predicting the ultimate outcome of their applicants' ventures.

All other columns, aside from "EIN" and "NAME" are fair game at worst for features. All can factor towards future applications of this model, particularly if Alphabet Soup wants to focus on the affiliation or organization of their applicants.

"EIN" and "NAME" need to be removed because our model is designed to be predictive of hypothetical applicants, not retroactively determine if some ventures "should" have failed or succeeded based on our other parameters.

###**Compiling, Training, and Evaluating the Model**


I chose 64 neurons because in a dataset like this, passing it through too few neurons prevents the model from making meaningful predictions; too many neurons and the model doesn't generalize. 64 felt optimal for the first layer of neurons.

For the same reasons, my model utilizes two hidden layers. Base Colab's lack of capacity, including multiple crashes when training my model, also meant playing it safe for the original data.

I used ReLU for the hidden layers and sigmoid for the output. Our data are both positive and nonlinear, so it fits better than a Tanh or leaky ReLU activation. Sigmoid is a probability, so it would be fed by the target predictions in each of our model's epochs.

###*Were you able to achieve the target model performance? What steps did you take in your attempts to increase model performance?*

My first model unfortunately achieved an accuracy of 72.676%, below Alphabet Soup's benchmark. I then made three separate, individual tweaks to the model by eliminating further columns, increasing the minima of the "APPLICATION_TYPE" and "CLASSIFICATION" bins, and adding three more hidden layers to the model. 

All three adjustments actually weakened the final accuracy. 

###**Summary** Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

This undertaking proved unproductive. Though Alphabet Soup involvement did appear to indicate successful dénouements for general applicants in the model, there is no compelling case for it under Alphabet Soup's criterion.

Using a logistic regression model will better streamline my data inputs, as Alphabet Soup has not currently raised concerns about bias or necessary weight. In the interim, I will also experiment with combining various tweaks of the new model, and with adding new tweaks.

######This project required the use of pandas, tensorflow, and Google Colab. Thanks to Jacob Dolinsky and Valeria Briones for their assistance.
