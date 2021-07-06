# Sentimental Analysis

Sentiment analysis (or opinion mining) is a NLP technique used to determine whether data is positive, negative or neutral. Sentiment analysis is often performed on textual data to help businesses monitor brand and product sentiment in customer feedback, and understand customer needs.
<img src="images/sentimentanalysishotelgeneric-scaled.jpg" >

## About the Project

In this project we have performed sentimental analysis on a dataset of covid tweets containing 179108 tweets with 13 different features including user name,user description ,user location etc.
The models used include Naive Bayes, LSTM, Random Forest and XGBoost.
Feature extraction has been done using 2 algorithms namely Bag of words and Tfidf Vectorizer.
The train data has been created by using TextBlob.
  
## Data Visualization
 Various graphs have been plotted such as the number of unique values in each column, number of tweets from different locations, number of users in various locations etc.
 

## Data Preprocessing
The dataset contains text with various kinds of features which are not useful for the analysis.
We have converted text to lowercase, removed text in square brackets,removed links,removed punctuation
,remove words containing numbers, removed emojis, removed stopwords and done lemmatization. This helps in making feature extraction much more easier.

<body>
    <table>
        <tr border: 1.5px solid black border-collapse: collapse>
            <th>Before Cleaning </th>
            <th>After Cleaning</th>
        </tr>
        <tr>
            <td>If I smelled the scent of hand sanitizers today on someone in the past, I would think they were so
                intoxicated thatâ€¦ https://t.co/QZvYbrOgb0
            </td>
            <td>smelled scent hand sanitizers today someone past would think intoxicated that…</td>
        </tr>
        <tr>
            <td>Hey @Yankees @YankeesPR and @MLB - wouldn't it have made more sense to have the players pay their
                respects to the Aâ€¦ https://t.co/1QvW0zgyPu</td>
            <td>hey yankee yankeespr mlb wouldnt made sense player pay respect a…</td>
        </tr>
        <tr>
            <td>@diane3443 @wdunlap @realDonaldTrump Trump never once claimed #COVID19 was a hoax. We all claim that
                this effort toâ€¦ https://t.co/Jkk8vHWHb3</td>
            <td>wdunlap realdonaldtrump trump never claimed hoax claim effort to…</td>
        </tr>
        <tr>
            <td>#coronavirus #covid19 deaths continue to rise. It's almost as bad as it ever was. Politicians and
                businesses wantâ€¦ https://t.co/hXMHooXX2C</td>
            <td>coronavirus death continue rise almost bad ever politician business want…</td>
        </tr>
    </table>
</body>

## Modelling 
Different models were used and it was observed that the Tfidf Vectorizer was not a good feature extractor for this dataset.
After each model we found the accuracy score,balnced accuracy score and also did hyperparamater tuning in some cases.
<body>
    <table>
        <tr k>
            <th>Model </th>
            <th>Hyperparameter Tuning</th>
            <th>Feature Extractor </th>
            <th>Accuracy Score</th>
            <th>Balanced Accuracy Score</th>
        </tr>
        <tr>
            <td>Guassian Naive bayes	
            </td>
            <td>None</td>
            <td>Bag of Words
            </td>
            <td>0.692759</td>
            <td>0.636655</td>
        </tr>
        <tr>
            <td>Guassian Naive bayes	</td>
            <td>None</td>
            <td>Tfidf Vectorizer</td>
              <td>0.613757	</td>
              <td>0.565149</td>
        </tr>
        <tr>
            <td>Random Forest</td>
            <td>None</td>
            <td>Bag of Words
            </td>
              <td>0.736251</td>
              <td>0.676058</td>
        </tr>
        <tr>
            <td>Random Forest</td>
            <td>Randomized Search Cv	</td>
            <td>Tfidf Vectorizer
            </td>
              <td>0.635475</td>
              <td>0.676058</td>
        </tr>
    </table>
</body>

## Neural Network
We have created a Neural Network consisting of LSTM, embedding, batchNormlization, Desnsely connected layers. The batchNormlization and Desnsely connected layers have been used twice.
<body>
    <table>
        <tr>
            <th>Tuning by keras Tuner </th>
            <th>Best Accuracy Score</th>
            <th>Best Val_Accuracy Score </th>
        </tr>
        <tr>
            <td>Before	
            </td>
            <td>0.9312</td>
            <td>0.9034</td>
        </tr>
        <tr>
            <td>After</td>
            <td>0.9213</td>
            <td>0.9002</td>
        </tr>
    </table>
</body>
<img src="images/plot14.jpg" >
      





