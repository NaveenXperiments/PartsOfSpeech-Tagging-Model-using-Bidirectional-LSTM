# Parts of Speech (POS) Tagging Model using Bidirectional LSTM

This repository contains code for a Parts of Speech (POS) Tagging model built using a Bidirectional Long Short-Term Memory (BiLSTM) network with TensorFlow. This model tags each word in a sentence with its corresponding part of speech, such as noun, verb, adjective, etc. The BiLSTM model leverages both past and future context for enhanced POS tagging accuracy.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Requirements](#requirements)
- [Installation](#installation)
- [Code Structure](#code-structure)
- [Training the Model](#training-the-model)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview
Parts of Speech tagging is a crucial task in Natural Language Processing (NLP). It labels each word in a sentence with its part of speech, making it useful for various downstream applications like Named Entity Recognition and Syntactic Parsing. This project demonstrates a POS tagging model using a Bidirectional LSTM network.

## Dataset
The dataset for this project is a set of sample sentences with their POS tags. For more robust training, you can replace this with a larger annotated dataset. 

### Example Data:
- **Sentence:** "I am learning TensorFlow"
- **Tags:** "PRON AUX VERB PROPN"

## Model Architecture
The POS Tagging model uses the following layers:
1. **Embedding Layer**: Converts words to dense vector representations.
2. **Bidirectional LSTM Layer**: Captures dependencies from both past and future context in the sentence.
3. **TimeDistributed Dense Layer**: Outputs probabilities for each POS tag for each word in the sentence using softmax.

## Requirements
- Python 3.x
- TensorFlow 2.x
- NumPy

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/POS-Tagging-BiLSTM.git
    ```
2. Navigate to the project directory:
    ```bash
    cd POS-Tagging-BiLSTM
    ```
3. Install dependencies:
    ```bash
    pip install tensorflow numpy
    ```

## Code Structure
- `pos_tagging_bilstm.py`: Contains the main code for data preprocessing, model creation, training, and evaluation.
- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies for easy installation.

## Training the Model
To train the model, run `pos_tagging_bilstm.py` which performs the following steps:
- Tokenizes and pads the input sentences and POS tags.
- Defines a BiLSTM model and trains it on the sample sentences.
  
Run the code:
```bash
python pos_tagging_bilstm.py
