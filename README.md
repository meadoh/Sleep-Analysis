## Executive Summary

The aim of this analysis is to see if we can predict the prescence of common health conditons using only the sleep-based features in our dataset. Participants in the initial study were asked if they had been treated for any of the following: arthritis, heart disease, diabetes, heartburn/GERD, depression and anxiety. These have been combined into one target column: has_condition. Only sleep-related features will be used. Features used are usual hours of sleep per night, whether or not they have an unconventional wake time, naps per month, and average length of naps. The purpose of modeling will be to predict a person's overall health on sleep-based features alone.

The classification models that will be tested are Logistic Regression, KNN and Random Forest. Good accuracy and f1 scores will show the relationship between sleep and overall health. Out of the three models, Random Forest performed the best with an accuracy of 64% and 61%, with the majority of the predictions being true positives/negatives. This would beat the baseline (55%) and thus shows a relationship between sleep and overall health.


**Data Description**
Data was captured via cold-calling by WBA Market research for the National Sleep Foundation in 2008. The questionnaire used by the interviewers is provided below in the Dataset section. 


**Dataset**
https://www.sleepfoundation.org/professionals/sleep-americar-polls/2008-sleep-performance-and-workplace
https://www.sleepfoundation.org/wp-content/uploads/2018/10/SIAQuestionnaire2008.pdf

**Risks and limitations:**
- There may be too few observations for meaningful predictions.
- Not enough sleep specific features to test on.

**Data Dictionary**

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**awake_time**|*object*|SIA / Questionnaire2008|Usual awake time|
|**start_work**|*object*|SIA / Questionnaire2008|Usual start work time|
|**end_work**|*object*|SIA / Questionnaire2008|Usual end work time|
|**bed_time_work_tomorrow**|*object*|SIA / Questionnaire2008|Usual bedtime on a day before a work day |
**no_work_awake_time**|*object*|SIA / Questionnaire2008|Usual awake time on a day before a non-work day|
**bedtime_no_work_tomorrow**|*object*|SIA / Questionnaire2008|Usual bedtime on a night that is not preceding a work day|
**usual_sleep_per_night**|*float*|SIA / Questionnaire2008|Usual sleep per night|
**employment_status**|*object*|SIA / Questionnaire2008|Current employment status|
**avg_weekly_hours_worked**|*float*|SIA / Questionnaire2008|Avg work hours per week|
**treated_for_heart_disease**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for heart disease|
**treated_for_high_blood_pressure**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for high blood pressure|
**treated_for_diabetes**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for diabetes|
**treated_for_heartburn_GERD**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for heartburn/GERD|
**treated_for_arthritis**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for arthritis|
**treated_for_depression**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for depression|
**treated_for_anxiety**|*boolean*|SIA / Questionnaire2008|If the patient is being treated for anxiety|
**marital_status**|*object*|SIA / Questionnaire2008|Current marital status|
**highest_edu**|*object*|SIA / Questionnaire2008|Highest level of education|
**single_dual_household**|*object*|SIA / Questionnaire2008|Single or dual income household|
**house_hold_income_bracket**|*object*|SIA / Questionnaire2008|Income bracket)|
**age**|*float*|SIA / Questionnaire2008|Age of participant|