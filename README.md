# Emotion Bubbles: Tracking Emotional Compositions of Online Discourse Before and After the COVID-19 Outbreak

Assem Zhunis, Gabriel Lima, Hyeonho Song, Jiyoung Han, and Meeyoung Cha. 

In Proceedings of the ACM Web Conference 2022 (WWW ’22), April 25–29, 2022, Lyon, France.

------
## Abstract:

The COVID-19 pandemic has been the single most important global agenda in the past two years. In addition to its health and economic impacts, it has left marks on people’s psychological states with the rise of depression, domestic violence, and Sinophobia. We traced how the overall emotional states of individual Twitter users changed before and after the pandemic. Our data, including more than 9 M tweets posted by 9,493 users, illustrated that the threat posed by the virus did not upset the emotional equilibrium of social media. In early 2020, COVID-19-related tweets skyrocketed in number and were filled with negative emotions; however, this emotional outburst was short-lived. We found that users who had expressed positive emotions in the pre-COVID period remained positive after the pandemic, while the opposite was true for those who regularly expressed negative emotions. We found that individuals achieved such emotional consistency by selectively focusing on emotion-reinforcing COVID-19 subtopics. The implications of the present study are discussed in light of emotionally motivated confirmation bias, which we conceptualize as emotion bubbles, and public resilience to a global health risk.

------
This repository contains data used for the analysis in the paper mentioned above. 

The dataframe is divided into 9 files (thewebconf22_x.pkl) which have to be combined to make full analysis. 

The columns include: 
'userNumber', 'tweetID', 'created_at',
       'anger', 'anticipation', 'disgust', 'fear', 'joy', 'love', 'optimism',
       'pessimism', 'sadness', 'surprise', 'trust', 'opinion',
       'covid_related', 'vaccine_related', 'china_related'.
       
* Emotional tags are given by using ML model developed by Baziotis et al. 

* 'opinion' tag is given by our ML model. We trained it on the dataset provided in the paper by Dusmanu et al. (Accuracy = 0.69, F1 = 0.8). This tag was not used in the analysis, we give it for reference.
       
*  'covid_related', 'vaccine_related', 'china_related' tags were labeled according to the keywords shown in the table below. 'vaccine_related', 'china_related' tags were not used in the paper as well.

|   **Topic**  |                              **Keywords**                              |% of all tweets|
|:--------:|:------------------------------------------------------------------:|:----------------:|
| COVID-19 | 'covid', 'ncov', 'corona', 'sarscov2', 'pandemic', 'virus', 'viru' |       5. 38      |
|   China  |                               ‘china’                              |       0.87       |
|  Vaccine |                'vaccine', 'vaccination', 'vaccinate                |       1.20       |
|  Opinion |                                 --                                 |       76.90      |
