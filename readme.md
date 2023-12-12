Link to the Jupiter notebook:https://github.com/praloysinha/BHcourse/blob/main/Praloy_Analyses_Code1.ipynb

Important: Please run the code once to generate the Plotly plots which may not be visible when you open the notebook.

**Objective: This project is to analyze the different factors which may influence the acceptance of eateries' coupons by the drivers who are in the vicinity.**


**Data Context:** It has the demographic information of the driver, passenger details, timing and frequency of restaurant visits etc.


**Approach:** I looked at the acceptance percentage of different types of driver cohorts by aplying different kind of filters and then seeing which factors lead to higher acceptance rates.


It was done in a Jupiter notebook and with Seaborn and Plotly plots. It is uploaded in this same folder. 


Initially data was explored to find out the null values and there were 6 variables which were detected with null values. The following action was taken.


1. Drop the car variable as it might not have an impact on the analyses and it is also missing in 99.15% of the cases

   
3. Keep the rest of the variables as it has 1-2% missing values and replace with the highest occurring case in each variable

   
5. Created a dataset data1 with the imputed values and cross-checking again for 0 null values this time
   
   
** Overall observations  **


Observation 1 - The proportion of total observations who chose to accept the coupon is 56.84%


#Coupon is a categorical variable which provides info which type of eatery is eating place is providing the discount. Hence the counts of the different types of coupons will provide a consolidated picture of the relative availability.


Observation 2 - #Coffee House coupons are the highest in number (3,996) followed by Restaurant(<20) which has 2,786 coupons


Observation 3 - #There are only 3 temperatures in the dataset viz. 80 degrees, 55 degrees, 30 degrees. The 80 degrees coupons are the highest and constitute more than half of the observations.



**Analyses of the bar coupons**


Observation 4 - #The acceptance rate of bar coupons at 41% is lesser than the overall average of 56% 


Observation 5 - The acceptance rate of bar coupons for people who visit the bar more 3 times a month at 77% is more than double of the the ones visting 3 or fewer times a month which is at 37%


Observation 6 - The acceptance rate of bar coupons of people going to a bar more than once a month and over the age of 25 is almost at 70% and is more than double of the rest of them.


Observation 7 - #The acceptance rate of bar coupons of people going to a bar more than once a month and  had passengers that were not a kid and had occupations other than farming, fishing, or forestry is more than double of the others.


Observation 8 - The acceptance rate of bar coupons of drivers who go to bars more than once a month, had passengers that were not a kid, and were not widowed is 71.32%


                The acceptance rate of bar coupons of drivers who go to bars more than once a month and are under the age of 30 is 72.17%

                
                The acceptance rate of bar coupons of drivers who go to cheap restaurants more than 4 times a month and income is less than 50K is 45.35%

                
Observation 9 - #The overall bar coupon acceptance rate is 41%. 


                #However a few groups within this overall group to which bar coupons were distributed have signifantly high %age of acceptance

                
                #People who visit bars more frequently are more likely to accept the coupons. This is clear from the fact that ~77% of the coupons were accepted for bar visitors of 3 or more times per month.

                
                #On similar lines, people who visit bars more than 1 time a month and do not have a kid travelling with them have a high acceptanec rate. It is 71.32% for a cohort within it for not being a widow or not working for a certain profession.

                
                #People with bar visits more than 1 time a month of greater than 25 and below 30 age is close to 70%. 

                
                #Hence it can be concluded that frequency of bar visits and age is an important factor of acceptance.

                
Observation 10 - The figure shows the acceptance rate is significantly higher for the high frequency visits (more than 1 time per month)


I then deep dived into the data with more than 1 time visit to the bar per month


Observation 11 - It can be concluded that travelling "alone" is most common and the highest acceptance happens at age 26. 


I looked at the acceptance rate by Passenger Type


Observation 12 - It can be concluded that travelling with "friends" increases the acceptance rate quite significantly


I looked at the acceptance rate by Gender and Time of coupon


Observation 13- It can be also worth noting that 6 PM is best time for acceptance of coupons more so for females. 10 PM is also good for males.


**Overall Conclusion for bar coupons** - Just as an example recommendation, it would be great to target "males" with age "26" driving with "friends" at "6 PM" who have "more than 1 visits per month" to the bar as the target group for high acceptance of coupons


**Analyses of the Coffee House coupons**


**Approach**


I took a look at the number of coupons and their acceptance criterion based on different categories of restaurants


Obs 1. I chose Coffee House as the next group to investigate since it has the highest number of coupons of almost 4k.  I created the dataframe for Coffee House.


Obs 2. The acceptance rate of Coffee House coupons at 49.92% is lesser than the overall average of 56%


I took a look at the potential variables and their influence over the acceptance criterion 


Obs 3. From the figure it can be observed that higher frequency visits(more than once a month) have higher acceptance % and if there is a friend or a partner, the acceptance is higher.


I created a dataframe for coffee house visitors more than once a month


Obs 4. From the figure it can be concluded that 10 AM and 6 PM are the top slots to drink coffee and ages 21 and 26 are the top ages to target. 


Obs 5.From this plot, we can infer that sunny weather with 80 degrees temperature has a high acceptance


Obs 6. From the below figures, it can be inferred that Computer & Mathemautical, Unemployed, Education & Training and Student have marginally higher acceptance and also Single and Married Partner are the top ones as per Marital Status


Obs 7.From the below plot, it can be inferred that opposite direction travel positively influences acceptance


Based on the above observations, I created a few groups which can have high acceptance % and can be potential target groups which are a subset of each other 


Group 0: Customers who have received coffee coupons


Group 1 - go to Coffee Houses more than once a month


Group 2 - go to Coffee Houses more than once a month, had passengers that were friends or partner


Group 3 - go to Coffee Houses more than once a month, had passengers that were friends or partner, aged 21 or 26


Group 4- go to Coffee Houses more than once a month, had passengers that were friends or partner, aged 21 or 26 visited at 10 AM or 6 PM


Group 5- go to Coffee Houses more than once a month, had passengers that were friends or partner, aged 21 or 26 visited at 10 AM or 6 PM and weather is sunny


Group 6- go to Coffee Houses more than once a month, had passengers that were friends or partner, aged 21 or 26 visited at 10 AM or 6 PM and weather is sunny and need to travel 


Overall Conclusion: It is clear from the above observations that we can increase our acceptance % of 49.92% in Coffee House coupons by filtering on certain variables like:


Frequency of visits, passenger type, age, time of visit, weather,travel direction


**Have created the groups 1-6 which increasingly improves the acceptance % to 81.94%.**


Have created a funnel which illustrates the target groups which can be used for issuing coupons and their definitions

