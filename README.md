# English to French Language Translator

This project implements a simple language translator using a Sequence-to-Sequence (Seq2Seq) model with LSTM architecture. The model translates English sentences into French using TensorFlow and Keras.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Dataset](#dataset)
- [Usage](#usage)
- [Training the Model](#training-the-model)
- [Inference](#inference)
- [Contributing](#contributing)

## Introduction

Language translation is an essential application in natural language processing (NLP). This project aims to build a Seq2Seq model that can accurately translate English sentences into French. The Seq2Seq architecture allows the model to handle variable-length input and output sequences, making it suitable for translation tasks.

## Features

- Seq2Seq architecture using LSTM for language translation.
- Preprocessing of text data including tokenization and padding.
- Simple command-line interface for user input.
- Ability to expand and improve with larger datasets and advanced techniques.

## Installation

To run this project, you need to have Python installed on your machine. Follow the steps below to set up the environment:

1. Clone this repository:

   ```bash
   git clone https://github.com/ahmdmohamedd/Seq2Seq-language-translator.git
   cd Seq2Seq-language-translator
   ```

2. Install the required libraries:

   ```bash
   pip install tensorflow numpy pandas
   ```

## Dataset

For demonstration purposes, a small dataset containing English-French sentence pairs is provided. You can extend the dataset using larger datasets such as the Tatoeba or Multi30k datasets for better model performance. Ensure that the dataset is formatted correctly for the model.

## Usage

1. Open a Python interpreter or Jupyter Notebook.
2. Import the necessary libraries and load the model.
3. Use the `translate()` function to translate English sentences into French.

### Example

```python
# Example usage
user_input = input("Enter English text to translate: ")
print("Translated text:", translate(user_input))
```

## Training the Model

The model is trained using the following command. Adjust the parameters as needed based on your dataset and requirements.

```python
model.fit([input_train, target_train[:, :-1]], target_train[:, 1:], batch_size=64, epochs=100, validation_data=([input_test, target_test[:, :-1]], target_test[:, 1:]))
```

The model training process may take time depending on the dataset size and the computational resources available. Ensure to monitor the training loss and accuracy for performance evaluation.

## Inference

After training, you can use the `translate()` function to get translations for English sentences. The function preprocesses the input text, predicts the French translation, and returns it.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (e.g., `feature-branch`).
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Create a pull request.
