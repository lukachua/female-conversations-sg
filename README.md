
# DSI-25 Capstone Project
#Female Conversations Online in Singapore: What is She Talking About?
### Topic Modelling of Female-focused YouTube Content


## Problem Statement

With the gradual liberalisation of the Singapore society that place a higher value on self-expression and freedom of thought, more female-focused content can be found online in the form of serious conversations that reflect the current concerns, opinions and values of Singapore women. Due to the personal and intimate nature of such conversations that are rooted in the local customs and cultures, such sentiments are not easily generalised or derived from information or studies conducted outside of Singapore. However, these feature-rich content are frequently overlooked as a source of information on female perspectives in Singapore as they form only a small portion of all local content created online. Hence, this project aims to use Natural Language Processing (NLP) techniques of Topic Modelling to uncover the everyday concerns and opinions of women in Singapore.

---

## Executive Summary

In this project, I have attempted to give insight to the topics of interests in female-focused video online by local creators using topic modelling techniques of LDA, Top2Vec and BERTopic. The main topics found in online female-focused conversations are: health, family planning, relationships, conflict management, harassment, identity, gratefulness, career and finance.

---

## Background

The past few decades have witnessed one of the most dramatic cultural changes that has occurred since the dawn of recorded history. Singapore too, has become more liberal since 2002, the first time it participated in the World Values Survey (WVS) - a global research project monitoring changing public beliefs and their socio-political impact over time across 80 countries ([source](https://www.straitstimes.com/singapore/community/singapore-still-conservative-on-moral-sexuality-issues-but-more-liberal-since)). The WVS has demonstrated over the years that people’s beliefs play a key role in economic development, the emergence and flourishing of democratic institutions, the rise of gender equality, and the extent to which societies have effective government. Advancements in technology has also not stagnated through the decades and most societies now have access to the internet and its various social networks. In a liberal post-industrial economy, an increasing share of the population has grown up taking survival and freedom of thought for granted, resulting in that self-expression is highly valued ([source](https://www.worldvaluessurvey.org/WVSContents.jsp)).

The algomation of the above realities have led to the rise of self-expression online in various forms on a wide range of platforms ([source](https://viewpoint.pointloma.edu/the-rise-of-the-social-media-influencer/)), including higher visibilities and more serious discussions on female-focused topics that have traditionally been overlooked or discouraged from being openly addressed ([source](https://womenlovetech.com/female-founders-apply-science-to-womens-health-issues/)). This global phenomena has also spread to Singapore and it is now more common than before to find videos, podcasts and other forms of social media contributions that have a female-centric focus or tackle female-related issues.

While these forms of female-focused content are present in our local online ecosystem and can be accessed easily by many,  they form only a small percentage of the information that online users are overwhelmed with daily ([source](https://www.wsj.com/articles/social-media-algorithms-rule-how-we-see-the-world-good-luck-trying-to-stop-them-11610884800). As a result, they are frequently overlooked as a source of information that can have larger impacts in the real world.
Using the ShiftPush API, our team collected about 2000 posts from the subreddits of cryptocurrency and investing, and will be building a suitable Natural Language Processing classifier model to cater to the needs of the company. We have also narrowed down the training model types to: Logisitic Regression and Naive Bayes. This report will walk the reader through the process of setting up the classifier model for the company.

---

## Project Impact

This project aims to analyse the topics discussed in a selection of Singapore-based female-focused YouTube channels to look into the concerns, opinions and values of Singaporean women through the use of topic modelling in Natural Language Processing (NLP). Sentiments expressed in these content are often unique to Singapore due to the personal and intimate nature of such discussions and are hence very valuable as they cannot be fully generalised from information obtained anywhere else other than in Singapore due to cultural and accessibiliy reasons. 

Online content can be used to provide an indicator of the current trends related to women in Singapore and have been shown to have far-reaching impacts ranging from product development ([source](https://www.sciencedirect.com/science/article/pii/S0148296320301363)), marketing campaigns ([source](https://digitalcontentnext.org/blog/2020/04/10/evaluating-the-value-of-media-content/) to wide-sweeping social change ([source](https://www.thedrum.com/opinion/2020/06/19/the-importance-social-media-instigating-social-change). As a serious discussion format, it is also an informal educational outlet that the younger, more tech-saavy girls have easy access to. The amount of online content has been growing and will only continue to grow, and so will female-focused content that are produced in Singapore. Therefore, it is worthwhile to know what topics have been addressed so that more varied narratives could be added to the present collection to provide more diverse perspectives for a wider reach.

---

## Dataset

The dataset used in this project is vectorised from the Google Cloud Speech-To-Text API text transcripts. These transcripts were obtained from 45 hours of audio content scraped from 2 local YouTube channels, [itsclarityco](https://www.youtube.com/channel/UCEAGCuChX7adlus-NQOamog/featured) and [Something Private](https://www.youtube.com/channel/UCAZ7NfSRX1reSpRUw0xtEmg). The 130 videos were obtained in batches over a span of two weeks from 28 November to 5 December 2021, and have upload dates ranging from 19 September 2020 to 1 December 2021.

---

|Feature|Type|Dataset|Description|
|---|---|---|---|
|text corpus|*str*|text_df|Text transcript of speech content scrapped from YouTube videos|

---

## Summary of analysis

Topic modelling is an unsupervised machine learning technique and in this project, we attempt to analyse the contents of female-focused conversations by Singapore creators on YouTube using several models. Although BERTopic proved to be the most helpful in providing context, I believe that taking the combined results from all the models and using them to derive overall insights might possibly be the most helpful approach.

From the model analyses, here are the topics of concern: health, family planning, relationships, conflict management, harassment, identity, gratefulness, career and finance.


---

## Conclusion

Despite the best efforts to tackle the problem statement, some limitations remain in this project:

- The size of the data sample is small at 45 hours of speech, especially so after the more impactful words are extracted. The data is also collected from only two YouTube channels due to availability. Future studies can include a bigger sample with data collected from other social media such as podcasts and social media text and image posts.

- The speech transcriptions are assumed to be fully accurate but that is not so, especially in the case of the more female-specific terms. Studies have shown that bias is present in AI and machine learning algorithms (source) and an extension of this project could include working on the automatic speech recognition (ASR) models for accuracy taking into account the Singapore English accent and the female-specific keywords. Insights and keywords from this project could be used to optimise the ASR model for better accuracy, which could then be used to improve the results of this project.

- The participants of the female-focused conversations in my dataset are mainly those who are in their twenties and thirties. Their opinions are hence unlikely to reflect those of women of all ages in Singapore and hence should only be considered for women of the specific age range.

In this project, I have attempted to give insight to the topics of interests in female-focused video online by local creators using topic modelling techniques of LDA, Top2Vec and BERTopic. My analyses revealed that they have concerns that is common of most urban populations, but discussions around relationships and identity have a more unique Singaporean/Southeast Asian twist to it. In this era of self-expression and gradual liberalisation, the creation of female-focused local content and the perspective shift they represent are invaluable observations of the everyday concerns of young women.
