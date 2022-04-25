
# Emoji Sentiment Analysis with Tweets
![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTigQWzoYCNiDyrz1BN4WTf2X2k9OZ_yvW-FsmcIMsdS9fppNmh)

## step1-Data collection
    - period: 2022-0415-2022-0425
    - filter: retweet or media
    - querry: tweeets that contain at least one concerned emoji
 
Our dataset consists of Tweets which contain at least one of the following emoji:
The baseline selection of common-used emoji refers to [Ian D. Wood, Sebastian Ruder, 2016](https://www.researchgate.net/publication/321057905_Emoji_as_Emotion_Tags_for_Tweets)
        
The tag of emoji is besed on human intuition accroding to the original paper, instead of meaning in context.
<img width="369" alt="image" src="https://user-images.githubusercontent.com/99280254/165020171-62551399-f2a6-40e3-93bc-35b9e65b06b9.png">


## step2-Data cleaning          
For English tweets, we follow the following steps:
    1. remove url
    2. remove user names
    3. remove punctuations
    4. remove stopwords
    5. lower the words
    6. lemmatization
    
And, we generate 3 new coloumns which:
                
        - 1) remove all emojis
        - 1) remove non-english words
        - 2) all emojis
        - 3) only concerned emojis

-----------
For Chinese tweets, we follow the following steps:
1. remove url
2. remove user names
3. cut the words
4. remove stopwords (en & zh)
5. transform to simplified Chinese
6. remove punctuations (en & zh)
7. remove english words

And, we generate 3 new coloumns which:
                
        - 1) remove all emojis
        - 2) all emojis
        - 3) only concerned emojis
         
## step3-EDA
1. plot the most requent emoji          
                
For English tweets:             
<img width="637" alt="image" src="https://user-images.githubusercontent.com/99280254/165021160-4a3396c3-363e-44f6-8ebb-e52bf0005c2b.png">

        
For Chinese tweets:             
<img width="669" alt="image" src="https://user-images.githubusercontent.com/99280254/165021062-f4f3c924-731d-4113-a788-0989f8c782cb.png">


## step3-Basic model
2. topic moedel with emoji using in english tweets --- first galance of emoji meaning
3. word embedding with only emoji
4. word embedding with both emoji and words


