# animemangatoon_AI_assignment

**task 1:**
Text Classification using Naive Bayes
1. Data Preparation
A small dataset of webtoon descriptions and their corresponding categories was created. This dataset consists of ten descriptions and their associated genres, such as "romance" and "fantasy."
The data was organized into a pandas DataFrame for ease of manipulation and processing.
2. Feature Extraction
The TfidfVectorizer was employed to convert the textual descriptions into numerical features. This process uses the Term Frequency-Inverse Document Frequency (TF-IDF) method, which measures how important a word is to a document in a collection.
The resulting feature matrix X represents the descriptions in a format suitable for model training, while the target variable y contains the respective categories.
3. Model Selection
The Multinomial Naive Bayes classifier was selected as the model for classification. This algorithm is particularly effective for text data, as it assumes that features (words) contribute independently to the outcome.
4. Cross-Validation
Five-fold cross-validation was performed to evaluate the model's performance. This technique involves splitting the dataset into five subsets, training the model on four subsets while validating it on the remaining subset, and repeating this process five times.
The mean cross-validation accuracy score provides a robust estimate of the model's generalization ability.
5. Train-Test Split
The dataset was divided into training and testing sets using an 80-20 split, ensuring that the model could be trained on a substantial amount of data while still having a separate portion for testing.
6. Model Training
The Naive Bayes model was trained using the training data (X_train and y_train).
7. Model Evaluation on Test Set
After training, the model was evaluated on the test set (X_test). Predictions were made to classify the webtoon descriptions into their respective categories.
8. Results
The mean cross-validation accuracy was calculated to assess the model's reliability.
The accuracy score on the test data was reported, along with a classification report that included precision, recall, and F1-score metrics for a comprehensive evaluation of the model's performance.

**task 2:**
Sentiment Analysis of User Comments
1. Sample User Comments
A sample dataset of user comments was created to reflect opinions on "The Difference Between Manga And Manhwa." This dataset includes a variety of comments expressing different sentiments regarding both mediums.
2. Sentiment Analysis
The TextBlob library was utilized to analyze the sentiment of each comment. This library provides a simple API for common natural language processing (NLP) tasks, including sentiment analysis.

For each comment, the sentiment polarity was assessed:

A polarity greater than 0 indicates a positive sentiment.
A polarity less than 0 indicates a negative sentiment.
A polarity equal to 0 indicates a neutral sentiment.
Two counters, positive_comments and negative_comments, were maintained to track the number of positive and negative comments, respectively.

3. Percentage Calculation
After analyzing all comments, the percentage of positive and negative comments was calculated. This was done by dividing the count of positive and negative comments by the total number of comments and then multiplying by 100.
4. Output Results
The total number of comments analyzed was printed, along with the calculated percentages of positive and negative comments. This provides a quick overview of the general sentiment of the user feedback regarding the topic.

**task 3:**
Castle Swimmer Chatbot Implementation
1. Setup and Data Preparation
The NLTK library is imported to handle natural language processing tasks. Specifically, the word_tokenize function is utilized to break down user input into individual words (tokens).

Required NLTK data (the Punkt tokenizer) is downloaded to ensure tokenization functionality.

A dictionary called responses is defined, containing predefined responses related to the "Castle Swimmer" plot, including details about the main characters and summaries of chapters 83 to 89.

2. Response Function
The get_response function is implemented to generate appropriate responses based on user input:
User input is converted to lowercase and tokenized to facilitate keyword matching.
The function iterates through the predefined responses, checking if any keywords from the responses dictionary appear in the user's input.
If a match is found, the corresponding response is returned. If no keywords match, a default message ("I'm sorry, I don't understand that question.") is provided.
3. Chatbot Interaction Loop
The chatbot function manages the interaction with the user:
A welcome message is displayed to introduce the chatbot.
A loop is initiated to continuously accept user input until the user types "exit."
Each user input is processed by the get_response function, and the corresponding bot response is printed.
If the user chooses to exit the chatbot, a goodbye message is displayed, and the loop terminates.
4. Execution
The chatbot is launched by calling the chatbot function, allowing users to engage in a conversation about the "Castle Swimmer" storyline, specifically focusing on chapters 83 to 89 and main characters.
