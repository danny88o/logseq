- ![Scientific Paper.pdf](../assets/Scientific_Paper_1674772142103_0.pdf)
- ![Media Article.pdf](../assets/Media_Article_1674772151917_0.pdf)
- ![FDS-S2-02-critique-4-sample-2.pdf](../assets/FDS-S2-02-critique-4-sample-2_1675096337313_0.pdf)
- ![supplementary info Nature Job recruitment.pdf](../assets/supplementary_info_Nature_Job_recruitment_1675178531294_0.pdf)
-
- ## Section 1 The following questions relate to the scientific paper
- ### 1a [10 points]
   Describe the **aims** of the study and its stated **findings**. Write between 80-120 words.
	- Research:
		- Aims to see ((63d7edf8-93d9-48c8-ba02-e7a3d2ce093e)) of unfavourable market outcomes
		- Aims to ((63d30109-48e7-4219-8e47-a620215ef81c)) and then apply it to a Swiss public employment service
		-
		- It finds that ((63d3019b-c06e-4af2-81d6-be0633d9007c)) and that ((63d301a9-31fd-4122-a2e0-8fbc938d55a3))
		- It also finds that this discrimination is more prevelant when the jobseekers are tired ((63d806cb-f462-4a4f-959f-b0d9e8ab236c))
	- Sample: ((63d80114-4946-4045-825c-cd1db773b6c3)) ((63d8012f-bdf6-48f0-998a-fab5c948481a))
	- Answer:  {{renderer :wordcount_uzzxscxe}}
		- The study aims to find to what extent of discrimination from recruiters affects the unfavourable market conditions that women, immigrants and individuals from minority ethnic groups experience in the job market. It does this by constructing a methodology to explore the potential hiring discrimination that monitors the recruiting activity on job sites and uses supervised machine learning with jobseeker characteristics that the recruiters observe.
		  It finds that the recruiter contact rate is 4-19% lower for immigrants and minority ethnic groups compared to  the majority group and that this discrimination is exacerbated when recruiters get more tired as the day goes on. It finds that there is discrimination towards the gender whose field is not dominated by, however it averages out so there is seemingly no effect
-
- ### 1b [15 points].
  Describe the methods used to **collect and process** the data in the study. Be specific about what is being **measured and how**. Write between 230-280 words.
	- Research:
		- ((63d7f49e-c32f-47a2-b690-7073446a6ad0))
		- ((63d7fe5b-4d64-412e-a2cd-2fbaceb853da))
		- ((63d93421-3bf2-4062-b3c5-406cb156d11f))
		- ((63d9424f-661e-495a-b493-e3c97d6718c1))
	- Sample: ((63d7fd7d-57da-4dea-a634-087b5ba564dd))
	- Answer: {{renderer :wordcount_orilmhttp}}
		- Data was collected from Job-Room from 6 March 2017 to 31 December 2017 by the State Secretariat for Economic Affairs, who then anonymized and shared the data. It has 2 sections, the click data and the register data which had to be linked together.
		- Certain pre-processing was carried out, with the following data discarded: from bot systems, from searches where another search was made less than 10 seconds later, and profile views where the profile was only glanced at for less than 2 seconds.
		- Ethnicity was estimated through 3 correlated markers: nationality, name and spoken languages. Nationality and language are easy to pair with an ethnicity, however name had to go through the name-classification algorithm "Onolytics" that can classify names based on ethnic origin. A jobseeker is then classified as either a 'typical' or 'atypical' member of their nationality's group main ethnic group, 'typical' members are nationals from that region that have a name and language typical of the region. The 'typical' members of these groups are the ones used to test for ethnic discrimination.
		- A binary outcome measure was established: the click event "Contact button clicked" which holds whether or not a recruiter presses a button to see the jobseeker's contact info is used.
		- The click data logged from the website was then linked with the jobseeker’s characteristics from the unemployment register. Since not all the information about the jobseekers is available on Job-Room,  the researchers could thus distinguish between jobseeker characteristics visible and not visible to recruiters.
- ### 1c [15 points]. 
  Identify the **statistical methods** used in the study and explain how they are applied to the data. Write between 220-250 words.
	- Research:
		- From piazza: Statistical methods can be any method that was used by the authors to analyse the data and determine the reported results. This can be a statistical method (e.g. t-test), a regression, a classification or any computational method that was used in the paper. If a paper mentions that a previously developed method was used for the analysis, you can indicate this method as the statistical method used. Remember: We don't expect you to describe the method in too much detail. A good answer should refer to what method is used, what are the inputs and outputs of the method and why the authors used this method.
		- ((63d800b1-82ea-418c-a8f8-8118f5389c3b))
			- ((63d91f6a-66e9-4ea5-9589-02b437b5827c))
			- ((63d91e71-dc39-4284-b843-ad60b4d9366a)) 3
		- ((63d806cb-f462-4a4f-959f-b0d9e8ab236c))
			- ((63d91eee-2864-49f6-ba4f-da1da1e1e6b1))
		- ((63d92b8f-7763-422c-a9f1-63a26cbd24c0))
			- ((63d92bd9-ff80-48b6-9590-0a6599abf531))
		- ((63d7f453-cfff-4440-8e6c-95b70c4bbf8e))
	- Layout: ((63da2610-dd82-4a81-a058-32e928519f32))
		- Records where the self-reported characteristics such as age, height, weight, BMI and
		  temperature fell within reasonable ranges were used for analysis. Metrics were
		  reported along with a 95% confidence interval (CI), which was obtained by
		  bootstrapping with replacement. To investigate the association between anosmia and
		  COVID-19, an implicit null hypothesis was posed: “There is no association between
		  anosmia and COVID-19.” The method of multivariate logistic regression including age,
		  sex and BMI as predictors was used to obtain the odds ratio of anosmia. This was done
		  for both, UK and US users of the app who underwent the SARS-CoV-2 test, respectively. The associated p-value was strictly less than 0.0001.
	- Answer: {{renderer :wordcount_dpjmlxlkkv}}
		- To test the effect of ethnicity on contact clicks were statistically significant the metrics from each ethnic group were reported along a 95% CI (Confidence Interval) where the p-value was lass than 0.001 for all but the group from southern Europe. The researchers used Ordinary Least Squares (OLS) regression to predict the average contact penalty they would receive. This same method was then applied but controlling for years of experience instead of ethnicity to show how even that, wouldn't make up for the discrimination.
		  
		  A similar approach is also used to analyse gender based discrimination, 95% CI of a 2-sided t-test showed no meaningful statistical difference when looking at all the data for all jobs. However deeper look into the data showed that this wasn't the full picture, that this average insignificance was a result of discrimination on both sides. The researchers then took the top male dominated fields and modelled linear regression to see if a woman faced a penalty and vice versa for men and found that both groups faced discrimination in the respective fields. A final association of hiring advantages vs (log) wage was tested and the 2-sided t-test revealed a p-value of 0.19, showing a weak link between the 2 factors.
		  
		  To study ethnic penalties over the course of the working day, the researchers focused
		  searches conducted by the same recruiter for the same job, but at different times of the day.
		  All observable candidate characteristics were controlled.
		-
		-
- ### 1d [30 points]. Provide a critical discussion of the paper. 
  Evaluate how strongly the data and analysis support the stated conclusions. Identify limitations of the study. Write between 440-550 words.
	- Research:
		- ((63d7feb7-e82a-42f4-b43d-6d50c34135e2)) might not always be true
		- Intersectionality?
		- Only one country- dATA ON
	- Answer: {{renderer :wordcount_abupvyr}}
		- The paper describes a robust, comprehensive, well-designed, and well-executed study to
		  develop a methodology to investigate hiring bias among recruiters. The researchers tracked
		  the search behaviour of recruiters on an online employment website, using supervised
		  machine learning to control for relevant jobseeker characteristics. This methodology presents
		  a significant advance on previous methods to investigate hiring bias based on observational
		  data and correspondence studies.
		  
		  Researchers linked the recruiter contact data with the jobseeker’s characteristics from the
		  unemployment register, thus allowing them to distinguish characteristics that were visible,
		  and not visible, to recruiters. They used sophisticated statistical analysis, employing OLS with the use of the Lasso-based post-double selection method to control jobseeker characteristics. The methodology allowed an in-depth analysis of bias with respect to ethnicity and gender. Other variables investigated included the time taken by recruiters in evaluating jobseeker profiles and within-recruiter variation in hiring discrimination across the workday. These latter variables provided insight into recruiter implicit biases.
		  
		  The researchers also probed some of the drivers of discrimination and investigated the
		  relationship of the extent of bias with respect to defined productivity-related characteristics of the jobseekers unobservable to the recruiters. Furthermore, the study described a series of placebo tests, validations and robustness tests to demonstrate the validity and strength of the research design. Overall, the methodology was found to be widely applicable, non-intrusive and cost-efficient tool to monitor hiring discrimination, identify some of the drivers of discrimination and inform approaches to address it.
		  
		  The study's scope is limited and potentially underestimates how much discrimination actually occurs. First and foremost, the study fails to consider the intersectionality of the discriminated attributes. That is to say the combination of discriminatory factors such as a woman from a minority ethnic group in a male dominated field could face even greater discrimination than each of those 2 factors by themselves. Another limitation is that the results might not be applicable for other countries around the world. The testing was done completely in Switzerland a country that will have its own unique biases, whether conscious or not, so extrapolating any data on an international level is not a good idea.
		  
		  On top of that using the "Contact button clicked" as a Boolean decider of whether someone is contacted or not will yield results that can be analysed up until that point, the discrimination people face does not end there most will still have to do a face to face interview. The nature of then being able to see the person allows for certain assumptions that can be made that were previously quite hard, such as race and age. This can pose problems women at certain ages struggle to find work more because some employers assume they will go on maternity leave, racial discrimination might only come up only when an interview sees a person as well and further ethnic discrimination might occur upon hearing a certain accent. The study fails to take into account these factors of discrimination that occur after the contact process occurs
		-
- ### 1e [10 points]. Identify and explain the ethical issues connected with the study
  Evaluate how well the authors discuss these issues. Write between 150-250 words.
	- Research:
		- ((63d7f5d8-3267-4935-bdc1-b69496654ae8))
	- Layout:
		- The study complies with ethical standards. Competing interests were clearly outlined. Consultation of and approval by the King’s College London Ethics Committee (UK) and Partners Human Research Committee (US) is clearly indicated. Furthermore, the source code for the application was made publicly available. Any form of data collection was preceded by user consent, and the collected data were stored in a protected manner. Collected data were anonymised and made available to other researchers.
	- Answer: {{renderer :wordcount_eeqnwkzjm}}
		- Data collection must have consent from the users of "Job Room" website, they were already informed that their data whilst using the site would be collected for statistical purposes. The data handling was then conducted in accordance with the relevant ethics board guidelines, which the ETH Zurich Ethics Committee then reviewed and approved.
		  
		  The amount of data collected was justified, only relevant features were recorded. None of the users where ever deceived about any happenings, which ais an improvement from many other studies of this nature
		  
		  It is important to use data to benefit society and the study did this by improving human understanding of a widely debated subject. It can definitely be used to for better economic efficiency. The data set was anonymised so there were no harms to privacy or security
		  
		  The source code for both the data collection and data analysis was made publicly available. The dataset can be accessed by signing an agreement with both the Swiss Secretariat for Economic Affairs and ETH Zurich.
- ## Section 2. 
  The following questions relate to the media report of your chosen study:
-
- ### 2a [5 points]. Summarise the report in your own words.
  Write between 70-110 words.
	- Answer: {{renderer :wordcount_kznsgbiis}}
		- The report describes a study by Swiss researchers that investigated recruiter hiring bias by
		  analysing data from the government recruiting website. Researchers found that although men and women were hired at about equal rates, there was evidence of occupational bias. Researchers also found discrimination based on the race and ethnicity of applicants. The further the candidates were from the majority group (culturally, linguistically, etc.), the greater the discrimination. Hiring bias by recruiters was found to increase at certain times of the day, which was attributed to recruiter exhaustion levels. The report describes how the research could be used to improve recruiting sites and reduce discrimination.
-
- ### 2b [15 points]. Evaluate how accurately the report summarized the study.
  You could identify aspects of the study that were not included in the report and discuss how important it would be to include them to give a fair impression of the research. Write between 150-250 words.
	- Answer: {{renderer :wordcount_rjaebgsck}}
		- The media report covered some aspects of the study, in a very simplified fashion. It noted the
		  findings that men and women were hired at about equal rates, but that gender occupational
		  bias existed, as did discrimination on the basis of race and ethnicity.
		  
		  Most of the explanations and discussion of the study findings comprised direct quotes from
		  the lead author, rather than describing the results and analysis of the paper per se.
		  The finding that bias varied across a working day was talked up considerably in the report
		  and even included in the report title (possibly for click-bait potential).
		  An incomplete explanation of the study methodology was given and many important aspects
		  of the study were not included. For example, no reference was made to the supervised
		  machine learning, or the sophisticated and rigorous data analysis used in the study. There was
		  only one statistic quoted "17% bias against those from sub-Saharan Africa".
		  
		  Also missing were the considerations given in the study to: the jobseeker work experience
		  and how it influenced bias; the time that recruiters spent in studying jobseeker profiles. The derivation of an occupation-specific “unobserved employability index” and its relationship to ethnic penalties was also not discussed, nor the value of using employment websites as a practical cost-efficient tool to monitor discrimination.
		  
		  As such, the report did not really do justice to the excellent methodology, rigorous analysis
		  and fascinating findings of the study.
-
## Advice 

<!--[if !supportLists]-->·       
<!--[endif]-->When you first read the studies, you will
probably find that you don’t understand several concepts in the papers. Don’t
worry; this is normal. Part of the skill of understanding a study is to
identify parts you don’t understand, and see what you can understand from the
rest of the paper.

<!--[if !supportLists]-->·       
<!--[endif]-->[“How
to read a paper” by Michael Mitzenmacher](https://www.eecs.harvard.edu/~michaelm/postscripts/ReadPaper.pdf) gives very good
advice on reading a paper *critically.*