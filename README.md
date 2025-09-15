# SyriaTel Customer Churn Analysis and predictive Modeling
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/0ae85ade5aae03b04636890103a3e4dbbfed8e73/les%20images/Image%2010.jpg)
[source](https://sl.bing.net/6MZvOEjFL2) 
## Introduction
For this analysis, we will use the dataset: [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) ,which contains comprehensive information about churn, customer service calls, account length (the number of days a client has had their account active), total calls per day, daily charge, etc.

The goal is to help the telecom business reduce the amount of money lost due to customer churn and build a model that will help predict the type of client that will likely do so.
    
## Methodology

#### **Exploratory Data Analysis (EDA)**
This step is essential to make sure things go smoothly and geting a good understanding of the dataset:
- data cleaning
- data/ Business understanding
#### **Statistical modeling**
In this part we will use the insight that we get from the exploratory data analysis to make a predictive model of SyriaTel Customer churn.
#### **Major questions**
Questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding. They will be answered by our model.(recommendations will be provided along answering the major questions)
#### **Summary**
#### **Contact information**

## Exploratory Data Analysis (EDA)
#### **Data cleaning**
the dataset has no duplicates nor missing values and it was already pretty clean ,so  many other cleaning steps aren't necessary.
we just had to remove space in column name and set number as ID.
#### **Data/ Business understanding** 
After cleaning, the data was found to be imbalanced, which means there is one class that was far more recurrent in the dataset than the other.

![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/f3ea6d6049aa100aaec2457d314bdb44bca69711/les%20images/Image%202.png)
  
#### **Data Understanding**
The dataset tracks SyriaTel customers’ phone activity and contract details, including location, phone number, international and voicemail plans, and stored messages. It also records service usage—minutes, calls, and charges across day, evening, night, and international periods—plus customer service interactions. The target variable churn indicates whether a customer canceled their subscription. The goal is to identify patterns that predict churn.
#### **Business Understanding**
Customer churn poses a financial risk for SyriaTel, making retention a priority. Understanding why customers leave—whether due to service quality, pricing, or support—is key. By analyzing usage and subscription data, the company can identify at-risk customers and build a predictive model to guide proactive retention strategies.
      
  

## Statistical modeling
- baseline model
- perfecting model
- final model
        
each model will be followed by an analysis of it's  performance.

#### **Baseline model**
we will  use Logistic regression because it’s simple, interpretable, and well-suited for binary classification and we will use the classification matrix to compare the model performance .
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/9be15a5355f48ee990d4329febc2dbab26fec7ef/les%20images/image%203.png)
#### **Analysis**
the baseline model performs well enough to predict non churn but very poorly on churn. As we can see the model predicted a lot of non churn while these customers actually churned. the data did not predict effectively the customer that are likely to churn. It has a high rate of false negative(predicting they will not churn while they actually do) so we won't chose this model.
### perfecting model.
we will have different version of the model tuned so that it can perform as best as possible.
In the end all model will be represented on a ROC curve for a better comparaison.
    
#### **Model 2**
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/9be15a5355f48ee990d4329febc2dbab26fec7ef/les%20images/image%204.png)
#### **Analysis**
This model showed improved performance in identifying churn, starting from 10 good prediction on the baseline to 74 on the model. There are much more true positive( prediction = actual occurence), yet the model gives a lot of false positive, which mean even though they perform well on Identifying most of the churn they still classify some important cases of non-churn as churn.

#### **Model 3**
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/23b5e9a9e5b655ddcff4690a9b2b51714f682453/Model%203.png)
#### **Analysis**
this model performs better  than the previous ones with higher rate of true negative and higher rate of true positive. That means the model performs well overall on saying true information.

#### **Model 4**
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/4df43d43624a7d1525de6e569700cc10506faac2/les%20images/Image%205.png)
#### **Analysis**
this model perform great overall whether it's precision or recall. it is also likely to perfom well on unseen data. with an AUC of 0.93 it's the best of all  the models which is why we will keep it.
Below is it's graph in comparaison with the other.
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/4df43d43624a7d1525de6e569700cc10506faac2/les%20images/Image%206.png)
## Major questions
    
bellow are questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding .They will be answered by our model.
- What customers are most likely to churn ?
- Do customer service calls play a significant role in churn?
- Based on our analysis, what are actionable strategies to reduce churn?
- Which specific states have the highest churn rates?
  
#### **What customers are most likely to churn ?**
![Alt text](https://github.com/Haender-Michael/SyriaTel-Customer-Churn-Analysis-and-predictive-Modeling/blob/4df43d43624a7d1525de6e569700cc10506faac2/les%20images/Image%207.png)
#### **Note** :  the customers that make the most international  plan along with the most customer service calls are the most likely to churn.
#### **Recommendation**:  the company may want to do additional data gathering on international calls, and try to see which of it's aspect botters client.
    
#### **Do customer service calls play a significant role in churn?**
Customers that has the most customer service call are among the most likely to churn. This is a sign that the customer service might still has room for improvement.

**Recommentdation**: the company should put more effort on understanding clients problem,and fix them as effectively as possible.
the call from customers should be handle with tact, as customer satisfaction is likely to  reduce churn.

**Based on our analysis, what are actionable strategies to reduce churn?**
to reduce churn the company might want to give the clients a better experience on international calls. they might also want to handle customer call more efficiently. since clients with most international and customer service call churn.An holistic approach would also be great since clients that churns may have many of the caracteristics affecting churn. All of the most recurrent caracteristic in customer that stops taking service at the company should be addressed.
    
**Which specific states have the highest churn rates?**
Mariland, Minesota and Virginia are the states that have the highest churn Rates.
**Recommendation**: further data should be gathered on this specific states.Poles might be a great way to proceed.

## Summary
For this analysis, we used the [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download). We began with a dataset overview and performed necessary data cleaning. After cleaning, we gained a good understanding of the data and the business problem it addresses. We then developed different models to find the one that provides the best predictions on unseen data. Finally, we addressed major questions based on our analysis and provided recommendations.

## Contact Information"
   
- First Name: Haender Michael
- Last Name: Jean Louis
- Email: michaelhaenderjeanlouis@gmail.com
- Phone Number: +509 41 75 0264
- LinkedIn: https://www.linkedin.com/in/michael-haender-jean-louis-4b7320316?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app
For further inquiries, feedback, or collaboration on this analysis, feel free to reach out. I welcome discussions and any contract to work with the head of the company's new movie team.
     
