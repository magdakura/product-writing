Technology is continuously enriching our lives by providing unbounded possibilities for learning, tracking, shopping, communicating, and more. As a Product Manager, I'm lucky to partake in this process by shaping the future of products and bringing them to the world.  

To unlock the next level of growth for your product, you need to purposefully design it to appeal to international audiences. These are the three most important learnings I've gained through my years of building global products. 

First Things First: Fancy Terms
-------------------------------

When building international products, you'll quickly come in contact with four important terms. These four terms represent the dimensions of the learnings I've gathered:

1.  *Globalization (g11n)* is the high-level strategy and planning that paints the picture for how your product will take the market around the world. **Globalization includes internationalization, localization, and translation.** 
2.  *Internationalization (i18n)* refers to developing the underlying technical framework of your product so that it supports many locales. Put simply, your tech needs to support different formats for street addresses, dates, and times (and much more) so that your product can be localized for regions that use these formats. **Internationalization enables localization.**
3.  *Localization (l10n)* is the process of adapting your product to meet the needs of a new market including cultural (tone, humor, traditions), technical (currencies, date formatting), user experience, and legal compliance aspects. **Localization is what makes your product look and feel natural in the new market.** 
4.  *Translation (t9n)* is converting the meaning from one language to another. 

A common confusion is to equate translation to internationalization or localization. Internationalization is a technology piece that enables localization including translation. Translation, in turn, is only one, albeit crucial, part of the localization process. 

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQGQtnNLD0qOXA/article-inline_image-shrink_1500_2232/0/1612906970906?e=1619049600&v=beta&t=08cNVELsruIsgRbHcrDvGQp8vfCZzdIRrlq4DeYVbA0)

Lesson One: Craft a Global Strategy (but not too early)
-------------------------------------------------------

Expanding to multiple markets is a smart product growth strategy. Having a presence in multiple markets allows you to reach a wider audience. However, I would caution against moving to a new market too early, prior to achieving product-market fit (PMF). **Solving locally specific problems can be a sandbox to your global growth.** 

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQESZa6wPcFviw/article-inline_image-shrink_1500_2232/0/1612908121308?e=1619049600&v=beta&t=XnByXLSxGj6-8hek3gATqmsR5QFbfP0rtyPJMjVi-GM)

Once you've achieved PMF, it's time to craft your global strategy. There are over 4.5 billion users online with another billion getting connected by 2025 ([Google](https://blog.google/technology/next-billion-users/new-internet-users-covid-19/#:~:text=Between%202015%20and%202020%2C%20more,Asia%2C%20Latin%20America%20and%20Africa.&text=Today%2C%20though%2C%20new%20internet%20users,the%20impact%20of%20COVID%2D19.)), and most of these new Internet users come from Asia, Latin America, and Africa. **Currently, less than 7% of the world's Internet users live in the US, and this number is continuously decreasing.**

Additionally, only 20% of the world's population understands English. As an example, less than 1% of mainland Chinese are conversational in English. In India, where English is one of the official languages, less than 12% of the population is English-speaking. These two countries constitute 36% of the world's population ([Pew](https://www.pewresearch.org/fact-tank/2018/07/11/world-population-day/)). At the same time, **there's an undeniably strong link between in-language content and a consumer's likelihood of making a purchase:** 

-   72.4% of consumers say they would be more likely to buy a product with information in their own language ([HBR](https://hbr.org/2012/08/speak-to-global-customers-in-t)).
-   56.2% of consumers said that the ability to obtain information in their own language is more important than price ([HBR](https://hbr.org/2012/08/speak-to-global-customers-in-t)).

To summarize, only one in five potential users of your product understands English. The other four will go to a local competitor of your product; that is, **the future = customized product experience.** Taking your product global is no longer just a growth hack, it's a necessity. 

Lesson Two: Get Your Tech Ready for Global (as early as Day 1)
--------------------------------------------------------------

You can start preparing your technology to go global with every line of code you write. **Internationalization should be part of the foundation of your product.** If you try to retrofit your product after the fact, this will be painful, messy, and lengthy. 

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQGsEH0PfIxKVw/article-inline_image-shrink_1000_1488/0/1612907358680?e=1619049600&v=beta&t=6X0mJIJpnLe364c77vM04xYrn5T2_zyxaO6_oGPdlrk)

This is because different markets have unique conventions for form fields, number/date/time formats, fonts, and other visual elements. Here are a few specific examples I've learned the hard way:

-   *Surnames* come before given names in some countries (e.g., China, Korea, Hungary)
-   *Dates and times:* **01/02/09** This is a date. It's the first of February in Colombia and the second of January in the United States. **01:02:09** This is a time. **01.02.09** This is a date in Poland and a time in Norway (i.e., even countries that are geographically close can have entirely different standards)

Understanding and complying with local conventions is obviously critical to your product's success in the market. But just understanding these differences is not enough. Your tech needs to account for those differences by adapting technical solutions that allow you to move fast without introducing technical debt. A common approach is to hardcode local rules for every market. This approach ends in a complete rewrite a couple of markets later. Instead, create a shared text strings repository, and set up localization and automation workflows from Day 1. 

Additionally, you need to adapt your design library to account for translations of UI texts into other languages. Some designers meticulously craft pixels based on the product copy --- that's an anti-pattern. Text expansion in certain languages will break your UI and even critical user journeys. You'll need to make sure that the UI elements work well with text strings that are 30-50% longer than your original English word or that work well with right-to-left languages. **Remember: Just because you found a great, short English word for your new UI element doesn't mean that the translator will be able to do the same.** 

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQH6CeafAvA-GA/article-inline_image-shrink_1500_2232/0/1612907822053?e=1619049600&v=beta&t=faOnz9yX1pXiptNKHPJlDB5g3n6Br5bjgPuDZKXZyiM)

Lesson Three: Localize, Translate, and Beware of Regulation
-----------------------------------------------------------

When designing or developing for the world, it's easy to assume that the end-users are similar to us --- English-speaking with unlimited access to data and great connectivity for their new devices. However, international users (and the next billion, specifically) have diverse sets of needs, sometimes much different from ours. **When designing for the world, you need to forget all of your assumptions.** Here are three important aspects of localization to keep in mind:

### 1\. Architecture and culture

Each market has unique local infrastructures and cultures. These differences will affect your product in unexpected ways and impact your metrics. As an example, there are obviously many cultural differences in expression in real life and in online products. Users may be comfortable with entirely different ways of sharing their accomplishments, personal plans, and data. If your product relies on social sharing features, you might need to reposition the feature and nudge the users in culturally appropriate ways. If your nudges are delivered through notifications, you need to make sure you understand the most culturally acceptable mediums of communication. Some markets aren't as familiar with email (e.g., mobile-first users often don't see value in creating an email account). 

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQGipUwI56vRNA/article-inline_image-shrink_1500_2232/0/1612907883975?e=1619049600&v=beta&t=glQ6_ZLYVNjVHkAslUFsR0pbxSVKjXHXOqWMl9XVz7M)

### 2\. Translation process and inevitable translation errors

Language translation is obviously an important piece of localization. For that reason, you will have to make some important early decisions on how you're going to translate. Some questions to consider:

-   What translation management system (TMS) are we going to use? 
-   Who is going to do the translation? (in-house translator? translation agency?)

Once you've hired translators, you need to educate them on what your product does, specific terminology, tone, and so on. The education you provide will help limit translation issues. Know that when the UI text you write is sent to translators, it's generally extracted from the product-build and often presented to translators without any context whatsoever so mistakes in understanding will happen. You can spot those mistakes by comparing your product usage data across markets. **An incorrect translation or language nuance will cause a disparity in usage metrics for the affected feature.** 

### 3\. Regulation

Lastly, you need to pay attention to the legal requirements and restrictions unique to each market. These may influence your product on various levels, and you may need to modify critical user journeys and features. Examples:

-   You can't share or store user information outside of the country's borders (applicable to EU, Korea).
-   You might need to require specific legal consent format, order, and content. You might need to uncheck checkboxes or force the user to see full disclosure before accepting legal terms. 
-   A payment product is actually not fully legal in a given jurisdiction. 

To Summarize...
---------------

1.  Your next customer does not speak English. Do you want to serve them?
2.  Internationalize early to avoid pain in tech and design. 
3.  Translation != Globalization. Drop your assumptions and be ready to listen to local expertise.

**I have the first point on a post-it card on my desk to constantly remind me to think globally.** 

In the next part of this article, I will dive deep into tools and tactics for internationalization and localization. Stay tuned!
