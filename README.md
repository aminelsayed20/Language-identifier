This project is a language detection model built using Python and the scikit-learn library. Here's a breakdown of the different components:

Data Loading: The project starts by loading a CSV file named "Language Detection.csv" into a Pandas DataFrame df. The dataset contains text data and their corresponding language labels.

Data Preprocessing: The dataset is split into features (text data) X and labels (language) y. The data is then further split into training and test sets using the train_test_split function from scikit-learn.

Feature Extraction: A CountVectorizer is used to convert the text data into numerical features. The fit_transform method is applied to the training data, and the transform method is used to transform the test data.

Model Training: A Multinomial Naive Bayes classifier (MultinomialNB) from scikit-learn is used to train the language detection model. The fit method is called to train the model on the vectorized training data.

Model Evaluation: The trained model is evaluated on the test set using the predict method. The accuracy score is calculated using the accuracy_score function from scikit-learn and printed.

Prediction Function: A function predict_language is defined to take in a text input and predict the language using the trained model. This function uses the transform method of the CountVectorizer to convert the input text into numerical features and then uses the predict method of the Multinomial Naive Bayes classifier to predict the language.

Sample Predictions: The predict_language function is used to predict the language of some sample text inputs, and the results are printed.

The goal of this project is to develop a language detection model that can accurately predict the language of given text inputs. The Multinomial Naive Bayes classifier was chosen as the model because it is well-suited for text classification tasks. The CountVectorizer is used to convert the text data into numerical features that can be processed by the machine learning model.

The project demonstrates the end-to-end process of building a language detection model, including data loading, preprocessing, feature extraction, model training, and model evaluation. The sample predictions show how the trained model can be used to detect the language of new text inputs.
