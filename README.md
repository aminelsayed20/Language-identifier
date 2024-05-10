# Language Detection using Naive Bayes Classifier

This repository contains Python code for detecting the language of a given text using a Multinomial Naive Bayes classifier. The classifier is trained on a dataset containing text samples in multiple languages.

## Dataset

The dataset used for training the classifier is provided in the file `Language Detection.csv`. It contains two columns:

- `Text`: Text samples in various languages.
- `Language`: Corresponding language labels for each text sample.

## Dependencies

- pandas
- scikit-learn

You can install the dependencies using pip:

```
pip install pandas scikit-learn
```

## Usage

1. Clone the repository:

```
git clone https://github.com/your_username/language-detection.git
```

2. Navigate to the repository directory:

```
cd language-detection
```

3. Run the Python script:

```
python language_detection.py
```

## Description

- The script loads the dataset using pandas.
- It splits the dataset into features (`X`) and labels (`y`).
- Splits the dataset into training and test sets using `train_test_split` from scikit-learn.
- Converts the text data into numerical features using `CountVectorizer`.
- Trains a Multinomial Naive Bayes classifier using the training data.
- Evaluates the classifier's accuracy on the test set.
- Defines a function `predict_language` to predict the language of a given text.
- Tests the model with some sample texts.

## Example

```python
sample_texts = [
    "Hola, ¿cómo estás?",
    "Bonjour, comment allez-vous?",
    "Привет, как дела?",
    "Hello, how are you?",
    "مرحبا انا استخدم اللغه العربيه"
]

for text in sample_texts:
    predicted_language = predict_language(text)
    print(f"The language of '{text}' is predicted to be: {predicted_language}")
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
