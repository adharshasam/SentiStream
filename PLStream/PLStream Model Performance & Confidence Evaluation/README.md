# PLStream Model Performance & Confidence Evaluation

**This folder contains all my contributions for the Data Science Research project - Online Sentiment Classification Of Massive Data Streams - as an Undergraduate Research Student at SUTD.**

Worked with a train.csv dataset containing actual tweet sentiments & sentiment predictions of 5,60,000 tweets made by the PLStream classifier which is a two-layer word2vec neural network followed by a softmax activation function & a categorical cross-entropy loss function.

<img width="250" alt="image" src="https://user-images.githubusercontent.com/64684527/199879816-ed0b10ab-2dd9-476a-8bb1-2c974a09ea09.png">

## PLStream System Architecture 

<img width="815" alt="image" src="https://user-images.githubusercontent.com/64684527/203735766-49a34564-7bcc-437f-9139-c23cb0714005.png">

## Evaluation of PLStream Model Performance

- Fixed binary class imbalance in the dataset using *Random Undersampling* & *SMOTE* techniques.

- Studied the trade-offs among Performance Evaluation Metrics such as *Confusion Matrix*, *Accuracy*, *F1-Score*, *ROC AUC* & *PR AUC* and recommended suitable performance metrics to accurately evaluate the performance of PLStream binary classifier, also considering its pros and cons.

<img width="847" alt="image" src="https://user-images.githubusercontent.com/64684527/199883550-4cb0276b-ab6c-485b-8999-914c62abd3b6.png">

## Data Wrangling & Manipulation of pseudo_dataset

The list form of *pseudo_dataset* found in *plstream_linear.ipynb* contains valuable information which could help us derive valuable insights on quantitatively evaluating PLStream model performance.

Data format : [index,|cosine similarity difference|, predicted label,{neg_coefficient,pos_coefficient,true_label,'cos_sim_bad','cos_sim_good'}]

To make the data easier to work with, conversion of the data to a data frame format containing cosine similarity difference and correct guess values was performed.

## Confidence Evaluation of PLStream Classifier

- Carried out the *Student's t-test* and detected a statistically-significant difference between mean cosine similarity difference values for correct and incorrect tweet sentiment predictions.

<img width="691" alt="image" src="https://user-images.githubusercontent.com/64684527/199883965-657e98a9-cd63-4045-83e4-db5b91af336c.png">

- Discovered the underlying *Normal Probability Density Function* for the frequency of correctly predicted tweets in relation to their corresponding cosine similarity difference values.

<img width="721" alt="image" src="https://user-images.githubusercontent.com/64684527/199883277-a8d1d8cc-0a47-4ee7-bc61-3fd77027a0dc.png">

- Calculated *Confidence Intervals* for the true means of the cosine similarity difference values for correct and incorrect tweet predictions made by the PLStream model.

<img width="667" alt="image" src="https://user-images.githubusercontent.com/64684527/199883388-eadc4c9c-f9c1-428a-a209-e176f3ed6946.png">

## Literature Review of Research Papers

- CAMEL - Managing Data for Efficient Stream Learning: https://dl.acm.org/doi/pdf/10.1145/3514221.3517836
- Online Coreset Selection for Rehearsal-based Continual Learning: https://openreview.net/pdf?id=f9D-5WNG4Nv
- Cynical Selection of Language Model Training Data: https://arxiv.org/abs/1709.02279
- Corpus Similarity Measures Remain Robust Across Diverse Languages: https://arxiv.org/abs/2206.04332
