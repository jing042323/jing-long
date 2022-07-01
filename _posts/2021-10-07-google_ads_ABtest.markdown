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

In comparing OPTION A and OPTION B, the objective is to determine which *‘JOIN US!’* button will receive more clicks. Hence we will set the performance evaluation on “click-through-rate”, or “CTR”, where,$CTR = unique clicks/unique impressions$.  

We do not know if OPTION A or OPTION B would lead to the same CTR. Therefore set our A/B test hypothesis as followed:
$$H_0: CTR_{OPTION_A} = CTR_{OPTION_B}$$  
$$H_0: CTR_{OPTION_A} \nq CTR_{OPTION_B}$$ 
<img src="https://render.githubusercontent.com/render/math?math=H_0:CTR_{OPTION_A}=CTR_{OPTION_B}">
<img src="https://render.githubusercontent.com/render/math?math=H_1:CTR_{OPTION_A} \nq CTR_{OPTION_B}">

If the CTR is different, we will then select the design option that contribute to a higher CTR as our design choice.

## <span style="color:DarkSeaGreen"> B.2 Test Setup in Google Tag Manager and Google Analytics </span> 








