# To Override or to Not Override? PM's Conundrum.

My mom likes watching birds, my best friend likes a good stroll and I like thinking about the types of improvements product teams at Oura get to release.  Of course, there are big feature announcements, small content updates, and a perfectly reasonable number of bug fixes. However, I think that one of the most intriguing updates to the Oura app are improvements to its myriad of algorithms, for example, its Sleep stage detection, Readiness score or Activity detection.

Oura's algorithms are at the center of its user value, and for that reason Oura's data engineers are constantly improving their models. In 2017, [researchers](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6095823/) compared the accuracy of Oura to the gold standard, Polysomnography (PSG) to assess the efficacy of the ring. At first sight, the results ranged from "woah" to "whoops". Relative to PSG, Oura had 96% sensitivity for detecting sleep, 48% specificity for detecting wakefulness, 65% agreement in detecting "light sleep", 51% agreement in detecting "deep sleep", and 61% agreement in detecting REM sleep. However, this is not  unexpected - an elegant ring is not exactly a giant electronic octopus feasting on your brain:

\
![](https://lh3.googleusercontent.com/DmqemWiRnc-zRWgNg4W7SCIqHL7OzSdVkInC2bjWdp73vXs1rmD5x9pb7WzGEVfQXaWO1XlaoMkwtboWyEajvaRJ9zv5EK1nN9lHV8L5qFn84uaeyNOy6FAfid3FsQFGUYsN8sQG)

_Polysomnogram setup & record_ ([source](https://www.psychdb.com/neurology/polysomnography))

We also know that the Oura team is focused on improving these metrics. In 2021 [a similar study](https://www.researchgate.net/publication/349306698_Multi-Night_Validation_of_a_Sleep_Tracking_Ring_in_Adolescents_Compared_with_a_Research_Actigraph_and_Polysomnography) was done, and the results were markedly better. Since updating the hardware implies releasing a new ring (HELLO Gen3, coming my way in a couple weeks!) model improvements  are the one lever to rely on.


## What would the release of such an improvement look like?

Imagine waking up one morning to a push notification from Oura informing you that "your data has been updated". You click through, and the first thing you see is your readiness is several points below your norm. You scroll to see your sleep metrics and note both deep sleep and REM are down 15 minutes. If you click through to trends, you'll see similar drops everywhere. _What's happening?!_ _What did I do?!_ You first question yourself, but then you question the device.


## Why did my historical data change? The PM conundrum - "to override (data) or to not override"

This is a good tradeoff question that I would want to mull over as a Product Manager at Oura: In case of a model update that leads to significant changes in the data, would I want to "override" the old data and show "corrected" historical data to the user? I'm assuming that we would want to use the new model going forward, however, it isn't so clear what to do about the historical data.

First, let's start with a few  considerations. If the change is dramatic, it will lead to a confusing experience for the majority of your users (case described above). People that have been tracking their data judiciously (researchers, coaches, pro athletes) will feel like their understanding of their metrics has been invalidated. _What is a good night of sleep anymore?_ Any experiments that users or researchers are currently conducting on their bodies may be rendered useless. In short, you might piss off your biggest believers.

On the other hand, having accurate data is better for those same groups of super users. If it turns out that they are actually sleeping better or worse than they thought, this insight could be extremely valuable. Additionally, depending on the type of errors (systematic vs random), over time if you don't update the historical data, users' trends will be all wrong.

In sum, there are two user groups here that will have an entirely distinct experience with the update:

1.  Normal users 

-   If the changes are small or the errors cancel out, most users won't notice.

-   Updating previous data might be very confusing. That said, if we continue improving over time, the long-term trends may not make sense depending on the type of error. 

2.  Super users who notice even small variations 

-   If there are on-going studies, updating previous data will be a very bad idea.

-   Otherwise, better data means better insights, so they may benefit from the update.


## What would I do?

I'd work with the data team to figure out how the change would impact users of all types (focusing on the two segments described above).

Systematic errors will affect the trends and therefore it may make sense to 'correct' the historical data  (e.g., if deep sleep is confused with light sleep more often than the converse). If the errors are systematic and the model updates improve detection significantly (where users would notice the differences) we might consider two example paths:

1.  We allow users to decide whether to update or not - On software update, we present the user with a CTA

2.  We show both: the old and new historical datasets - Maybe with a drop-down while reviewing the trends.

I would sketch both of these options and consider additional questions such as: What to do on further updates? Will we show a user the option to update their historical data every time we update the model? Do we show historical data for every version of the algorithm?

On the other hand, if the errors are randomly distributed, they would cancel out, i.e the long-term trends would stay correct. Sleep stage classification will be wrong as often as it is right, rendering the averaged values correct.  If you take this, along with the fact that the ring hardware has limitations that are not solvable via software I would expect most model modifications to have marginal effect on the long-term trends. This is why scientists take several measures in experiments - most errors diminish as the number of data points  increase.


## Unsatisfying end to my deliberation

After agonizing over this question for a full week I arrived at a disappointing answer: **This is most likely a no-op.**

My gut feeling is that  the team at Oura leaves the historical data as is and only uses the new model with new data. That said, pro users may still have an option to update historical data via a one-off request.
