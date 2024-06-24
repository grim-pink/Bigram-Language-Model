# Bigram Language Model with Emotion-Oriented Text Generation

## Overview

This project involves creating a Bigram Language Model (BigramLM) from scratch, implementing smoothing techniques, and generating emotion-oriented text samples.

## Features

1. **Bigram Language Model**:
    - Developed a `BigramLM` class with methods for learning the bigram model from a dataset and calculating probabilities.

2. **Smoothing Algorithms**:
    - Implemented Laplace and Kneser-Ney smoothing within the `BigramLM` class.
    - Compared and analyzed the probabilities from both techniques.

3. **Emotion-Oriented Text Generation**:
    - Used the `emotion_scores()` function from `utils.py` to obtain emotion scores for sentences.
    - Modified the bigram probability to include an emotion component, β:

       \[
      P(w_i \mid w_{i-1}) = \frac{\text{count}(w_i, w_{i-1})}{\text{count}(w_{i-1})} + \beta
      \]
      
4. **Extrinsic Evaluation**:
    - Generated 50 samples for each of the 6 emotions and saved them in `.txt` files.
    - Trained an SVC model using the original corpus as training data and generated samples as testing data.
    - Used the TF-IDF vectorizer and Grid Search for parameter optimization.

