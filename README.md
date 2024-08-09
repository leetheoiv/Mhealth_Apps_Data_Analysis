# Mhealth Apps Data Analysis
# Final Product
![Example Image](https://github.com/leetheoiv/Mhealth_Apps_Data_Analysis/blob/main/Mhealth%20Dashboard.png)
# Data Source 
https://www.kaggle.com/datasets/subhamsarkar2002/mobile-health-apps-evaluation-dataset
# Tools Used
- Python (Pandas, Scipy)
- PowerBI

## Overview
- Mental health apps, also known as mHealth apps, are designed to help users manage mental health issues such as depression, anxiety, and other conditions. These apps are required to adhere to FDA regulations, but this doesn't necessarily mean that developers undergo rigorous testing before publishing their apps or acquiring users. The primary obligation is to ensure compliance with FDA guidelines related to health applications. Although numerous mental health apps are available on app stores, many lack clinical testing, which raises questions about their efficacy. In this project, I developed a dashboard to review and analyze mHealth apps using a dataset provided by The Machine Learning for Learning Health Systems Research Lab, with the goal of exploring the landscape of these applications.
## Research Questions
1. How many applications have been made with clinicians involved in the process?
    1. Out of all the applications reviewed, approximately 64% lacked any involvement from clinical professionals during their development. This statistic is concerning, considering the critical role clinicians play in ensuring that these apps deliver accurate feedback and information to patients. Clinician input is essential not only for maintaining the quality and reliability of health-related apps but also for fostering trust and confidence among users in their healthcare journey.
    2. Does this statistic generalize to the broader population of health applications, or is it specific to the sampled apps?
        1. The estimated proportion of apps developed without clinical professional involvement, approximately 64%, falls within a 95% confidence interval ranging from 56.21% to 72.26%. This interval suggests that the sample statistic is likely reflective of the broader population of health-related applications. However, further studies would be beneficial to confirm this finding across a wider range of apps and contexts.
           
2. How many apps are FDA compliant?
    1. Approximately 99% of the apps in this sample are not FDA compliant. The FDA classifies mobile medical apps into three categories based on risk: Class I (low risk, general health information), Class II (moderate risk, requires special controls), and Class III (high risk, requires premarket approval). The high rate of non-compliance suggests that these apps may fall into the low-risk Class I category. However, it's also possible that developers are either unaware of FDA requirements or choose to disregard them. Further investigation is needed to determine the underlying reasons for this widespread non-compliance 

3. Is there a difference in clinician  involvement when the developer is a non-for profit, government funded, or for-profit?
    1. Considering the larger representation of for-profit companies among app developers, there is a noticeable disparity in clinician involvement across different developer types. Generally, there appears to be lower clinical expert engagement observed among for-profit and individual developers compared to non-profit and government-funded developers. This trend suggests that the involvement of clinical experts may vary significantly depending on the developer's organizational structure and funding source.
        
4. What is the difference in the average number of app ratings when a clinical expert is involved in development or isn’t?
    1. When a clinician is involved in app development, we observe a notable difference in average ratings between iOS and Android platforms. Specifically, apps with clinician involvement tend to receive approximately 44% more ratings on iOS compared to Android. This inverse relationship suggests that clinician input may influence user engagement and feedback differently across these platforms
    2.  Are these differences statistically significant?

**Hypotheses:**
- \( H_0 \): There is no association between clinical expert involvement in app development and the number of iOS ratings.
- \( H_1 \): There is an association between clinical expert involvement in app development and the number of iOS ratings.

**Results:**
- T-test statistic: 0.925
- p-value: 0.365
- Degrees of freedom: 21.21

Given these results, we fail to reject the null hypothesis at an alpha level of 0.05. 
This suggests that there is insufficient evidence to conclude that clinician 
involvement significantly affects the number of iOS ratings.

            
**Hypotheses:**
- \( H_0 \): There is no association between clinical expert involvement in app development and the number of Android ratings.
- \( H_1 \): There is an association between clinical expert involvement in app development and the number of Android ratings.

**Results:**
- T-test statistic: 0.993
- p-value: 0.334
- Degrees of freedom: 17.00

Based on these results, we also fail to reject the null hypothesis at an alpha level of 0.05.
This indicates that there is insufficient evidence to suggest that clinician 
involvement significantly influences the number of Android ratings.

            
5. Is there a difference between developer categories and the average app rating?

**Hypotheses:**
- \( H_0 \): There is no difference in average app rating among different developer categories.
- \( H_1 \): There is a difference in average app rating among different developer categories.

**ANOVA Results:**
- For iOS Average Rating:
  - p-value: 0.93
- For Android Average Rating:
  - p-value: 0.98
- Significance level (alpha): 0.05

Based on the ANOVA results, we fail to reject the null hypothesis for both iOS and Android average ratings at a significance level of 0.05. This suggests that there is insufficient evidence to conclude that there is a significant difference in average app rating across different developer categories. Therefore, we must accept the null hypothesis and reject the alternative hypothesis in both cases.

