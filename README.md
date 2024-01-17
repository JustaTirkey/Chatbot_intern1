
# ChatBot using Random Forest Classifier

## Introduction
This Python code implements a simple chatbot using a Random Forest Classifier for intent recognition. The chatbot is designed to understand user input and provide appropriate responses based on pre-defined patterns and responses stored in a dataset.

## Code Overview
The code consists of a main function `chatbot()` that initializes and trains the chatbot. Here's an overview of the key components:

1. **Data Loading and Preprocessing**
   - The code reads intent data from a JSON file (`intents.json`) and extracts relevant information.
   - Label encoding is applied to convert textual tags into numeric format for training.

2. **Random Forest Training**
   - The patterns in the dataset are tokenized and transformed into a Bag-of-Words (BoW) representation using CountVectorizer.
   - A Random Forest Classifier is trained on the BoW representations to predict the intent tags.

3. **User Input Processing**
   - User input is preprocessed by removing punctuation and converting it to lowercase.
   - TextBlob is used for spell correction.

4. **Intent Prediction and Response**
   - The trained classifier predicts the intent tag for the user input.
   - Based on the predicted tag, a response is randomly selected from the set of possible responses.
   - If the predicted tag probability is below a threshold, a default "Sorry, I don't understand this!!!" response is given.

5. **User Interaction Loop**
   - The chatbot engages in a continuous loop, taking user input until the user types 'exit' to end the conversation.

## Dependencies
- pandas
- numpy
- textblob
- scikit-learn
- string

## How to Run
1. Ensure the required dependencies are installed.
2. Place your intent data in a JSON file named `intents.json` with the structure specified in the code.
3. Execute the code to start the chatbot interaction. Type 'exit' to end the conversation.

## Additional Notes
- The code uses a RandomForestClassifier for simplicity, and you may explore other classifiers for better performance.
- Adjustments to the spell correction threshold and response probabilities can be made based on specific use cases.

Feel free to customize the code and dataset according to your needs.

