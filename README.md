### NAME : M J ANISH
### REGISTER NO : 212221230005
### DATE:11/5/2024
### Project Based Experiment
## Objective: 
Perform sentiment analysis using your Facebook data and filter the data that has only neutral feedback for the code given in the following link.
## Program:
```
import pandas as pd
from textblob import TextBlob

# Load your Facebook data from CSV into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Filter the DataFrame to include only rows with neutral sentiment
neutral_feedback = df[df['Sentiment'] == 0]  # Sentiment polarity of 0 indicates neutral sentiment
```
# Output the neutral feedback


## Output:
![image](1.png)

## Inference:
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only neutral feedback for the code is done.

