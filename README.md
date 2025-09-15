# SyriaTel Customer Churn Analysis and predictive Modeling
![Alt text](https://your-image-host.com/image.png)
source: https://syrianobserver.com/uncategorized/syriatel-receivership-to-be-lifted-soon-new-ceo-appointed.html
## Introduction
"For this analysis, we will use the dataset: [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) ,which contains comprehensive information about churn, customer service calls, account length (the number of days a client has had their account active), total calls per day, daily charge, etc.\n",
        "\n",
        "The goal is to help the telecom business reduce the amount of money lost due to customer churn and build a model that will help predict the type of client that will likely do so."
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Y5qHoxpotuOz"
      },
      "source": [
        "## Methodology\n",
        "#### **Exploratory Data Analysis (EDA)**\n",
        "This step is essential to make sure things go smoothly and geting a good understanding of the dataset:\n",
        "- dataset overview\n",
        "- data cleaning\n",
        "- data/ Business understanding\n",
        "#### **Statistical modeling**\n",
        "In this part we will use the insight that we get from the exploratory data analysis to make a predictive model of SyriaTel Customer churn.\n",
        "#### **Major questions**\n",
        "Questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding. They will be answered by our model.(the recommendations will be provided along answering the major questions)\n",
        "#### **Summary**\n",
        "#### **Contact information**"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "## Exploratory Data Analysis (EDA)\n"
      ],
      "metadata": {
        "id": "EJAGcYA3__7R"
      }
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qQGtceTymZkc"
      },
      "source": [
        "#### **Dataset overview**\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "####**Data cleaning**"
      ],
      "metadata": {
        "id": "MyPCJZWICMxs"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "### Data/ Business understanding\n",
        "- check for class imbalance\n",
        "- understanding"
      ],
      "metadata": {
        "id": "qyaCQbkDDppO"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Data Understanding**\n",
        "The dataset tracks SyriaTel customers’ phone activity and contract details, including location, phone number, international and voicemail plans, and stored messages. It also records service usage—minutes, calls, and charges across day, evening, night, and international periods—plus customer service interactions. The target variable churn indicates whether a customer canceled their subscription. The goal is to identify patterns that predict churn.\n",
        "\n",
        "####**Business Understanding**\n",
        "Customer churn poses a financial risk for SyriaTel, making retention a priority. Understanding why customers leave—whether due to service quality, pricing, or support—is key. By analyzing usage and subscription data, the company can identify at-risk customers and build a predictive model to guide proactive retention strategies.\n",
        "\n",
        "\n"
      ],
      "metadata": {
        "id": "ib_jfwydAGdu"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## Statistical modeling\n",
        "- baseline model\n",
        "- perfecting model\n",
        "- final model\n",
        "\n",
        "each model will be followed by an analysis of it's  performance."
      ],
      "metadata": {
        "id": "BSnDNjujIKnP"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Baseline model**\n",
        "we will  use Logistic regression because it’s simple, interpretable, and well-suited for binary classification.\n"
      ],
      "metadata": {
        "id": "up7144JDuEp9"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Analysis**\n",
        "the baseline model performs well enough to predict non churn but very poorly on churn (with low precision, accuracy and F-1 score) . and since we are mostly interested in churn we will keep tuning the model."
      ],
      "metadata": {
        "id": "s2v6jr6gnZFv"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "### perfecting model.\n",
        "we will have different version of the model tuned so that it can perform as best as possible.\n",
        "In the end all model will be represented on a ROC curve for a better comparaison."
      ],
      "metadata": {
        "id": "mvjq_4Oev-nH"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Model 2**"
      ],
      "metadata": {
        "id": "7IqatVEqLQde"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "####**Analysis**\n",
        "This model showed improved performance in identifying churn, with recall for True rising from 0.09 in the baseline to 0.64  and a really higher F1-score."
      ],
      "metadata": {
        "id": "sOamu6acFKGb"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Model 3**"
      ],
      "metadata": {
        "id": "9Qe-iyCTLq4W"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Analysis**\n",
        "this model performs better in precision for both True and False and the f1-score has come from 0.37 to 0.44."
      ],
      "metadata": {
        "id": "QDyxDO3MKvBP"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Model 4**"
      ],
      "metadata": {
        "id": "N7VsdrtYMTpT"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Analysis**\n",
        "this model perform great overall whether it's precision or recall. it is also likely to perfom well on unseen data. with an AUC of 0.93 it's the best of all  the models which is why we will keep it."
      ],
      "metadata": {
        "id": "Hs2Lji3nW8jO"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## Major questions\n",
        "\n",
        "bellow are questions that the management Team of SyriaTel might want to ask.These questions are based on our data and business understanding .They will be answered by our model.\n",
        "- What customers are most likely to churn ?\n",
        "- Do customer service calls play a significant role in churn?\n",
        "- Based on our analysis, what are actionable strategies to reduce churn?\n",
        "- Which specific states have the highest churn rates?\n"
      ],
      "metadata": {
        "id": "lPpr7REKtmUO"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **What customers are most likely to churn ?**"
      ],
      "metadata": {
        "id": "EPVWxJaMj3OK"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Note**: the customers that make the most international  plan along with the most customer service calls are the most likely to churn.\n",
        "#### **Recommendation**: the company may want to do additional data gathering on international calls, and try to see which of it's aspect botters client."
      ],
      "metadata": {
        "id": "bbp0DYCnf-8u"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Do customer service calls play a significant role in churn?**\n",
        "Customers that has the most customer service call are the most likely to churn. This is a sign that the customer service might still has room for improvement.\n",
        "**Recommentdation**: the company should put more effort on understanding clients problem,and fix them as effectively as possible."
      ],
      "metadata": {
        "id": "HHKbB3NBkfIq"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Based on our analysis, what are actionable strategies to reduce churn?**\n",
        "to reduce churn the company might want to give the clients a better experience on international calls. they might also want to handle customer call more effectively."
      ],
      "metadata": {
        "id": "hyIUgiL0nw9F"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Which specific states have the highest churn rates?**\n",
        "Mariland, Minesota and Virginia are the states that have the highest churn Rates.\n",
        "**Recommendation**: further data should be gathered on this specific states.Poles might be a great way to proceed."
      ],
      "metadata": {
        "id": "4_yURJeCoL2x"
      }
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "3ff85463"
      },
      "source": [
        "## Summary\n",
        "\n",
        "> For this analysis, we used the [Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download). We began with a dataset overview and performed necessary data cleaning. After cleaning, we gained a good understanding of the data and the business problem it addresses. We then developed different models to find the one that provides the best predictions on unseen data. Finally, we addressed major questions based on our analysis and provided recommendations."
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vc0gqxkK51ik"
      },
      "source": [
        "##Contact Information"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Jk9DbLk2iQMD"
      },
      "source": [
        "- First Name: Haender Michael\n",
        "\n",
        "- Last Name: Jean Louis\n",
        "\n",
        "- Email: michaelhaenderjeanlouis@gmail.com\n",
        "\n",
        "- Phone Number: +509 41 75 0264\n",
        "\n",
        "- LinkedIn: https://www.linkedin.com/in/michael-haender-jean-louis-4b7320316?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app\n",
        "\n",
        "For further inquiries, feedback, or collaboration on this analysis, feel free to reach out. I welcome discussions and any contract to work with the head of the company's new movie team."
      ]
    }
  ],
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "display_name": "Python 3",
      "name": "python3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "nbformat": 4,
  "nbformat_minor": 0
}
