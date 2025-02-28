# Telecom

This dataset is used for churn prediction, a supervised learning problem where we predict whether a customer will churn (1) or stay (0). 
The dataset contains customer details, usage statistics, and plan information that can help in understanding customer behavior.

Column Description:

state		              State of the customer (numeric code)
account_length	    	Number of months the customer has been with the company
area_code	          	Area code of the customer
phone_number	      	Unique phone number identifier
intl_plan	            Has an international plan, 0 = No plan
voice_mail_plan	int64 Has a voicemail plan, 0 = No plan
number_vmail_messages	Number of voicemail messages received
total_day_minutes	   	Total minutes of daytime calls
total_day_calls		    Number of daytime calls
total_day_charge	  	Total charge for daytime calls
total_eve_minutes	  	Total minutes of evening calls
total_eve_calls	    	Number of evening calls
total_eve_charge	  	Total charge for evening calls
total_night_minutes		Total minutes of night calls
total_night_calls	  	Number of night calls
total_night_charge		Total charge for night calls
total_intl_minutes		Total minutes of international calls
total_intl_calls	  	Number of international calls
total_intl_charge	  	Total charge for international calls
number_customer_service_calls		Number of calls made to customer service
churned	               Customer is churned or not

This dataset is suitable for supervised Learning, Churned column is target column as its depended on other columns, and rest of the column in the dataset as independent. So this dataset is sutable for
Supervised Learning with Categorical Task.

Data PreProcessing for Machine Learning:
The dataset contains categorical columns stored as object data types, which need to be converted to numerical values for machine learning models. 

The following transformations were applied:
Phone Number 
Initially stored as an object, converted to an int64 data type.
International Plan (intl_plan) & Voicemail Plan (voice_mail_plan) Stored as object with values "yes" and "no". Converted using .replace({"yes": 1, "no": 0}).
State (state) column, converted using Ordinal Encoding to map unique state names to numerical values.
Churn Boolean (True/False) column, converted to int64 using .astype(int), where True → 1 and False → 0.

