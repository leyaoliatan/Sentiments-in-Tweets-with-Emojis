
# Sense Exploring of Emojis with Word2Vec Model and Using Emojis to Modify Short-text Sentiments Classification
![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTigQWzoYCNiDyrz1BN4WTf2X2k9OZ_yvW-FsmcIMsdS9fppNmh)

## step1-Data collection
    - period: 2022-0415-2022-0528
    - filter: retweet or media
    - querry: tweeets that contain at least one concerned emoji
 
Our dataset consists of Tweets which contain at least one of the following emoji:
The baseline selection of common-used emoji refers to [Ian D. Wood, Sebastian Ruder, 2016](https://www.researchgate.net/publication/321057905_Emoji_as_Emotion_Tags_for_Tweets)
        
The tag of emoji is besed on human intuition accroding to the original paper, instead of meaning in context.
<img width="369" alt="image" src="https://user-images.githubusercontent.com/99280254/165020171-62551399-f2a6-40e3-93bc-35b9e65b06b9.png">


## step2-Data cleaning   
### 2.1-First EDA
### 2.2-Data cleaning
        
For English tweets, we follow the following steps:      

    1. remove url
    2. remove user names
    3. remove punctuations
    4. remove stopwords
    5. lower the words
    6. lemmatization
    7. keep only english characters and emojis
        
For Chinese tweets, we:     
        
    1. remove url
    2. remove user names
    3. cut the words
    4. remove stopwords (en & zh)
    5. transform to simplified Chinese
    6. remove punctuations (en & zh)
    7. remove sensitive Chinese words
    8. remove non-chinese words

### 2.3-Extract pure emojis and text   
And, we generate 3 new coloumns which:
- remove all emojis      
----
- include all emojis
        
----
- only include concerned emojis

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


For Chinese tweets, we follow the following steps:      
1. remove url
2. remove user names
3. cut the words
4. remove stopwords (en & zh)
5. transform to simplified Chinese
6. remove punctuations (en & zh)
7. remove sensitive Chinese words
8. remove english words

And, we generate 3 new coloumns which:
                
        - 1) remove all emojis
        - 2) all emojis
        - 3) only concerned emojis
         
## step3-EDA & Word embedding
### 3.1 data exploring
1. plot the most frequent emojis        
                
<img width="864" alt="image" src="https://user-images.githubusercontent.com/99280254/171414950-28c5fdd0-3533-4380-a6ca-2be1c429bfe0.png">

### 3.2 word embedding
1. Word2Vec word embedding with only emoji
2. word embedding with both emoji and words


## step4-Sentiment Classification
### 4.1 Method 1: only text
### 4.2 Method 2: text + emojis' description names
### 4.3 Method 3: text + emojis' most similar text tokens
### 4.4 method 4: text + pre-trained word embedding model
