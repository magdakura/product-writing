## Prompt

Add-to-cart rate is often used as an indicator of visitors' purchase intent. You, a product manager on the ecomm team, noticed that this week's ATC rate is down significantly y-o-y. The tracking functionality is working as expected, as well as the query used to pull the data. **How would you go about investigating the cause of the drop?**


## Answer

I have a tested approach to investigating performance issues on my products. First, I want to understand the metric itself, and the nature of the decrease. Then, I slice and dice the data to identify user cohorts and points in user journey that might be negatively impacted outside of the metric. Below is the exact checklist  I use to diagnose performance problems:

**1\. What is happening?** 

-   What is the definition of the metric? *Assumption:* ATC rate = unique visitors who click "add to cart" CTA / unique visitors to the Product Description page with "ATC" CTA.

-   Is this a sharp or progressive decline? Is the decline happening just this week? *Assumption:* This is a sharp decline. This is the first week we see the decline. 

-   Data pipeline and tracking okay? Confirmed in the prompt that there's no issue with the underlying data or the analytics tools used to pull the data. 

-   Seasonality? Confirmed that this trend is not due to seasonal drop.

**2\. Who is affected?** 

-   Geography: Is one geographical region driving the drop?  

-   Device: Is the drop driven by a certain platform, operating system, device type or browser?

**3\. Where else is it happening?**

-   Up funnel: What is happening with the metrics higher up the funnel? Are we seeing a proportional drop elsewhere? 

-   Down funnel: What is happening with metrics lower in the conversion funnel, specifically, is the checkout rate experiencing a proportional drop?

Answers to questions above help diagnose the root cause of the problem, which could fall into internal or external factors. Examples include:

**4\. Why is it happening?**

Internal factors as reasons for the change:

-   Are there any recent launches that might have caused bugs or usability issues? (on our team and outside of our team)

-   Are we running an A/B test that may have caused the change? 

-   Are there any changes to the marketing strategy? 

-   Are there any changes to the business strategy? (eg: pricing model, sales strategy)

-   Have we run any initiatives that might have cracked down on bot or other robo-traffic recently that might have altered the metrics? 


External factors as reasons for the change:

-   Is there a new entrant to the market (competition)?

-   Has there been recently a negative PR event that may have impacted our metrics? 

-   Has there been a macroeconomic change that may be driving the drop? (eg. COVID, natural disaster, etc.)
