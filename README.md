## Introduction
The objective of this research is to analyse the public opinion of the Israel–Palestine conflict by examining online discussions and identifying sentiment patterns, key themes and commonly used language associated with each position. 
The main research questions are: 
What are the key terms used to express the two opposing positions?
What common topics appear across both types of comments?

This study focuses on: 
Sentiment analysis: classification of opinions expressed toward Israel and Palestine
Exploratory analysis: identification of themes, patterns and relationship between words

## Data collection
The dataset consists of English language comments reflecting debates and opinions supporting either israel or Palestine, collected from Reddit platform.
Examples of discussions include: 
•	“What is your opinion on the Israel–Gaza war?”
•	“What is the deal with the Israel–Palestine conflict? Who is right, who is wrong?”
•	“Has anyone noticed a shift in public opinion regarding the Gaza conflict?”
•	“How have your views on the Israel–Palestine conflict changed in the last month?”
Since the research focuses on events following the 2023 escalation, comments were extracted between the timeframe of December 2023 – June 2024. The total number of the comments is 1000. 



## Data Cleaning
Reddit is known to enable anonymous participation, which often leads to open, honest and highly diverse discussions. As a result, many comments may deviate from the research topic, making automated analysis challenging. 
In order to ensure relevance and accuracy, manual data was performed instead of an automated one. For further analysis only comments explicitly expressing positions toward Isarel or Palestine were retained. Off topic or ambiguous comments were removed.
Comments were manually labeled into two categories: 
•	Pro-Israel  (e.g., “I support Israel”, “Zionist”, “Palestinian terrorism”)
•	Pro-Palestine (e.g., “I stand with Palestine”, “Anti-Zionist”, “Genocide”, “Anti-Hamas”)

Criticism of Israel involving terrorism or military actions was also considered supportive of the pro-Palestine position.
After filtering the final dataset remained with 400 comments:
•	207 Pro-Palestine
•	193 Pro-Israel

## Data preprocessing
Text preprocessing steps included: 
•	Removal of punctuation and special characters
•	Conversion to lowercase
•	Stop-word removal
•	Tokenization
•	Lemmatization to reduce words to their base form

## Sentiment Analysis
Text representation was performed using a Document-Term Matrix (DTM) with a vocabulary size of 6000 words. 

The dataset was split in 80% training data and 20% testing data. 

Two classification algorithms were applied, XGBoost Classifier and Support Vector Machine (SVM).

## XGBoost Results
•	Precision: 0.73 (Pro-Palestine), 0.67 (Pro-Israel)

•	Recall: 0.66 (Pro-Palestine), 0.74 (Pro-Israel)

•	F1-score: 0.69 (Pro-Palestine), 0.71 (Pro-Israel)

•	Overall Accuracy: 70%

The model demonstrates balanced performance across both classes, though improvements are possible, particularly in recall and precision.

## Support Vector Machine Results

•	Precision: 0.74 (Pro-Palestine), 0.67 (Pro-Israel)

•	Recall: 0.63 (Pro-Palestine), 0.77 (Pro-Israel)

•	F1-score: 0.68 (Pro-Palestine), 0.71 (Pro-Israel)

•	Overall Accuracy: 70%

## Model Comparison
Both models show similar performance with minor differences:

•	SVM achieves slightly higher precision for the Pro-Palestine class

•	SVM also shows better recall for the Pro-Israel class

•	XGBoost maintains more balanced recall across both classes

Overall accuracy and macro averages are identical. While SVM performs marginally better in certain metrics, the differences are relatively minor.

The research also includes a co-occurrence network analysis to identify relationships between frequently used words and uncover thematic structures within the discussions. 

## Conclusions
Regarding the results of the exploratory analysis, the most frequently used words are related to supporting positions, as well as to war and violence. Both categories of opinions, those about Israel and those about Palestine, share common themes of freedom and war, as well as sympathy and frustration.

This analysis aimed to examine the way people express their opinions regarding their positions on Israel and Palestine. In doing so, I sought to focus on comments posted on the Reddit platform, more specifically to emphasize the nature of the discourse and the authors’ expressions. Both pro-Israel and pro-Palestine supporters use emotional and moral arguments to support their points of view. While both models show reasonable performance, further improvements could be achieved through larger datasets, more advanced feature representations, or deep learning approaches.
