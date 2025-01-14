# NBA-Sentiment-Analyzer

Reddit Data Scraper: 
Used PRAW to collect data about all the different NBA teams using the NBA subreddit as well as the specific team subreddits. Using the script, I was able to extract a dataset of roughly 120,000 reddit posts regarding the NBA with features such as title, author, # of comments, id, link, etc. 

Data Cleaning/Preprocessing: 
To clean the data I created a pipeline with the following steps: 
1. Remove duplicate rows from the dataframe
2. Remove irrelevant characters like URLs, special characters, and HTML tags
3. Normalized data by converting all text to lowercase
4. Remove stop words (common words (e.g., "is," "the," "and")
5. Normalize Whitespace

Labeling: 
Then using the NLTK library, I labeled the data as positive, negative, or neutral. Encoded these labels as 2, 0, and 1 respectively.

Tokenization: 
Using the RoBERTa Tokenizer from the Hugging Face library, I tokenized the data by using padding/truncation for tokens with roughly even lengths. 

Model/Prediction System: 
RoBERTa was the best model due to it's versatility and it's ability to handle nuanced text like reddit comments well especially since the subreddits I pulled from had subtle sentiment expressions. 
