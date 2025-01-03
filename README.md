> [**Return to Portfolio home**](https://krista-lowry.github.io/portfolio/)

>[Access Project in Git View](https://github.com/krista-lowry/funnel-cro)

# Project 2: Funnel Conversion Rate Optimization and A/B Testing
This project materialized after my team made an observation, over multiple previous CRO experiments, that a few distinct user patterns were emerging. We were noticing the following user types and associated behavior patterns:
- Bouncers (users who don't convert)
- Clickers (users who convert)
Although these user segments are obvious (anyone who doesn't convert is a bouncer, right?), they were important for us to distinguish because we needed to intentionally optimize for the non-converter behavior pattern.

It was clear in our past winning experiments that we had optimized for the Clickers user segment well, but were missing the mark on the Bouncers. To approach this problem, we needed a clearer view of the Bouncers and their behavior patterns: Did they spend time on the page and leave, or did they leave right away? If they did spend time on the page, what were they doing?

## Research
To approach this issue, I gathered data from Google Analytics and from a user survey.

#### Google Analytics data
Using GA4 data, I grouped users into segments depending on events in their session. I utilized Google Tag Manager event tracking and GA4 custom dimensions I had set up previously:
- Scroll tracking, using Google Tag Manager's default scroll trigger 
- Ad visiblity, using Element Visibility triggers
- Ad click, using click listener triggers

#### User Survey
I also put together a proposal for a user survey. This was the first survey we had run on this domain, so I needed to get explicit stakeholder approval. My proposal included the project background, goal, proposed survey design, and supporting data.

After gaining approval, I collaborated with a UX researcher to design a SurveyMonkey survey asking users if they were able to find the information they were looking for.

To mitigate any negative impact on the Clickers user segment, we ran two surveys with triggers aimed at the Bouncers:
1. Time-delayed Survey, displayed after 20 seconds
2. Exit-intent Survey, triggered when the user moves to exit the browser

## Research Findings
The survey results showed that user's primary pain point is missing information. They were frustrated that the article did not contain key information that they expected, naturally leading to a bounce instead of a conversion.

After combining the survey data with GA4 data, a distinct pattern emerged: Bouncers are scrolling quickly, spending less than 20 seconds on the page, and are not converting. These are roughly 30% of users.

<img src="images/proj-1b-scrol.png" alt="Sample Image" width="200" height="150" align = "center">


The next question is: How can we capture the bouncers attention before they leave?

## Proposal: Related Post widget
<img src="images/proj-1c-pop.png" alt="Sample Image" width="50" height="150" align="left" style="margin-right:25px">


I designed an idea for a Related Posts popup. This would serve a dual purpose of capturing the user's attention at a key point in the funnel and offering them the information they are presumably missing.

**Hypothesis:** If we can capture the user's attention at key point in the funnel and offer relevant information via a related posts popup, then users will continue in our funnel and convert.



### Proof-of-Concept Test Details
Scope:
- To reduce the scope, we will run a very limited experiment with only one article. The article will have a high volume of traffic with diverse traffic sources.
- No dev work needed upfront:
    - Related posts will be hand-picked for relevancy
    - Popup will be created and deployed through a third-party tool and managed through their platform

Design:
- Experiment Length: 7 days
- MDE: 8%
- Power: 95%
- Confidence: 95%
- Sample size: x,xxx sessions
- Number of variants: 2 (Control and Popup)

Success Criteria:
- Revenue KPI deltas must be greater than 8% to detect a significant effect.

## Experiment Results
Ultimately, the data showed that we can't detect any effect over the control towards the negative or positive: Revenue KPI deltas were below the defined MDE of 8%.

**Popup data**: The popup had a very low CTR (<5%), but intent was high in the users who did click on a related post. In fact, after the user clicked on a related post, they exhibited behaviors similar to the Clickers:
- Conversons on the Related Posts were higher than average
- Scroll depth on the Related Posts were lower than average
- Users who converted on a Related Post did so within 20 seconds

## Looking forward
We planned to expand this test on a larger scale. If we increase popup impressions by rolling this out on more pages and sustain the high conversion rate on the click-through posts, then we could generate signficant total revenue lift. 

> [**Return to Portfolio home**](https://krista-lowry.github.io/portfolio/)
