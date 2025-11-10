<H3>NAME : Bhuvaneshwaran H</H3>
<H3>REGISTER NUMBER : 212223240018</H3>
<H3>DATE : 23.10.2025</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective :</H3>
  
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.

<H3>Program:</H3>
  
```py
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
```

<H3>Output:</H3>

<img width="681" height="859" alt="Screenshot 2025-10-23 092359" src="https://github.com/user-attachments/assets/93a89c97-4098-4ae4-99ce-e79c1b6352a2" />


<H3>Inference:</H3>
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
