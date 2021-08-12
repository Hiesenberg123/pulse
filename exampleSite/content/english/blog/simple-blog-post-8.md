---
title: "Inorganic Twitter Activity around Anti-Farm Law Protests"
author: "Kunal Anand"
date: '2021-06-25T14:51:12+06:00'
output:
  html_document:
    df_print: paged
image_webp: images/blog/blog-post-2.webp
description: This is meta description
image: images/blog/blog-post-2.jpg
---

The rise of Social Media has led to the proliferation of trolls and bots. These inorganically created accounts might be innocuous, just trying to entertain themselves at others’ expense, at the same time they can also be political actors sowing mistrust or discord in the larger society.
Document lays out the steps for detection of such accounts on social media platforms and their impact on narrative shaping, using the case of ongoing protests against the farm law. For the purpose of the study, we scraped 8,600 tweets with the search item “#farmlaws” from the date range of “18-26 June”. Around 1600 unique users have been analyzed for the study. Out of which, 200 were identified as inorganic accounts that have been created for the purpose of giving a boost to the protest in digital space.

## Framework for identification of inorganic accounts

The major steps for detection of such accounts would include the following elements

![Framework](https://pbs.twimg.com/media/E8hA8CMVgAA9cl3?format=png&name=small)

Data Collection- from the social media sites through API’s. This data would be sanitized for feeding into our model.

## Major features used for classifying such inorganic accounts

The following features have been found more often to be the defining features for identifying a troll. The magnitude of the relevance of each feature varies from case to case. Therefore while analyzing data in any machine learning model these fields should be analyzed for their correlation for incidence of trolls.

### 1. Profile Features:

#### Name and description of profiles (Twitter Handle)

Name and description of fake and troll accounts often have similarities and are correlated with any particular agenda.
Profile Picture: Genuine profiles have a much larger probability of having a profile picture compared to troll accounts.

Below, two-word clouds present the word clouds of profile description of profiles created before and after Jan 2020. It clearly depicts the following features:
- Increased correlation of description with farmer’s protests
- The presence of keywords like a farmer, Kishan, Punjabi words have increased significantly
- Canada flag icon is visible with many accounts

![Description New](https://pbs.twimg.com/media/E8hCARYVEAUUNob?format=jpg&name=small)
 
> *Fig 1: Description of profiles created after Jan, 2020* 


![Description New](https://pbs.twimg.com/media/E8hCARaUUAAL24G?format=jpg&name=small)
>*Fig 2: Description of profiles created before Jan, 2020*

#### Date of account creation

Inorganically created accounts are usually created in bulk at a particular time instance of significance such as before elections, or any major events. As portrayed by the graph below, the frequency of account creation captured in our study increased significantly (almost doubled) closer to the farmer’s protests. It proves that the growth of handles opinionating in support or against of farmer’s protest was not all organic.

![Description New](https://pbs.twimg.com/media/E8hH5OeVIAM6F1z?format=png&name=small)
>*Fig 3: Month-wise distribution of Account creation*

### 2.Behavioral features: Stylometry

Number and type of Hashtags used in a comment: Analysis of hashtag pattern of accounts under consideration was done for recent tweets. Pattern clearly shows the overwhelming presence of hashtags related to farmers' protests in accounts that were created after Jan 2020. Hashtags like Savefarming_SaveDemocracy formed more than 35% of total hashtags in accounts which were created after Jan 2020, whereas it formed only 8% of total hashtags in accounts which were created before Jan 2020.

![Description New](https://pbs.twimg.com/media/E8hH7z-VgAYXZUw?format=png&name=small)
>*Fig 4: Comparison of hashtags used in the account created before Jan 2020 and after Jan 2020*


#### Frequency of using particular words

The likelihood of such accounts repeating a particular set of words is much higher than any normal account. The graph shows the probability of word repetition declines after reaching a peak in a normal tweet, while the same remains at a high level in a troll/ bots.

### Identification of troll accounts

Above analysis helped us in identifying potential troll accounts. Accounts matching most/ all of these criteria were identified as inorganic account created for the purpose of increasing digital support for protests only
- Accounts created after Jan 2020
- Accounts with clear descriptions mentioning farmer protests etc.
- Accounts with an overwhelming presence of hashtags and contents supporting the farmer protests
- Accounts following a disproportionately high number of leaders or influencers in support of farmers protests
- Recent online activities mostly related to farmer protests

### Results

A Machine Learning model was prepared earlier to identify the sentiment around any tweet for ongoing farmers’ protest wrt Central Government. Here, we have done a comparison of overall sentiment around these tweets among the troll/ fake/ bot accounts and non-troll accounts as identified by our model. A comparison reveals a significant difference in sentiment between the two sets as portrayed by the two plots below.

![Description New](https://pbs.twimg.com/media/E8hH9L2VIAEyKTZ?format=png&name=small)
>*Fig 5: Twitter sentiment around farm laws among the identified troll accounts*

![Description New](https://pbs.twimg.com/media/E8hH-ZrUYAEbdCB?format=png&name=small)
>*Fig 6: Twitter sentiment around farm laws among the identified non-troll accounts*
