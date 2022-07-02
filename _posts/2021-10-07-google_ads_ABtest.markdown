---
layout: post
title: Google Ads Campaign - A/B Test
date: 2021-03-30
image: google_ads_ABtest.jpeg
tags: [Digital Marketing]
---

In this project, we had a very exciting firsthand experience of 'running' a business. We first design and launch our own website by Weebly, and use tag manager to monitor the site via Google Analytics. To find out a more effective plan for our website design, we conduct an A/B test through analysing the real data we collect over a few weeks. 

The full report contains: 

**Section A - Business Context**  
- Introduction  
- Business Interest  

**Section B – Test Design and Implementation**  
- Test Design  
- Test setup in Google Tag Manager and Google Analytics  
- Test implementation  

**Section C – Analysis**  
- Exploratory Data Analytics  
- A/B test on ‘JOIN US!’ Button with CTR Evaluation  

**Section D – Further insights & Improvements**  
- Improvement 1: Separate testing for mobile vs desktop users  
- Improvement 2: A/B testing using Google optimize  

**Section E: Conclusion and Reflection**

***

# <span style="border-bottom:2px solid DarkSeaGreen;color:DarkSeaGreen">Section A - Business Context</span>  

## <span style="color:DarkSeaGreen"> A.1 Introduction </span> 

We are a new start-up travel consultancy company, set up by four travelling enthusiasts who like traveling around the globe exploring new places and experience. We are interested to share our great experience with others, hence offering this service to provide customized tour consulting service to customer in curating the personalized tour itinerary, accommodations, logistic planning based on our experience and network across different continents. With the personalized plan offered, customer could save time in doing the tour planning work, grab their luggage, and enjoy the travelling.

We have developed a website (http://tourscurator4u.weebly.com/) to showcase our service and as one of the means to spread our business. Our website is structured with a home page, and three sub-pages, which reflects our main three offerings: 
- City/Urban tour
- Cultural tour
- Adventurous tour

<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/d1.jpg" height="190" width="600" />  
</p>

In order to build and expand our customer base, we plan to use our website to attract potential customers. We have created a *‘JOIN US!’* button in our website, which enables our website visitors to become our member. We would like to use this *‘JOIN US!’* button to collect more customer information, such as contact information, demographic information, interests, etc, to better segmentize our customer, provide customized service, as well as providing targeted engagement like travelling tips, blogs. In addition, for every click of *‘JOIN US!’* button, it offers opportunity for us to respond and offer follow-up of customized and personalized tour advices, hence turning in potential revenue.  

For click of button in every session by visitor, we will be able to follow-up with the visitor. Say, a visitor views our website, interested to get our service, and clicks the *‘JOIN US!’* button on day 1. We will respond accordingly. If the same visitor comes back a week later and have another idea in mind to explore another tour, he/she can click ‘JOIN US!’ button again, for a new service offering for the new tour. Similarly, we will respond to the new request received.

## <span style="color:DarkSeaGreen"> A.2 Business Interest </span> 

It is important for us to capture the visitors who click the *‘JOIN US!’* button as that represents potential revenue with every click. Click through rate (CTR), which is clicks over impressions, would be a key indicator in our website design for a new start-up as we will rely on the website in offering services in different countries. Having no website before, CTR would be a more important indicator in evaluating the current website design in turning in clicks by visitor, or attractiveness of webpage design to convert a click from visitors; rather than conversion rate despite the true revenue will be measured from conversion rate. Converting a visitor into true revenue will be subjected to offering of service by the company in responding to the visitor’s click. Therefore, it is our immediate interest in our website design to attract visitors to join us.  

Unsure of how effective would be our website design in capturing the visitors attention to the *‘JOIN US!’* button, we intend to perform an A/B test to decide where to put our *‘JOIN US!’* button. We are considering two design options:

- **Option A**. Put *‘JOIN US!’* button on the subpages of our website, which are city/urban tour page, cultural tour page and adventurous tour page. In each subpage, we provide a specific kind of tour with some photos and introductions. We think people may be more willing to click to proceed leaving a contact with us to follow-up when they view the individual sub-page showing offerings by tour type, which is meeting their interest.

<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/d2.jpg" height="190" width="600" />  
</p>

- **Option B**. Put *‘JOIN US!’* button on the homepage of our website. Normally, the homepage is the most viewed page and putting the *‘JOIN US!’* button there is the most direct way. When visitors come into our website, they can easily see the *‘JOIN US!’* button without taking several minutes to go through all the subpages. It is kind of a guarantee that every visitor can see the *‘JOIN US!’* button.

<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/d3.jpg" height="190" width="600" />  
</p>

We will implement this A/B test on the above two design on placement of *‘JOIN US!’* button, and evaluate its CTR.  

We are going to use built-in functions from Google Tag Manager and Google Analytics to tag our website, and subsequently extract the relevant data to evaluate each CTR. In addition, we will use data extracted from Google Analytics to explore analytics on visitors' profile, i.e. device access and page view, so that we can improve our website design.

# <span style="border-bottom:2px solid DarkSeaGreen;color:DarkSeaGreen">Section B - Test Design and Implementation</span>  

## <span style="color:DarkSeaGreen"> B.1 Test Design </span>  


### <span style="color:DarkSeaGreen"> B.1.1 Test Size </span>  

As the business interest is to use the A/B test to determine the best location of placing the *‘JOIN US!’* button for leading visitors to click and then leave their personal information on this newly launched website, we need to get sufficient number of visitors for the A/B test to be done. We use the following assumption in determining the required sample size (or minimum visitors) to run our test.

- As a new business entity, we set our 1st business target as acquiring the first 100 visitors to view our website as one of business milestone. Given the COVID-19 pandemic spread when we set up the business and the website, we expect headwind in promoting our business idea for people to look-up for tours consulting services. Therefore, we assume 100 as our population size, and we set a 10% margin of error, with a 90% confidence interval (lower than the industry norm of 95%). The high margin and lower confidence interval would make our sample size smaller, but faster to acquire the necessary test samples to test our website and offering in the beginning stage (and in the challenging time of COVID-19 pandemic).  
- We use available sample size calculator from [SurveyMonkey](https://www.surveymonkey.com/mp/sample-size-calculator/) to calculate the required size.  
- The result using the SurveyMonkey sample size calculator shows a sample size of 41.We will need to get at least 41 samples for our A/B test.

<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/d4.jpg" height="190" width="600" />  
</p>

### <span style="color:DarkSeaGreen"> B.1.2 Test Hypothesis </span> 

In comparing OPTION A and OPTION B, the objective is to determine which *‘JOIN US!’* button will receive more clicks. Hence we will set the performance evaluation on “click-through-rate”, or “CTR”, where $$CTR = \frac{unique clicks}{unique impressions}$$.  

We do not know if OPTION A or OPTION B would lead to the same CTR. Therefore set our A/B test hypothesis as followed:  

$$H_0:CTR_{OPTION_A}=CTR_{OPTION_B}$$  
$$H_1:CTR_{OPTION_A} \neq CTR_{OPTION_B}$$

If the CTR is different, we will then select the design option that contribute to a higher CTR as our design choice.

## <span style="color:DarkSeaGreen"> B.2 Test Setup in Google Tag Manager and Google Analytics </span> 

We plan to use Google Tag Manager to track button clicks into Google Analytics.  

**(1) View the source code**  
In Chrome, we could right-click the button and select ‘Inspect’. This will open Developer Tools, allowing us to view the source code of the page.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/1.jpg" height="90" width="600" />  
</p>   
We could see that the button locates in a form and that the button has a class of “wsite-button wsite-button-large wsite-button-normal”. We could track button clicks by using the class in Google Tag Manager.

**(2) Enable the variable**  
Google Tag Manager has a range of built-in variables that automatically make the details of interactions available when configuring tags and triggers. For example, we can use variables to check whether someone views a particular page, watches an embedded video, scrolls down a page, or in our case, clicks a particular button on our website.  
Since we have identified the button’s class, we could enable ‘From Class’ from build-in variable.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/2.jpg" height="190" width="600" />  
</p>  

**(3) Create a tag**  
Now, we could create our tag which will send data to Google Analytics when our button is clicked. Select ‘Tags’, click ‘New’ and name our tag ‘button’. After that, select ‘Google Analytics: Universal Analytics’ from Featured tab. Change the Track Type to ‘Event’, and enter the ‘Button’ as Category, ‘Click’ as the Action.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/3.jpg" height="190" width="600" />  
</p>  
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/4.jpg" height="240" width="300" />  
</p>
Before we save our new tag, we still need to add a trigger.  

**(4) Create a trigger**  
Trigger tells Google Tag Manager when a tag should (or shouldn’t) fire. For our button click tag we need to create a trigger so that the tag only fires when our button has been clicked. To do this, we select ‘Triggering’ for the tag to create a new trigger. In our case, we select ‘All Elements’ from Click section in trigger type.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/5.jpg" height="240" width="300" />  
</p>
Now we need to change the trigger so that it only fires on some clicks. We then select ‘Form Classes’, ‘Equals’ and enter the class we identified when we viewed the source code of our page.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/6.jpg" height="190" width="600" />  
</p>
Now, we could save the trigger, then save the tag.  

**(5) Publish the container**  
Click ‘Submit’ from the Workspace page of Tag Manager to publish the container to our website.  
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/7.jpg" height="90" width="600" />  
</p>  

**(6) Check Google Analytics**  
Now, we should be able to see the click data from ‘Behaviour’ in Google Analytics.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/8.jpg" height="190" width="600" />  
</p>  

## <span style="color:DarkSeaGreen"> B.3 Test Implementation </span> 
After we have finalized the test setting in Google Tag Manager and Google Analytics, we published our website on 14th March 2021. We set our 1st test on 16th March ~ 19th March 2021, representing the A-test, and 2nd test on 20th March ~ 23rd March 2021, representing the B-test. We used the gap between 14th March 2021 and 16th March to familiarize ourselves to operate Google Analytics, where preliminary data was collected and analytics performed to understand functionality of Google Analytics. These data were not used in our A/B test.  

We reached out to own connections (friends, colleagues, university cohorts), spreading the website address to acquire the required sample size. We mainly spread the word about our website through social media platform, i.e. Whatsapp, Facebook. We tracked the daily users, and views in Google Analytics.  

We had initially planned for 4 days per test, where we have the design OPTION A for the first 4 days, and changed the website to design OPTION B on the 5th day, which is 20th March 2021. With the target sample size of 41 samples, and estimation of getting approximately 10 visitors per day (or with each group member turning in 10 visitors among his/her network, leading to at least 40 sessions), we had planned for 4 days duration for each test, to meet the sample size of 41.  

Unfortunately, we had managed to get 2 visitors on A-test in the first 2 days. It gained traction on day-3 (18th March 2021) after more promotion among circle of connections. At the initial planned finish date of day-4 (19th March 2021), we could only accumulate 25 users and registered 28 sessions, short of the required sample size target. Therefore, we had to extend our test duration, and managed to acquire 42 visitors and 45 sessions recorded as of 21st March 2021. We then switched the design to OPTION B to run B-test on 22nd March 2021.  

The following Table 1 shows the plan and actual test implementation dates.
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/t1.jpg" height="190" width="600" />  
</p>  

The following Graph 1 shows trending of users and sessions for A-test (16th ~ 21st March 2021) and B-test (22nd ~ 25th March 2021) 
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/g1.jpg" height="220" width="600" />  
</p> 

# <span style="border-bottom:2px solid DarkSeaGreen;color:DarkSeaGreen">Section C - Analysis</span>  

## <span style="color:DarkSeaGreen"> C.1 Exploratory Data Analytics </span>  

### <span style="color:DarkSeaGreen"> C.1.1 Pageviews Analysis </span>  
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/t2.jpg" height="190" width="600" />  
</p> 
We can see that homepage represents more than 50% of the total pageviews and most visitors enter directly from the homepage. At the same time, visitors spend much longer time on homepage than the time on subpages. These findings can support our OPTION B where we think homepage will be the most viewed page.

Moreover, there are some interesting findings on Bounce Rate and Percentage of Exit. The bounce rate and %Exit of homepage is the highest which means approximately half of our visitors leave our website after visiting the homepage only. So it is better for us to improve the guidance on homepage to our subpages to decrease the bounce rate and %Exit on homepage. In this way, we may improve the CTR.

### <span style="color:DarkSeaGreen"> C.1.2 Geo Analysis </span> 
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/t3.jpg" height="230" width="600" />  
</p>
Most of our visitors come from Malaysia, Singapore, Ireland and United Kingdom. This is in line with the way we obtain our sample which is our own connections (friends, colleagues, university cohorts). The average bounce rate is 53.27% and the average pages/Session is 2.9. Visitors from Singapore spend much more time on our website with average session duration of 234.89, which means our products may be most attractive to Singapore visitors.

### <span style="color:DarkSeaGreen"> C.1.2 Device Analysis </span> 
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/t4.jpg" height="110" width="600" />  
</p>
More users visit our website by mobile, while the average session duration is much longer for desktop visitors. One of the reasons is that our website is designed for desktop visitors and looks clear and nice in the desktop version. With such a high proportion of mobile users, a user-friendly website version for mobile users should be developed. Moreover, the difference performance in device category suggests that a deeper analysis in device data should be meaningful.

## <span style="color:DarkSeaGreen"> C.2 A/B test on ‘JOIN US!’ Button with CTR Evaluation </span>
Our A/B test hypothesis is a two-tail test with significance level $$\alpha = 10%$$ as followed:  
$$H_0:CTR_{OPTION_A}=CTR_{OPTION_B}$$  
$$H_1:CTR_{OPTION_A} \neq CTR_{OPTION_B}$$  

We can construct a t statistic which is  
$$t_{\hat{CTR_A}-\hat{CTR_B}}=\frac{\hat{CTR_A}-\hat{CTR_B}}{se(\hat{CTR_A}-\hat{CTR_B})}=\frac{\hat{CTR_A}-\hat{CTR_A}}{\sqrt{\frac{(n_1-1){s_1}^2+(n_2-1){s_2}^2}{n_1+n_2-2}(\frac{1}{n_1}+\frac{1}{n_2})}}$$  
where $$\hat{CTR_A}$$ and $$\hat{CTR_B}$$ are the mean CTR of the two samples; $$s_1$$ and $$s_2$$ are the standard deviation of the two samples;$$n_1$$ and $$n_2$$ are the sample sizes.  

If $$|t| > critical value 0.1$$ or $$P-value < \alpha$$, we reject $$H_0$$.  

Based on the data we collected, we get:
<p align="center">
<img src="{{site.baseurl}}/assets/img/Google_Ads_ABtest/t5.jpg" height="190" width="600" />  
</p>
We can see that:
- $$t stat = 1.0879 < t critical value = 1.6623$$;  
- $$P-value = 0.2796 > 0.1$$.  

Therefore we fail to reject $$H_0$$ at significance level of 10%, which means there is no significant difference between the CTR from OPTION A and OPTION B.  

# <span style="border-bottom:2px solid DarkSeaGreen;color:DarkSeaGreen">Section D - Further insights & Improvements</span>  







