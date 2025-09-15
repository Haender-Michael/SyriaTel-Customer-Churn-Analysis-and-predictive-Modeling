# SyriaTel Customer Churn Analysis and predictive Modeling
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/0ae85ade5aae03b04636890103a3e4dbbfed8e73/les%20images/Image%2010.jpg)
source: https://syrianobserver.com/uncategorized/syriatel-receivership-to-be-lifted-soon-new-ceo-appointed.html
## Introduction
For this analysis, we will use the dataset: [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) ,which contains comprehensive information about churn, customer service calls, account length (the number of days a client has had their account active), total calls per day, daily charge, etc.

The goal is to help the telecom business reduce the amount of money lost due to customer churn and build a model that will help predict the type of client that will likely do so.
    
## Methodology

#### **Exploratory Data Analysis (EDA)**
This step is essential to make sure things go smoothly and geting a good understanding of the dataset:
- dataset overview
- data cleaning
- data/ Business understanding
#### **Statistical modeling**
In this part we will use the insight that we get from the exploratory data analysis to make a predictive model of SyriaTel Customer churn.
#### **Major questions**
Questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding. They will be answered by our model.(the recommendations will be provided along answering the major questions)\n",
#### **Summary**
#### **Contact information**"

## Exploratory Data Analysis (EDA)
#### **Data cleaning**
### Data/ Business understanding
- check for class imbalance
- understanding
  
#### **Data Understanding**
The dataset tracks SyriaTel customers’ phone activity and contract details, including location, phone number, international and voicemail plans, and stored messages. It also records service usage—minutes, calls, and charges across day, evening, night, and international periods—plus customer service interactions. The target variable churn indicates whether a customer canceled their subscription. The goal is to identify patterns that predict churn.
####**Business Understanding**
Customer churn poses a financial risk for SyriaTel, making retention a priority. Understanding why customers leave—whether due to service quality, pricing, or support—is key. By analyzing usage and subscription data, the company can identify at-risk customers and build a predictive model to guide proactive retention strategies.
      
  

## Statistical modeling\n",
- baseline model
- perfecting model
- final model
        
each model will be followed by an analysis of it's  performance.

#### **Baseline model**
we will  use Logistic regression because it’s simple, interpretable, and well-suited for binary classification.

#### **Analysis**
the baseline model performs well enough to predict non churn but very poorly on churn (with low precision, accuracy and F-1 score) . and since we are mostly interested in churn we will keep tuning the model.
    
### perfecting model.
we will have different version of the model tuned so that it can perform as best as possible.
In the end all model will be represented on a ROC curve for a better comparaison.
    
#### **Model 2**
    
####**Analysis**
This model showed improved performance in identifying churn, with recall for True rising from 0.09 in the baseline to 0.64  and a really higher F1-score.
     
#### **Model 3**
    
#### **Analysis**
this model performs better in precision for both True and False and the f1-score has come from 0.37 to 0.44."
    
#### **Model 4**

#### **Analysis**
this model perform great overall whether it's precision or recall. it is also likely to perfom well on unseen data. with an AUC of 0.93 it's the best of all  the models which is why we will keep it.

## Major questions
    
bellow are questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding .They will be answered by our model.
- What customers are most likely to churn ?
- Do customer service calls play a significant role in churn?
- Based on our analysis, what are actionable strategies to reduce churn?
- Which specific states have the highest churn rates?\n
  
#### **What customers are most likely to churn ?**
    
#### **Note**: the customers that make the most international  plan along with the most customer service calls are the most likely to churn.\n",
#### **Recommendation**: the company may want to do additional data gathering on international calls, and try to see which of it's aspect botters client.
    
#### **Do customer service calls play a significant role in churn?**
"Customers that has the most customer service call are the most likely to churn. This is a sign that the customer service might still has room for improvement.
**Recommentdation**: the company should put more effort on understanding clients problem,and fix them as effectively as possible."

**Based on our analysis, what are actionable strategies to reduce churn?**\n",
to reduce churn the company might want to give the clients a better experience on international calls. they might also want to handle customer call more effectively."
    
**Which specific states have the highest churn rates?**\n",
Mariland, Minesota and Virginia are the states that have the highest churn Rates.\n",
**Recommendation**: further data should be gathered on this specific states.Poles might be a great way to proceed."

## Summary
For this analysis, we used the [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download). We began with a dataset overview and performed necessary data cleaning. After cleaning, we gained a good understanding of the data and the business problem it addresses. We then developed different models to find the one that provides the best predictions on unseen data. Finally, we addressed major questions based on our analysis and provided recommendations."

## Contact Information"
   
- First Name: Haender Michael
- Last Name: Jean Louis\n",
- Email: michaelhaenderjeanlouis@gmail.com
- Phone Number: +509 41 75 0264\n",
- LinkedIn: https://www.linkedin.com/in/michael-haender-jean-louis-4b7320316?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app
For further inquiries, feedback, or collaboration on this analysis, feel free to reach out. I welcome discussions and any contract to work with the head of the company's new movie team."
     
