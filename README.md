McCurr Consultancy is an MNC that has thousands of employees spread across the globe. The company believes in hiring the best talent available and retaining them for as long as possible. A huge amount of resources is spent on retaining existing employees through various initiatives. The Head of People Operations wants to bring down the cost of retaining employees. For this, he proposes limiting the incentives to only those employees who are at risk of attrition. As a recently hired Data Scientist in the People Operations Department, you have been asked to identify patterns in characteristics of employees who leave the organization. Also, you have to use this information to predict if an employee is at risk of attrition. This information will be used to target them with incentives.

### Objective :

* To identify which are the different factors that drive attrition.
* Make a model to predict the attrition.


### Dataset :
The data contains demographic details, work-related metrics and attrition flag.

* EmployeeNumber - Employee Identifier
* Attrition - Did the employee attrite?
* Age - Age of the employee
* BusinessTravel - Travel commitments for the job
* DailyRate - Data description not available**
* Department - Employee Department
* DistanceFromHome - Distance from work to home (in km)
* Education - 1-Below College, 2-College, 3-Bachelor, 4-Master,5-Doctor
* EducationField - Field of Education
* EmployeeCount - Employee Count in a row
* EnvironmentSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
* Gender - Employee's gender
* HourlyRate - Data description not available**
* JobInvolvement - 1-Low, 2-Medium, 3-High, 4-Very High
* JobLevel - Level of job (1 to 5)
* JobRole - Job Roles
* JobSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
* MaritalStatus - Marital Status
* MonthlyIncome - Monthly Salary
* MonthlyRate - Data description not available**
* NumCompaniesWorked - Number of companies worked at
* Over18 - Over 18 years of age?
* OverTime - Overtime?
* PercentSalaryHike - The percentage increase in salary last year
* PerformanceRating - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
* RelationshipSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
* StandardHours - Standard Hours
* StockOptionLevel - Stock Option Level
* TotalWorkingYears - Total years worked
* TrainingTimesLastYear - Number of training attended last year
* WorkLifeBalance - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
* YearsAtCompany - Years at Company
* YearsInCurrentRole - Years in the current role
* YearsSinceLastPromotion - Years since the last promotion
* YearsWithCurrManager - Years with the current manager

EDA ANALYSIS:
Age Distribution:

Pro: The company has a balanced age range, with most employees between 30-50.
Con: There might be a lack of younger employees (under 30) for fresh perspectives.
Improvement: Consider targeted recruitment of younger professionals to balance the workforce.


Compensation (Daily/Hourly/Monthly Rate):

Pro: The uniform distribution suggests fair compensation across levels.
Con: Lack of clear salary bands might lead to pay inequities.
Improvement: Implement structured pay scales to ensure consistency and fairness.


Distance From Home:

Pro: Most employees live close to work, potentially reducing commute stress.
Con: Limited geographic diversity in the workforce.
Improvement: Offer remote work options to attract talent from diverse locations.


Education:

Pro: Diverse educational backgrounds with concentrations at levels 2 and 4.
Con: Potential skill gaps if education levels don't match job requirements.
Improvement: Provide training programs to bridge skill gaps and support career development.


Job Involvement and Satisfaction:

Pro: High levels indicate an engaged workforce.
Con: Could mask underlying issues if not accurately reported.
Improvement: Conduct regular, anonymous surveys to verify and maintain high satisfaction levels.


Job Level:

Pro: Pyramid structure with more employees at lower levels is typical.
Con: Potential for career stagnation at lower levels.
Improvement: Implement clear career progression paths and mentorship programs.


Monthly Income:

Pro: Right-skewed distribution is normal in most organizations.
Con: Large income disparity could lead to dissatisfaction.
Improvement: Ensure competitive pay at all levels and transparent communication about compensation.


Number of Companies Worked:

Pro: Most employees have some diverse experience.
Con: Potential lack of fresh perspectives from other industries.
Improvement: Consider hiring from diverse industry backgrounds for certain roles.


Percent Salary Hike:

Pro: Consistent salary increases for most employees.
Con: Narrow range of increases might not reward high performers adequately.
Improvement: Implement performance-based bonus structures to complement salary hikes.


Performance Rating:

Pro: Most employees are rated positively.
Con: Potential rating inflation or lack of differentiation.
Improvement: Train managers on objective performance evaluation and use a more granular rating scale.


Total Working Years:

Pro: Good mix of experience levels.
Con: Potential skill obsolescence for long-term employees.
Improvement: Offer continuous learning opportunities and cross-functional projects.


Years at Company, in Current Role, and Since Last Promotion:

Pro: Indicates a dynamic environment with recent changes.
Con: High turnover or frequent role changes could disrupt continuity.
Improvement: Balance job rotations with stability, and ensure clear career progression paths.


Work-Life Balance:

Pro: Most employees report good work-life balance.
Con: Uniform high scores might not reflect reality accurately.
Improvement: Investigate actual working hours and stress levels, implement wellness programs.


Stock Option Level:

Pro: Offers financial incentives to some employees.
Con: Many employees at level 0 might feel less invested in company success.
Improvement: Consider broader employee stock ownership plans or alternative long-term incentives

Understanding the Metrics:

Before we dive into the best model, let's clarify what each metric represents:

Accuracy: The overall proportion of correct predictions.
Recall: The proportion of positive cases correctly identified.
Precision: The proportion of positive predictions that were actually correct.
F1-score: The harmonic mean of precision and recall, providing a balanced measure.
Evaluating the Training and Testing Performance:

Training Performance:

All models achieved perfect accuracy, recall, precision, and F1-score. This might indicate overfitting, where the models have learned the training data too well and might not generalize well to unseen data.
Testing Performance:

Accuracy: Weighted Random Forest Classifier and Random Forest Classifier have the highest accuracy.
Recall: Decision Tree Estimator, Bagging Estimator, and Random Forest Estimator have the highest recall.
Precision: Weighted Bagging Classifier has the highest precision.
F1-score: Weighted Random Forest Classifier has the highest F1-score.
Considering Overfitting:

Given the perfect training performance and potential overfitting, we should focus on the testing performance.

Choosing the Best Model:

Based on the testing performance, the Weighted Random Forest Classifier appears to be the most promising model. It has the highest F1-score, a good balance of precision and recall, and competitive accuracy.

Additional Considerations:

Interpretability: If interpretability is important, the Decision Tree Estimator might be a good choice, as it's easier to understand its decision-making process.
