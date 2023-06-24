# PLStream Model Performance & Confidence Evaluation

**As an Undergraduate Research Student, I worked under the guidance of Prof. Shuhao Zhang & his IntelliStream Research Team who aimed to develop a novel online sentiment classification system - PLStream - which processes data streams incrementally, classifies tweets with or without labels, & scales linearly with increasing hardware resources.**

## PLStream System Architecture

<img width="815" alt="image" src="https://user-images.githubusercontent.com/64684527/203735766-49a34564-7bcc-437f-9139-c23cb0714005.png">

**I worked independently to quantitatively assess the overall model performance & predictive accuracy of PLStream using various statistical techniques in Python.**

**Dataset of Population Sample** contained actual tweet sentiments & sentiment predictions of 5,60,000 tweets made by the PLStream binary classifier which is a two-layer word2vec neural network followed by a softmax activation function & a categorical cross-entropy loss function.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/fe133db9-cf01-4b9a-9765-eac986b327a2)

## Evaluation of PLStream Model Performance

● **Random Undersampling** & **SMOTE** techniques to fix binary class imbalance in the sample dataset containing true & predicted tweet sentiments.

● Experimented with different Performance Evaluation Metrics such as **Confusion Matrix**, **Accuracy**, **F1-Score**, **ROC AUC** & **PR AUC** to understand trade-offs & choose the best metric for the PLStream binary classifier.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/c038a4fd-ef8f-4bff-a84f-a693496088d9)

## Data Wrangling & Manipulation of pseudo_dataset

The list form of *pseudo_dataset* found in *plstream_linear.ipynb* contains valuable information which could help us derive valuable insights on quantitatively evaluating PLStream model performance.

**Data format :** [index,|cosine similarity difference|, predicted label,{neg_coefficient,pos_coefficient,true_label,'cos_sim_bad','cos_sim_good'}]

To make the data easier to work with, conversion of the data to a data frame format containing cosine similarity difference and correct guess values was performed.

● **Student's t-test** to discover a statistically-significant difference between mean cosine similarity difference values for correct & incorrect tweet sentiment predictions.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/b572fb1c-35db-40b9-bc07-4b0b8a950766)

● **Kernel Density Estimation** to discover the underlying Normal Probability Density Function of the frequency of correctly predicted tweets for their corresponding cosine similarity difference values.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/dbeeb29f-e670-44b2-98de-9ed0f91ef4d4)

● **Confidence Intervals** of the true means of the cosine similarity difference values for correct & incorrect tweet predictions made by PLStream model.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/19d2adb9-2194-408d-82fb-23df78f82a69)

## Ad-Hoc Tasks

**Literature Review of Research Papers**

- CAMEL - Managing Data for Efficient Stream Learning: https://dl.acm.org/doi/pdf/10.1145/3514221.3517836
- Online Coreset Selection for Rehearsal-based Continual Learning: https://openreview.net/pdf?id=f9D-5WNG4Nv
- Cynical Selection of Language Model Training Data: https://arxiv.org/abs/1709.02279
- Corpus Similarity Measures Remain Robust Across Diverse Languages: https://arxiv.org/abs/2206.04332

**Corpus Correlation Analysis of Scholarly STEM Articles from 2018 - 2022**

**Dataset used:** https://www.kaggle.com/datasets/Cornell-University/arxiv

Text pre-processing -> TF-IDF DTM -> Pivot Table -> Dimensionality Reduction on Sparse Matrix with PCA -> Correlation Analysis Heat Map

<img width="432" alt="image" src="https://user-images.githubusercontent.com/64684527/210374182-ca9698bc-2576-470f-bd2c-f8a2550cf9f0.png">
