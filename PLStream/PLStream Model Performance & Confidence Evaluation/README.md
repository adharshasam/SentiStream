# PLStream Model Performance & Confidence Evaluation

**As an Undergraduate Student Researcher, I worked with the IntelliStream Research Group @ SUTD under the guidance of Prof. Shuhao Zhang who aimed to develop a novel, Apache Flink-based, semi-supervised online sentiment classification system – PLStream – which processes massive data streams incrementally, classifies text data (such as Twitter tweets or online product reviews) with or without labels as positive or negative text sentiments & scales linearly with increasing hardware resources.**

_The preprint of the research paper describing the framework of PLStream can be accessed here:_ [arXiv:2203.12368](https://arxiv.org/abs/2203.12368) [cs.DB]

## My Role in the IntelliStream Research Group

As a UROP (Undergraduate Research Opportunities Programme) Student, I was involved in the _‘Confidence Evaluation’_ segment of this NLP Research Project.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/2a65514e-c47a-4d6a-8a19-c786ca7318d8)

<sub>Fig: PLStream Online Text Sentiment Classification System Architecture</sub>

Using statistical & machine learning techniques in Python, I quantitatively evaluated the performance of the text sentiment classifier & calculated the 'confidence' of text sentiment predictions. 

During the course of this UROP project, I got good exposure to important concepts in Natural Language Processing & also received the opportunity to get hands-on experience using Data Science Python packages shown below.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/a12dcc69-e71e-4bea-929f-6d21565d1c75)


## Performance Evaluation of the Text Sentiment Classification System

★ Evaluated the performance of semi-supervised binary text sentiment classifier (a two-layer word2vec neural network + softmax activation function + categorical cross-entropy loss function) with labelled text data of over 300k predicted sentiment entries using various model performance metrics such as:

• **Confusion Matrix (Accuracy, Precision, Recall)**

• **F1-Score**  

• **ROC Curve & AUC Score**

• **Precision-Recall Curve & Average Precision**

• **Silhouette Coefficient**

• **Calisnki-Harabasz Coefficient**

for both supervised & unsupervised machine learning.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/64c1c00b-37a6-4758-bed8-9d6340aea68c)


![image](https://github.com/adharshasam/SentiStream/assets/64684527/cb60debc-a8b2-4d0c-b349-778314a90a2b)

<sub>Fig: Labelled text sentiment data containing ground_truth & prediction values</sub>


## 'Confidence' Evaluation of Text Sentiment Predictions

★ Performed **Two-Sample t-Test** to detect a statistically-significant difference between the mean cosine similarity difference values and the correct & incorrect text sentiment predictions.

★ Approximated the Gaussian PDF for the frequencies of correct text sentiment predictions using **Kernel Density Estimation**.

![image](https://github.com/adharshasam/SentiStream/assets/64684527/1e952392-4390-4c16-9f4a-f365b065bf22)

★ Calculated **Confidence Intervals** of the true mean of the cosine similarity difference values for text sentiments accurately predicted by the sentiment classification system.


## Adhoc Tasks

★ **Literature Review of Relevant Research Papers** to brainstorm ways for a more robust **Data Stream Mining** (Stream Learning). 

• CAMEL - Managing Data for Efficient Stream Learning: https://dl.acm.org/doi/pdf/10.1145/3514221.3517836

• Online Coreset Selection for Rehearsal-based Continual Learning: https://openreview.net/pdf?id=f9D-5WNG4Nv

• Cynical Selection of Language Model Training Data: https://arxiv.org/abs/1709.02279

• Corpus Similarity Measures Remain Robust Across Diverse Languages: https://arxiv.org/abs/2206.04332


★ **Corpus Correlation Analysis of Scholarly STEM Articles from 2018 – 2022**

**Kaggle Dataset Used:** https://www.kaggle.com/datasets/Cornell-University/arxiv

Text Data Pre-Processing > TF-IDF DTM (Pivot Table) > Dimensionality Reduction on Sparse Matrix with Principal Component Analysis (PCA) > Yearly Corpus Correlation Heat Map

![image](https://github.com/adharshasam/SentiStream/assets/64684527/cd6fb63e-6b15-49ae-af58-00032b4a4b0b)
