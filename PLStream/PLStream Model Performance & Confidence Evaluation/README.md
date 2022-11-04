# PLStream Model Performance & Confidence Evaluation

Worked with a train.csv dataset containing actual tweet sentiments & sentiment predictions of 560000 tweets made by the PLStream classifier which is a two-layer word2vec neural network followed by a softmax activation function & a categorical cross-entropy loss function.

<img width="250" alt="image" src="https://user-images.githubusercontent.com/64684527/199879816-ed0b10ab-2dd9-476a-8bb1-2c974a09ea09.png">

## Evaluation of PLStream Model Performance

- Fixed binary class imbalance in the dataset using *Random Undersampling* & *SMOTE* techniques.

- Studied the trade-offs among Performance Evaluation Metrics such as *Confusion Matrix*, *Accuracy*, *F1-Score*, *ROC AUC* & *PR AUC* and recommended suitable performance metrics to accurately evaluate the performance of PLStream binary classifier, also considering its pros and cons.

<img width="608" alt="image" src="https://user-images.githubusercontent.com/64684527/199881161-ce21a77f-f052-4620-8486-cabceefb6046.png">

## Data Wrangling & Manipulation of pseudo_dataset

The list form of *pseudo_dataset* found in *plstream_linear.ipynb* contains valuable information which could help us derive valuable insights on quantitatively evaluating PLStream model performance.

*Data format : [index,|cosine similarity difference|, predicted label,{neg_coefficient,pos_coefficient,true_label,'cos_sim_bad','cos_sim_good'}]*

To make the data easier to work with, conversion of the data to a data frame format containing cosine similarity difference and correct guess values was performed.

## Confidence Evaluation of PLStream Classifier

- Carried out the *Student's t-test* and detected a statistically-significant difference between mean cosine similarity difference values for correct and incorrect tweet sentiment predictions.

![image](https://user-images.githubusercontent.com/64684527/199881870-7da2751d-eed5-46b1-8bf4-4fb837edb116.png)

- Discovered the underlying *Normal Probability Density Function* for the frequency of correctly predicted tweets in relation to their corresponding cosine similarity difference values.

<img width="551" alt="image" src="https://user-images.githubusercontent.com/64684527/199881376-c8a57b3d-dfcb-4367-9829-7505a69185ab.png">

- Calculated *Confidence Intervals* for the true means of the cosine similarity difference values for correct and incorrect tweet predictions made by the PLStream model.

<img width="506" alt="image" src="https://user-images.githubusercontent.com/64684527/199881567-6c42804c-e345-41b5-879a-b49dd2a95ea9.png">
