ANALYSIS OF COUNTERFACTUAL EXAMPLES IN LINE WITH CJEU’S CASE LAW ON RIGHT TO EXPLANATION UNDER GDPR 

A.	ABSTRACT

This study examines the role of counterfactual explanations in fulfilling the right to explanation under the General Data Protection Regulation (GDPR) in light of the Court of Justice of the European Union’s (CJEU) decision in Case C-203/22 (CK). It analyses how legal requirements concerning transparency, intelligibility, and meaningful information can be operationalized in the context of automated decision-making systems based on machine learning.
The research conceptualizes the normative and distributive effects of machine learning algorithms, emphasizing their capacity to significantly affect individuals’ legal and economic positions. It applies the principles articulated by the CJEU to two concrete use cases involving supervised learning models: an employee hiring scenario and an employee attrition risk assessment. In both cases, counterfactual explanations are generated using an explainable AI (xAI) framework and translated into natural language explanations with the assistance of a Large Language Model (LLM).
The analysis demonstrates that the legal adequacy of counterfactual explanations is inherently context dependent. While counterfactual explanations may provide meaningful and actionable information where decisive variables remain within the data subject’s control, their practical value diminishes in settings dominated by controller-side discretion, even though they may still support the right to contest automated decisions. The study further shows that although LLM-generated explanations can enhance accessibility and clarity, they also introduce risks of interpretative distortion. It concludes that existing legal standards on explainability require further refinement to address the distinctive characteristics of generative AI systems.,

B.	INTRODUCTION 

Interpretability and explainability of machine learning algorithms is a hot topic in computer science, in particular for deep learning and reinforcement learning (RL) algorithms . With the emergence and common use of Large Language Models (LLMs), the explainability of machine learning algorithms has become more crucial both from technical and legal perspective. 
General Data Protection Regulation is the most important piece of legislation, concerning the legal supervision of the machine learning and AI systems. The Court of Justice of the European Union (CJEU) has made a recent decision concerning the scope of right to explanation, set forth under GDPR. As emphasis is made to counterfactual examples, we wish to implement the principles set forth by the CJEU on concrete examples.  
The Court and the legislation require that the explanation provided to the individuals (data subject) to be concise and clear. For this purpose, LLMs can be used to generate explanation for the outcome of the xAI algorithms, explaining the respective algorithm. This feature of the LLMs is worth analyzing, from a legal perspective. 
Within the scope of this research, the first step will be to define legal requirements for explanations provided for machine learning algorithms, in line with the recent case law of the  Court of Justice of the European Union (CJEU)  . The general purpose of this research is to apply general principles defined by the legislation and caselaw for right to explanation set forth under General Data Protection Regulation (GDPR) on the explanations provided by the xAI library and LLM model, and analyze whether these explanations satisfy the legal requirements, in terms of their content. The accuracy and performance of the respective machine learning algorithm(s),  and the fidelity of the counterfactual examples generated is out of scope of this research. The scope of this research is limited with the analysis of the outcome of the machine learning and xAI algorithm.

C.	BACKGROUND INFORMATION
The first step of the legal analysis of an algorithm is the normativity analysis, as the use of algorithms should have substantial effect on individuals to fall within the scope of the GDPR and right to explanation.

I.	Normative Feature

a.	Normativity

There are many definitions of normativity or norm, however, one could easily argue that norm should include some kind of rule. We will focus on rule feature of normativity , which can be defined as a rule or set of rules that differentiate / classify cases / individuals according to a criteria. 
In discriminative AI, algorithms define a decision boundary, in other words, impose a rule. Thus, data (or users in real life) is classified by the rule defined by the algorithm, and then individuals are subject to positive or negative decisions, according to such rule. This shows the normative feature of the algorithm(s). Generative AI algorithms do not impose a direct rule, however, generate new data, with an algorithm capturing the pattern of the existing data. 
Supervised machine learning algorithms (discriminative AI) are normative by their nature. After completion of training process, the algorithm imposes a rule, to classify new data (individual) according to its target (variable). This can be technically shown with a decision boundary.  As shown in the implementation part, in some use cases, an algorithm can still be normative, although a decision boundary is not defined explicitly. It is related to its effect on individuals, with a continuous logic. 
Generative AI is not entirely independent of discriminative features. In many generative models, discriminative algorithms play a crucial role in learning the structure of real-world data (i.e. GANs). This discriminative process provides feedback that guides the generator to approximate the true data distribution more closely. Therefore, while the discriminative algorithm does not directly define the probability distribution itself, it establishes the evaluative boundaries that help shape how the generative model learns to reproduce realistic data patterns. 

b.	Normative and Distributive Effect

The rule imposed by the machine learning algorithm may directly change individuals’ situation like in case of a decision to recruit an individual to a job position (normative effect) or it may affect their economic situation and their position vis-à-vis others like in case of a decision affecting the performance note, thus, wage increase of the employee (distributive effect).    

•	Normative Effect 

There are cases where public and private authorities directly use machine learning for certain decisions (taxation, grant of entry to territory, risk assessment). Border control systems, in particular, European Travel Information and Automation System (ETIAS) are good examples of the use of machine learning algorithm by public authorities having a substantial normative effect . Private parties also use similar systems for a decision to grant a right or not (employee recruitment, credit assessment ) or allow a type of behavior by their users or not (content moderation ). All these automated decisions have direct effects on individuals’ situation. 

•	Distributive Effect

In some cases, the effects of machine learning algorithms on individuals are not as direct as those explained above. Decision made by machine learning algorithms may have economic effects on individuals. Ranking algorithms , content recommendation systems , performance note algorithms are examples.  

•	Normative Feedback Loop

The decision taken by the machine learning algorithm may cause feedback to its own mechanisms, in certain cases, and algorithm itself may have an effect of the outcome predicted by itself. Every block in the Machine Learning decision making process (sampling, individual, feature attraction) except prediction can be affected by the feedback loop . The risk of such (normative) feedback loop worth analysis, as well.

II.	Interpretability / Explainability Problem

More complex models tend to be more precise and accurate, but less interpretable. Interpretable models tend to be less accurate accordingly (interpretation-precision trade-off). Machine learning algorithms may be classified as follows, according to their level of interpretability: 

a.	Interpretable (simple) models:
  a.	Linear regression,
  b.	Logistic regression,
  c.	Simple decision trees

b.	Black box models:
  a.	Deep Neural Networks
  b.	Support Vector Machines
  c.	Ensemble methods: Boosting and random forest

c.	Reinforcement learning (RL) / Deep Reinforcement Learning (DRL)
d.	Generative Artificial Intelligence / LLMs

The interpretability problem is more complicated for unsupervised learning, in particular, RL, being a trial-and-error learning algorithm, where an autonomous agent takes actions to find optimal solution through a learning process based on reward.  Generative AI algorithms have a totally different nature, in terms of their decision taking mechanisms. Language models are their primary mechanisms, but they have many sub-operations including RL, Deep Neural Networks etc. Their interpretation and legal requirements for their explanation should be applied in line with their such unique and complex nature. 

III.	Legal Framework

Data privacy law has close connections with machine learning. General Data Protection Regulation (GDPR) is the main regulation under European Union Law for data protection and has various provisions, which have relevance for the explainability and interpretability of machine learning algorithms. 
Individuals’ rights vis-à-vis algorithmic decision making are also regulated under fundamental treaties concerning human rights: (i) Charter of Fundamental Rights of the European Union (CFREU), and (ii) European Convention on Human Rights (ECHR).  The issue is also regulated in different dimensions under European pieces of legislation for those concerning areas other than data protection itself: (i) Digital Markets Act (DMA), (ii) Digital Services Act (DSA), (iii) P2B Regulation , and (iv) AI Act .  Right to data protection is also a fundamental right set forth under Art 8 of the CFREU. 
We will focus on the right of explanation and obtain meaningful information regarding algorithms. These rights can be derived from fundamental right perspective, . However, GDPR is an important piece of legislation, which constitutes a concrete implementation of the fundamental rights in data protection legislation, for transparency. 

a.	Transparency

As per Article 5 of the GDPR and Recital 39 of the GDPR, data controller is required to provide data subject information relating to its right in a concise, transparent and intelligible manner. Such information should be easily accessible and provided in clear and plain language . Thus, a trade-off between conciseness and simplicity exists in GDPR law,  . 
Abovementioned requirements (conciseness, transparency, intelligibility, easy access, clear and plain language) are of relevance for rights related to automated decision making. 
In addition to GDPR provisions, European Court of Human Rights (ECtHR) also accepts transparency requirement for automated decision making.  The AI Act (Article 13) also provides general provisions with respect to the transparency requirements for high-risk systems. 

b.	Right of explanation

Right of explanation is expressly used in Recital 71 of GDPR. However, such right can be derived from articles 13,14, 15 and 22. As per articles 13, 14 and 15 of GDPR, data subjects should be informed of automated decision-making processes  as meaningful information about the logic involved. As reference is made to article 22, the automated decision should be based solely on the machine learning algorithm and should have significant effects on data subject for the abovementioned provisions to be applicable. 
The right of explanation can be derived from transparency requirements and other principles related to fundamental human rights, from a general perspective.  

c.	Right to contest and request human intervention

As per article 22(2), data subjects have the right not to be subject to automated decision making, having legal or significant effects on them. As per Guidelines on Automated Decision Making on Automated Decision Making and Profiling, termination of a contract, refusal of admission to citizenship or grant of social right, decisions affecting credit eligibility, access to health services or education, employment opportunity are examples of such type of decisions.
However, this provision is not applicable if (a) the automated decision making is necessary for a contract between data controller and data subject, (b) it is authorized by EU law or member state, (c) an express consent is given by data subject.
Safeguards to be provided by the data controller, as required by Regulation, for abovementioned cases (a) and (c) would include the right to be provided an explanation, namely, meaningful information on the logic involved and the basis of denial . This is reasonable as being informed is a practical condition for contesting a decision.
Right to request human intervention is also granted under AI Act for high-risk systems (Article 14). 

d.	Meaningful information

The concept meaningful information has its roots in general principles concerning fundamental rights, and codified in article 15 of the GDPR.
The definition of “meaningful information” is of relevance to determine what information to be provided to data subject with respect to the automated decision-making process, namely, machine learning algorithms.
There are several opinions in the literature with respect to its scope:

a.	general functionality of the system (i.e., general information on how the algorithm works ),
b.	counterfactual explanations ,
c.	information enabling data subject to contest to the decision  and exercise her rights under GDPR and Law ,
d.	explanation regarding how inputs relate to prediction ,
e.	test comprised of detailed questions about architecture and implementation of the algorithm ,
f.	subject centric explanations .

From legal perspective, explanations for automated decision making should be concrete and local (meaningful for data subject) and in a manner to enable data subject to contest to the respective decision. 

Meaningful information is required from fundamental right perspective, in accordance with transparency requirement. This is a general requirement and is not defined under the legislation. An explicit reference is made to parameters and their weighting in certain legislations (P2B Regulation, Consumer Right Directive). AI Act provide more generic provisions with respect to the type of explanation to be provided . 

IV.	Types of Explanation/Interpretability

From a technical view, a basic distinction can be made as intrinsic and post-hoc interpretability. Intrinsic interpretability is the information derived from the model itself, as it is interpretable (e.g., linear regression). Post hoc interpretability are technics to interpret the model, after the deployment of the model, without considering the inner structure of the same.  

We will not dive into the detailed explanations about types of explanations. We will focus on counterfactual examples, as accepted in C-203/22 (CK) case . Counterfactual examples allow to understand “the smallest change” to be made to have a possible outcome from the respective algorithm, without diving deep into the algorithms inner mechanism , thus, gives a (limited) concrete information to the individual for its position vis-à-vis algorithm. 

V.	CJEU Case 

Although debated by scholars, both from a legal and technical perspective, case law regarding this issue is very limited. The first is Netherlands case law, which ruled that “criteria relied on in reaching the decision” should be provided to the data subject. 
The important case regarding the right to explanation is CJEU’s recent decision on a profiling algorithm for customers of a telecommunication company (C-203/22 (CK) case ). In this case, CJEU focused on the right to contest of the individual for explanations to be provided and difference in data between the positive result and actual negative result, thus, counterfactual explanations.  

The approach of the court is important from several perspectives: 
(i)	The court defines the scope of the information to be provided and provide guidance on the type of explanation to be provided. 
(ii)	The interpretation is based on balance between two fundamental rights: protection of trade secrets and data privacy. 

Given that the court applied the principle of proportionality and clarified the scope and limits of the right to explanation, it is beneficial to implement these judicial principles into concrete data and case. 

VI.	Legal Requirements according to the Caselaw

In line with the abovementioned case law of the CJEU, we focused on the counterfactual examples, as type of explanation to be provided for the algorithm. 

The outcome of such case is summarized below, as to define legal requirements with respect to the explanations provided for machine learning algorithms:
-	The information is provided in a concise, transparent, intelligible and easily accessible form. 
-	The information is sufficiently transparent and intelligible to inform the data subject of the extent to which a variation in the personal data taken into account would have led to a different result (counterfactual example). 
  o	NOT complex mathematical formula or detailed description of each step (not concise, transparent, intelligible or easily accessible form)

As the information should be easily accessible to data subject, we put special emphasis on LLM generated explanations, as they are easily accessible and generated with a single prompt. 

D.	IMPLEMENTATION 

We wish to apply legal requirements of the CJEU case law on the following concrete examples with a supervised learning algorithm:
a)	Hiring Dataset (synthetic data),
b)	IBM HR Analytics Attrition Dataset.

Hiring dataset has been chosen as an implementation of a use case, having direct normative effect on the individual(s) (normative effect). IBM HR Analytic Attrition Dataset’s implementation has an indirect effect on the individuals’ economic situation (distributive effect). This use case may also constitute an example of so-called “normative feedback loop”. 

Within the scope of this research, a black-box supervised learning algorithm (Random Forest) will be trained and tested on the abovementioned datasets, counterfactual examples will be generated with the help of an existing xAI framework (m-dice library) and results will be converted to natural language explanation with the help of the LLM (OpenAI / gpt-4.1-mini). 

I.	Employee Hiring Data

The use case is use of a black-box algorithm to decide for hiring an employee, according to personal variables such as age, experience, education level, coding score, interview score. No real human intervention is planned for the candidates with negative outcome as per the algorithm. 
As the algorithm’s outcome directly affect the decision to hire or not, the use case has direct normative effect on individuals. 

a.	Dataset
 
A synthetic dataset has been generated, in code, randomly, as the subject of this work is to illustrate counterfactual examples and analyze their content. The following features are used in the dataset. 

b.	Model / xAI Library 

Random forest model is used, as the black-box algorithm. Sklearn library is used as to be compatible with Dice, which is for generation of counterfactual examples. 

As synthetic data has been generated and we trained the model as to constitute a base for counterfactual examples, no data-preprocessing or fine tuning has been made. 

The model has been trained on train data, upon splitting data into test and train sets. The test accuracy (0.8175) is acceptable, for illustration purposes.  

c.	Counterfactual Example Generation

An instance has been chosen from test data and used for counterfactual example generation.  The following instance has been chosen: 

The counterfactual examples have been generated with Dice library, with the following approaches. 

-	With all features

Generated counterfactual examples contain variances of the age variable. Accordingly, these counterfactual examples may not be beneficial for the individual, since it is not possible to be younger in real life. Thus, we generated counterfactual examples on the condition that age variable is constant. 

-	Age variable excluded

As shown in Figure 4, only variables that can be changed by the candidate are used to create counterfactual explanations. In the counterfactual examples, Coding Score and Interview Score is higher, which is a reasonable explanation and guidance for the candidate.

d.	LLM Explanation Generation

OpenAI’s “gpt-4.1-mini” model is used for natural language explanation generation. API call has been made to OpenAI API with a prompt to generate explanation for counterfactual explanation generated above with Dice.

i.	Explanation for Each Counterfactual Example

First, LLM is asked to generate natural language explanations for each counterfactual explanation. The result is as follows: 

“1) Explanation for CF #1  
- Changed features: CodingScore increased from 72 to 79, InterviewScore increased from 59 to 61.  
- Explanation: Improving both your coding test score and interview performance shows stronger skills and better preparation, which makes you more attractive to the hiring model. These improvements give the impression that you are more capable and ready for the job.  
- Actionable guidance: To increase your hiring probability, you would need to improve your coding test score from 72 to 79 and slightly enhance your interview performance from 59 to 61.
2) Explanation for CF #2  
- Changed features: CodingScore increased from 72 to 74, InterviewScore increased from 59 to 68.  
- Explanation: Compared to the original, your coding skills improved a little, but your interview skills improved significantly. A much better interview score suggests you communicate well and fit the role, which strongly boosts your chances.  
- Actionable guidance: To increase your hiring probability, you would need to improve your coding test score slightly from 72 to 74 and focus more on improving your interview performance substantially, from 59 to 68.
3) Explanation for CF #3  
- Changed features: CodingScore increased from 72 to 83, InterviewScore increased from 59 to 61.  
- Explanation: A significant increase in your coding score shows strong technical ability, which is often a crucial factor for hiring decisions. Even a small improvement in the interview also helps. Together, these changes greatly improve your likelihood of being hired.  
- Actionable guidance: To increase your hiring probability, you would need to improve your coding test score considerably from 72 to 83 and slightly improve your interview performance from 59 to 61.”

As it can be seen, the explanation is quite long, and not very concise. For this reason, we asked LLM to generate a single explanation, for what can be done to be classified as hired according to the algorithm and in line with counterfactual examples. 

ii.	A single explanation for all counterfactuals

The following explanation has been provided by the LLM with a prompt to generate a single explanation: 

“The original candidate’s hiring probability is notably lower than the counterfactual versions, mainly because they have lower scores on key skills and are slightly older than some of the more favored candidates. The model favors candidates with higher coding and interview scores, and a bit younger age seems to correlate with a higher chance of hiring in these examples. Experience and education level remain the same, so improvements there are less relevant in this case.

To improve your chances, consider focusing on the following:
- **Increase your coding test score** by practicing problem-solving and programming challenges to demonstrate stronger technical skills.
- **Improve your interview performance** by preparing for common questions and practicing clear, confident communication.
- **If possible, leverage your youth as an advantage** by emphasizing your energy, adaptability, and willingness to learn quickly.
- Since years of experience and education are unchanged, focus mainly on showcasing and enhancing your practical skills and interview readiness.”

The explanation includes explanations both for the factors affecting the algorithm’s decision and actions that can be taken to have a positive outcome from the algorithm, based on the counterfactual examples.

Additionally, although the age variable is not modified in the counterfactual examples, a minor explanation has been made by the LLM with respect to the age. This information is in fact true, for the model, but misleading for counterfactual examples.  

This illustrates how LLM-generated explanations may inadvertently reintroduce legally sensitive inferences even where such variables are formally excluded from counterfactual generation.

II.	IBM HR Attrition Dataset

A black-box algorithm is trained on employee data and the outcome is used to determine the wage raise of current employees.

The dataset has been imported from Kaggle. The dataset is not synthetic. The data shows whether the respective employees have quitted their job, according to several variables such as education level, environment satisfaction, job involvement, job satisfaction, relationship satisfaction  as well as more sensitive data such as marital status, age, gender etc. 

The following use cases are assumed within the scope of our research:
(i)	If the employee’s attrition probability is above a certain threshold (i.e., 0.50), less wage increase is applied (as they are more inclined to quit, so less investment is done.): 
(ii)	No threshold is set, but the bonus/salary increase is penalized with the probability.
 
Both use cases have a normative effect on individuals, and even no explicit norm has been imposed in the scenario (ii), it is still normative, as it affects individual’s position, with the direct application of the probability metric. 

In both use cases, use of algorithm on current employees can even cause normative feedback loop: the norm created by the algorithm—often operationalized through an explicit probability score—can influence individuals’ behavior, which will then constitute a data for the algorithm for the next time. For instance, an employee’s satisfaction level can decrease due to less bonus given, as a result of the algorithm. Such decreased job satisfaction level can be a data for the algorithm to give a less bonus, in next year. This feedback loop risk is more relevant, for the use case described in (ii) above, as increase in Attrition risk applies to all employees, without any decision boundary.  

a.	Dataset

Dataset has been imported to the workbook from Kaggle library. The dataset has 35 variables, which are listed in Annex 1. 

Simple data pre-processing steps have been completed as to map target variable, remove null values and unnecessary columns.

EmployeeNumber is irrelevant, and EmployeeCount, StandardHours and Over18 columns have only one unique value. Thus, we dropped these variables from the dataset. 

b.	Model / xAI Library 

The same model (Random Forest) is used, as the black-box algorithm. Sklearn library is used as to be compatible with Dice, which is used as xAI external library. 

The model is trained as to constitute a base for counterfactual examples, basic data preprocessing and fine tuning (threshold/metrics check) steps have been followed up. The model has been trained on train data, upon splitting data into test and train sets. The test accuracy is acceptable, however, metrics show that the model does have many false negatives.

Accordingly, threshold has been revised to 0.25, as to have a better recall, and false negative ratio. 

Our focus is not model accuracy, thus, counterfactual examples are generated with the original probability threshold (0.5). 

c.	Counterfactual Example Generation

An instance has been chosen from test data and used for counterfactual example generation.  The following instance has been generated: 

The counterfactual examples have been generated with Dice library, with the following approaches. 

-	With all features

-	Discriminative/immutable variables excluded
  
We excluded the following variables: Age, Gender, MaritalStatus, Education, Department, EducationField, JobRole, DistanceFromHome, TotalWorkingYears, NumCompaniesWorked, YearsAtCompany, YearsInCurrentRole.

d.	LLM Explanation Generation

OpenAI’s “gpt-4.1-mini” model is used for natural language explanation generation. API call has been made to OpenAI API with a prompt to generate explanation for counterfactual explanation generated above with Dice.

i.	Explanation for Each Counterfactual Example

First, LLM is asked to generate natural language explanations for each counterfactual explanation. The result is as follows: 

“The machine learning model predicts a high attrition risk (Attrition=1) for the original employee profile based on several key factors. Notably, the employee has a relatively low **JobInvolvement** score of 1, which indicates minimal engagement with their work. Additionally, the **EnvironmentSatisfaction** score is also low at 2, suggesting dissatisfaction with the work environment. Furthermore, the employee has been in their current role for 7 years without a promotion, as indicated by the **YearsSinceLastPromotion** score of 1, which may contribute to feelings of stagnation and a desire to seek opportunities elsewhere. The combination of these factors likely signals to the model that the employee is at a higher risk of leaving the organization.
### Counterfactual Explanations
 **Counterfactual 1: OverTime=0, PercentSalaryHike=20**
   - **Change**: The employee's **OverTime** status changes from 1 (indicating they work overtime) to 0, and the **PercentSalaryHike** increases from 13 to 20.
   - **Impact**: Reducing overtime may improve work-life balance, potentially increasing job satisfaction and reducing attrition risk. A higher salary increase could enhance the employee's financial satisfaction and perceived value within the company, further decreasing the likelihood of leaving.
**Counterfactual 2: JobLevel=2**
   - **Change**: The **JobLevel** increases from 1 to 2.
   - **Impact**: A higher job level typically correlates with greater responsibility, recognition, and potential for career advancement. This change may enhance the employee's engagement and satisfaction with their role, thereby reducing the risk of attrition.
**Counterfactual 3: EnvironmentSatisfaction=4**
   - **Change**: The **EnvironmentSatisfaction** score increases from 2 to 4.
   - **Impact**: An improved environment satisfaction score suggests a more positive work atmosphere, which can significantly influence an employee's decision to stay with the organization. Higher satisfaction in the work environment may lead to increased loyalty and reduced attrition risk.
**Counterfactual 4: JobSatisfaction=2, OverTime=0**
   - **Change**: The **JobSatisfaction** decreases from 4 to 2, while **OverTime** changes from 1 to 0.
   - **Impact**: Although the decrease in job satisfaction appears counterintuitive, the reduction in overtime may still improve overall work-life balance, which can mitigate the negative impact of lower job satisfaction. This balance may lead to a more favorable view of the job, thus lowering attrition risk.
In summary, the model's prediction of high attrition risk for the original employee is influenced by low job involvement, low environment satisfaction, and a lack of recent promotions. The counterfactual examples illustrate how changes in job level, salary increases, and work environment satisfaction can effectively reduce the predicted risk of attrition by enhancing engagement, satisfaction, and overall employee well-being.”

As it can be seen above, the explanation is not concise and clear. The text is long enough and may include LLM’s own interpretation, even misleading ones. 

ii.	A single explanation for all counterfactuals

The LLM is prompted to provide a single explanation for all counterfactual examples. The result is as follows: 

“The original candidate is currently at a high risk of attrition due to several factors that are less favorable compared to the counterfactual examples. Notably, the original candidate has a lower "PercentSalaryHike" and a lower "EnvironmentSatisfaction" score, which are critical indicators of employee satisfaction and retention. The counterfactuals show that candidates with higher salary increases and better satisfaction levels are less likely to leave the company. 
Key features that appear to be important across the counterfactuals include:
- **PercentSalaryHike**: Counterfactuals show higher salary increases (20% vs. 13%).
- **EnvironmentSatisfaction**: Some counterfactuals have a higher score (4 vs. 2).
- **OverTime**: Some counterfactuals do not work overtime, which may contribute to better work-life balance.
To improve their chances of being hired and reduce attrition risk, the original candidate should focus on the following changes:
- **Seek a Higher Salary Increase**: Aim for a salary increase of at least 20% during the next review to align with more successful candidates.
- **Improve Environment Satisfaction**: Engage in activities or initiatives that enhance the workplace environment, such as team-building exercises or providing feedback to management.
- **Consider Reducing Overtime**: If possible, try to limit overtime work to improve work-life balance, which may enhance overall job satisfaction.
- **Enhance Job Satisfaction**: Explore opportunities for professional development or new projects that could lead to greater job satisfaction, especially if current satisfaction levels are low.”
By addressing these areas, the original candidate can better align with the profiles of employees who are less likely to leave the company.”

The output of the LLM is satisfactory in terms of showing which conditions to be improved by the company administration to increase the satisfaction level of the employee. However, it does not provide any meaningful information to the data subject, regarding steps to be taken to improve its own situation, according to the algorithm.  

E.	CONCLUSION

As a result of the analysis of the employee hiring dataset and the IBM HR Attrition dataset, the overall finding is that counterfactual explanations are not equally informative for data subjects across all use cases.

In the employee hiring scenario, counterfactual examples generated by the hiring algorithm provide meaningful and actionable information. The single natural language explanation produced by the LLM is clear and concise. When considered together with the table presented in Figure 4, the explanation offers sufficient insight into which skills the individual would need to improve in order to be classified as “hired” by the algorithm. As noted above, recent case law does not require the disclosure of detailed information regarding the internal functioning of the algorithm. Accordingly, there is no legal necessity to provide additional information on model architecture, feature importance, or similar technical details. Additionally, LLM generated explanation may be misleading, thus, mechanisms to check the accuracy of the same should be implemented. Any legal reliance on LLM-generated explanations should therefore be accompanied by procedural safeguards ensuring fidelity, auditability, and consistency across explanations.

By contrast, counterfactual examples generated for the attrition risk algorithm do not offer relevant practical guidance to the data subject. The variables modified in the counterfactual scenarios largely fall within the employer’s discretion, leaving the data subject with limited capacity to alter the decisive factors influencing the algorithmic outcome. Nevertheless, such counterfactual explanations may still serve a legal function by enabling the data subject to contest the decision, even if they do not provide actionable guidance for changing the outcome. 

Moreover, as counterfactual explanations constitute a form of local explanation, different counterfactuals may be generated across different iterations. This variability may be misleading for data subjects, particularly in models with a high number of variables. In addition, the selective exclusion of certain variables may further distort the explanatory value of counterfactuals. Where sensitive or immutable variables are excluded from the explanation, variations in these variables will not be visible to the data subject, despite their continued use by the algorithm in the decision-making process. Given that, under the C-203/22 (CK) decision, data controllers are not required to disclose further information about the algorithm, this limitation may substantially restrict the data subject’s ability to exercise effective oversight over automated decision-making systems.

Finally, this research is limited to the illustration of counterfactual explanations using synthetic and publicly available datasets. The LLM is employed solely to generate natural language explanations for counterfactuals produced by the DICE framework. Neither the predictive models nor the counterfactual generation mechanisms were fine-tuned or systematically evaluated using performance metrics. Future research could build on this work by employing real-world datasets and incorporating data preprocessing, model evaluation, and fine-tuning stages.

F.	DISCUSSION

LLM is used in this research solely to generate a natural language explanation, for a supervised machine learning algorithm. LLMs can instantly provide explanations for their processes and their explanations can be revised with an instant prompt. Thus, their explanations are concise, clear and understandable, and instantly accessible, by nature. 
On the other hand, LLMs are complex and comprised of many functions and operations and unique in terms of their nature and features. Thus, legal framework should be revised as to comply with unique features of LLMs and Generative AI algorithms. Technical mechanisms to ensure fidelity for answers and explanations provided by LLMs should be introduced. In this sense, mechanisms/layers, immune from uncertainty and vagueness related to large language models, should be implemented for the explanation of the LLMs.

CJEU's case law requiring provision of counterfactual examples as an explanation is not in line with respect to the unique structure of the Generative AI/LLMs. As they have completely different process (generative process), and they are not discriminative by nature, counterfactual examples will not constitute a sufficient explanation, from legal and technical perspective. Additionally, creation of counterfactual examples is also a generative process, their fidelity and accuracy will be questionable.

G.	REFERENCES

Agata Ciabattoni and others ‘Normative Reasoning for AI (Dagstuhl Seminar 23151)’ (2023) In Dagstuhl Reports 13(4) <https://doi.org/10.4230/DagRep.13.4.1> accessed 26 February 2025.
Amanda Musco Eklund ‘Frontex and ‘Algorithmic Discretion’ (Part I): The ETIAS Screening Rules and the Principle of Legality’, (2022) VerfBlog  <https://verfassungsblog.de/frontex-and-algorithmic-discretion-part-i> accessed 1 March 2025.

Amanda Musco Eklund ‘Rule of Law Challenges of ‘Algorithmic Discretion’ & Automation in EU Border Control: A Case Study of ETIAS Through the Lens of Legality’ (2023) 25(3) European Journal of Migration and Law <https://doi.org/10.1163/15718166-12340152> accessed 1 March 2025.

Andrew D Selbst and others, ‘Meaningful Information and the Right to Explanation’ (2017) 7(1) International Data Privacy Law <https://doi.org/10.1093/idpl/ipx022> accessed 30 January 2025.

Ajaya Adhikari and others, ‘Leafage: Example-Based and Feature Importance-Based Explanations for Black-Box ML Models’ (2019) FUZZ-IEEE <https://doi.org/10.1109/fuzz-ieee.2019.8858846> accessed 30 January 2025.

Bryce Goodman and others, ‘European Union Regulations on Algorithmic Decision-Making and a “Right to Explanation”’ (2017) 38(3) AI Magazine <https://doi.org/10.1609/aimag.v38i3.2741> accessed 30 January 2025.

Case C 203/22 CK v Magistrat der Stadt Wien and Dun & Bradstreet Austria GmbH [2025] ECLI:EU:C:2025 <https://curia.europa.eu/juris/document/document.jsf?docid=295841&doclang=EN> accessed 15 June 2025.

Chiara Patricia Drolsbach and others  ‘Content Moderation on Social Media in the EU: Insights From the DSA Transparency Database’ (2024) In Companion Proceedings of the ACM Web Conference 2024 (WWW '24) Association for Computing Machinery <https://doi.org/10.1145/3589335.3651482> accessed 1 March 2025.

Christoph Molnar ‘Interpretable Machine Learning: A Guide for Making Black Box Models Explainable’ <https://christophm.github.io/interpretable-ml-book> accessed 1 June 2025.
Chiyuan Zhang and others ‘A Study on Overfitting in Deep Reinforcement Learning’ (2018) <https://arxiv.org/abs/1804.06893> accessed 1 March 2025.

Derya Ozkul ‘Automating Immigration and Asylum: The Uses of New Technologies in Migration and Asylum Governance in Europe’  (2023) Oxford: Refugee Studies Centre, University of Oxford <https://www.rsc.ox.ac.uk/publications/automating-immigration-and-asylum-the-uses-of-new-technologies-in-migration-and-asylum-governance-in-europe> accessed 1 March 2025.

Elena Falletti ‘Credit scoring and transparency between the AI Act and the Court of Justice of the European Union’ (2024) < https://ceur-ws.org/Vol-3744/paper7.pdf > accessed on 1 March 2025.

Erika Puiutta and others, ‘Explainable reinforcement learning: A survey’ (2020) arXiv preprint <http://arxiv.org/abs/2005.06247> accessed 31 January 2025.

George A. Vouros, ‘Explainable Deep Reinforcement Learning: State of the Art and Challenges’ (2023) 1(1) <https://doi.org/10.1145/3527448> accessed 31 January 2025.

Gianclaudio Malgieri and others, ‘Why a Right to Legibility of Automated Decision-Making Exists in the General Data Protection Regulation’ (2017) 7 (4) International Data Privacy Law <https://doi.org/10.1093/idpl/ipx019> accessed 30 January 2025.

Hamed Taherdoost ‘Enhancing Social Media Platforms with Machine Learning Algorithms and Neural Networks’ (2023) 16(6) Algorithms <https://doi.org/10.3390/a16060271> accessed 26 February 2025.

Heike Felzmann and others ‘Transparency you can trust: Transparency requirements for artificial intelligence between legal norms and contextual concerns’ (2019) 6(1) Big Data & Society <https://doi.org/10.1177/2053951719860542> accessed 26 February 2025.

Lilian Edwards and others, ‘Slave to the Algorithm? Why a Right to Explanation Is Probably Not the Remedy You Are Looking For’ (2017) 16(18) Duke Law & Technology Review <https://doi.org/10.2139/ssrn.2972855> accessed 30 January 2025.

Lundberg and others, ‘A Unified Approach to Interpreting Model Predictions’ (2017) Neural Information Processing Systems <https://arxiv.org/abs/1705.07874> accessed 31 January 2025.
Maja Brkan and others, ‘Legal and Technical Feasibility of the GDPR’s Quest for Explanation of Algorithmic Decisions: Of Black Boxes, White Boxes and Fata Morganas’ (2020) 11(1) European Journal of Risk Regulation <https://doi.org/10.1017/err.2020.10> accessed 30 January 2025.

Marco Tulio Ribeiro and others, ‘Why Should I Trust You? Explaining the Predictions of Any Classifier’ (2016) Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining <https://doi.org/10.1145/2939672.2939778> accessed 31 January 2025.

Michaela Benk and others, ‘Explaining Interpretable Machine Learning: Theory, Methods and Applications’ (2020) SSRN Electronic Journal <https://doi.org/10.2139/ssrn.3748268> accessed 31 January 2025.

Randa Natras and others ‘Machine Learning Model Development for Space Weather Forecasting in the Ionosphere’ (2021) <https://www.researchgate.net/publication/359415194_Machine_Learning_Model_Development_for_Space_Weather_Forecasting_in_the_Ionosphere> accessed 26 February 2025.

Nicolò Pagan and others ‘A classification of feedback loops and their relation to biases in automated decision-making systems’ (2023) <https://arxiv.org/abs/2305.06055> accessed 01 December 2025.

Paulina Jo Pesch and others ‘Data Protection and Machine-Learning-Supported Decision-Making at the EU Border: ETIAS Profiling Under Scrutiny’ (2022) In Privacy Technologies  and Policy: 10th Annual Privacy Forum, APF 2022, Warsaw, Poland, June 23–24, 2022, Proceedings. Springer-Verlag, Berlin, Heidelberg <https://doi.org/10.1007/978-3-031-07315-1_4> accessed 26 February 2025.

Pintelas, Emmanuel and others, ‘A Grey-Box Ensemble Model Exploiting Black-Box Accuracy and White-Box Intrinsic Interpretability" (2020) 13(1) Algorithms <https://doi.org/10.3390/a13010017> accessed 31 January 2025.

Roger Brownsword ‘Technological management and the Rule of Law’ (2016) 8(1) Law, Innovation and Technology <https://doi.org/10.1080/17579961.2016.1161891> accessed 26 February 2025.
Sandra Wachter and others, ‘Counterfactual Explanations without Opening the Black Box: Automated Decisions and the GDPR’ (2017) 31(2) Harvard Journal of Law & Technology <https://doi.org/10.2139/ssrn.3063289> accessed 31 January 2025.

Sandra Wachter and others, ‘Why a Right to Explanation of Automated Decision- Making Does Not Exist in the General Data Protection Regulation’ (2016) International Data Privacy Law < https://doi.org/10.2139/ssrn.2903469> accessed 31 January 2025.

Sharma, Sanjay and others, ‘Definitions, Methods, and Applications in Interpretable Machine Learning’ (2019) 116(44) Proceedings of the National Academy of Sciences <https://doi.org/10.1073/pnas.1900654116> accessed 31 January 2025.

Stephanie Milani and others, ‘Explanaible Reinforcement Learning: A Survey and Comparative Review’ (2024) 56(7) ACM Comput. Surv <https://doi.org/10.1145/3616864> accessed 31 January 2025.

Shikhar Sharma ‘A Visual Introduction to Neural Networks’ (2017) TDS Archive <https://medium.com/towards-data-science/a-visual-introduction-to-neural-networks-68586b0b733b> accessed 26 February 2025.

Teresa Quintel ‘Connecting Personal Data of Third Country Nationals: Interoperability of EU Databases in the Light of the CJEU's Case Law on Data Retention’ (2018) SSRN Electronic Journal. <https://10.2139/ssrn.3132506> accessed 1 March 2025.

Wells Lindsay ‘Explainable AI and Reinforcement Learning—A Systematic Review of Current Approaches and Trends’ (2021) 4 Frontiers in Artificial Intelligence <https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2021.550030> accessed 1 March 2025.




 
ANNEX 1 – IBM HR ATTRITION DATASET VARIABLES LIST

Data columns (total 35 columns):
 #   Column                    	Non-Null Count  Dtype 
---  ------                   		 --------------  ----- 
 0   Age                       	1470 non-null   int64 
 1   Attrition                 	1470 non-null   object
 2   BusinessTravel            	1470 non-null   object
 3   DailyRate                 	1470 non-null   int64 
 4   Department                	1470 non-null   object
 5   DistanceFromHome         1470 non-null   int64 
 6   Education                 	1470 non-null   int64 
 7   EducationField            	1470 non-null   object
 8   EmployeeCount            	1470 non-null   int64 
 9   EmployeeNumber            1470 non-null   int64 
 10  EnvironmentSatisfaction 1470 non-null   int64 
 11  Gender                    	1470 non-null   object
 12  HourlyRate                	1470 non-null   int64 
 13  JobInvolvement            	1470 non-null   int64 
 14  JobLevel                  	1470 non-null   int64 
 15  JobRole                   	1470 non-null   object
 16  JobSatisfaction           	1470 non-null   int64 
 17  MaritalStatus             	1470 non-null   object
 18  MonthlyIncome             	1470 non-null   int64 
 19  MonthlyRate               	1470 non-null   int64 
 20  NumCompaniesWorked 1470 non-null   int64 
 21  Over18                    	1470 non-null   object
 22  OverTime                  	1470 non-null   object
 23  PercentSalaryHike         	1470 non-null   int64 
 24  PerformanceRating         1470 non-null   int64 
 25  RelationshipSatisfaction 1470 non-null   int64 
 26  StandardHours             	1470 non-null   int64 
 27  StockOptionLevel          	1470 non-null   int64 
 28  TotalWorkingYears        1470 non-null   int64 
 29  TrainingTimesLastYear 1470 non-null   int64 
 30  WorkLifeBalance           1470 non-null   int64 
 31  YearsAtCompany           1470 non-null   int64 
 32  YearsInCurrentRole       1470 non-null   int64 
 33  YearsSinceLastPromotion1470 non-null   int64 
 34  YearsWithCurrManager  1470 non-null   int64 

<img width="454" height="700" alt="image" src="https://github.com/user-attachments/assets/bacee8ca-919c-4c35-8b74-8a420e43b567" />
