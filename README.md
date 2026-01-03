# Customer Churn Prediction Project
## Overview
Customer churn is a significant challenge for subscription-based businesses, as losing customers directly impacts revenue and long-term growth. In this project, I developed a machine learning based classification approach to predict which customers are most likely to churn. The primary objective was not only to build an accurate predictive model, but also to generate insights that can support proactive customer retention strategies.
Rather than reacting after customers leave, this project focuses on identifying high risk customers early so that targeted actions—such as improved customer support or retention offers can be implemented. The analysis follows the full data science process, including business understanding, data preparation, modeling, evaluation, and interpretation of results, with an emphasis on clear communication to non-technical stakeholders.
## Business and Data Understanding
### Stakeholder Audience
The primary stakeholders for this project are a telecommunications company’s **customer retention and customer experience teams**. These teams are responsible for reducing churn, improving customer satisfaction, and maximizing customer lifetime value. From a business perspective, the key question is not just *why* customers churn, but *which* customers are most at risk of leaving so that limited resources can be focused where they will have the greatest impact.
### Dataset Choice 
I used a telecom customer dataset containing information on **3,333 customers**. The dataset includes variables related to customer usage patterns, service plans, charges, and customer service interactions. The target variable is **churn**, indicating whether a customer left the service or remained active.
This dataset was well suited for the project because;
- Churn is a **binary outcome**, making it appropriate for classification modeling
- The features reflect realistic business drivers, such as usage, pricing, and customer experience
- The dataset contains a **class imbalance**, with approximately 14–15% of customers churning, which reflects real-world churn behavior and requires thoughtful metric selection
## Modeling
I approached modeling as an **iterative process**, starting with simple, interpretable models and progressing to more flexible models to improve performance.
First, I established a **baseline classification model** to understand how well churn could be predicted using a straightforward approach. This baseline provided a reference point for evaluating improvements and ensured that more complex models were justified.
Next, I explored more advanced models and tuned their settings to better capture non-linear relationships in the data. Throughout this process, I carefully prepared the data to avoid leakage by applying transformations only to the training data and then consistently applying them to the test data.
The final model was selected based on its ability to balance business priorities;
- Identifying as many churners as possible
- Avoiding unnecessary targeting of loyal customers
- Performing reliably on unseen data
Rather than focusing on technical complexity, model selection was guided by how useful the predictions would be in a real business setting.
## Evaluation
Model evaluation focused on **business-relevant classification metrics**, with particular emphasis on **recall**. Recall measures how many of the customers who actually churned were correctly identified by the model. From a business standpoint, missing a churner represents a lost opportunity to intervene, making recall a critical metric.
I evaluated model performance using a holdout test set to ensure that results reflected real-world predictive ability. The final model demonstrated a strong improvement over the baseline, successfully identifying a majority of churners while maintaining high overall accuracy.
In addition to numerical metrics, I examined a confusion matrix to better understand the types of errors being made. This helped translate model performance into practical implications, such as how often the business might reach out to customers who are not at risk versus how often true churners are successfully flagged.
I also analyzed feature importance to understand which factors contributed most to churn predictions. These insights helped connect the model’s output back to actionable business drivers.
## Conclusion
This project demonstrates how classification modeling can be used to support proactive customer retention efforts. By identifying customers who are most likely to churn, the business can move from reactive responses to targeted, data-driven interventions.
Key insights from the analysis indicate that;
- High usage and high charges are strong indicators of churn risk
- Frequent customer service interactions signal dissatisfaction
- Certain service plans, including international plans, are associated with higher churn rates
These findings suggest clear opportunities for action, such as improving service quality for high-contact customers and reviewing pricing structures for heavy users.
Overall, this project highlights the value of combining machine learning with business context. While the model itself is an important tool, its true value lies in how the insights are translated into strategic decisions that reduce churn, improve customer experience, and protect long-term revenue.
