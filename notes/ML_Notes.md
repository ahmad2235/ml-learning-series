# Machine Learning Notes

## What is Machine Learning (ML)?

ML offers new ways to solve problems, answer complex questions, create new content, and create **never-seen-before** images.

- To predict the weather, we give an ML model an enormous amount of data until it learns the mathematical relationship between weather patterns → then it predicts the weather.
- A supervised ML model can find connections in data that a human cannot.
- An ML model can evolve, giving better predictions.

## Types of ML Systems

- **Supervised learning** (sees correct data) → Regression, Classification
- **Unsupervised learning**
- **Reinforcement learning**
- **Generative AI**

### Supervised Learning

Finds connections in data that produce correct answers.

- **Regression model:** predicts numeric values (continuous).
- **Classification:** predicts the likelihood that something belongs to a category.
  - **Binary:** output is one of two values.
  - **Multiclass:** output is one of more than two values.

### Unsupervised Learning

Aims to identify meaningful patterns in a dataset (grouping the data).

- **Example:** the clustering method organizes similar data into groups called "clusters".

#### Why isn't clustering classification?

- Because the categories aren't defined by you.
- Classification needs labels you already know. Clustering doesn't (groups nobody defined beforehand).

### Reinforcement Learning

Rewards good actions and penalizes bad ones until the model learns a strategy (policy) that maximizes reward.

### Generative AI

Creates content from input. It can take a variety of inputs and generate a variety of outputs, like text-to-text, text-to-image, image-to-image...

- Produces **new but similar** data.
- Initially trained using an unsupervised approach, sometimes trained further using supervised or reinforcement learning.

## Supervised ML Is Based On

Data, Model, Training, Evaluating, Inference.

## Datasets

A dataset is made of **examples** that contain **features** and a **label**.

- **Example:** a single row in a spreadsheet.
- **Features:** the values a supervised model uses to predict the label.
- **Label:** the value we want the model to predict ("the answer").
- **Labeled examples:** examples that contain both features and a label.
- **Unlabeled examples:** the model predicts the label from the features after it's created.

### Dataset Characteristics

A dataset is characterized by its **size** and **diversity**. If both are high, the dataset is good.

- **Size:** the number of examples.
- **Diversity:** the range these examples cover.
- Also: the number of features (not always useful).

**Good dataset** = a large number of examples that cover a variety of use cases, sometimes with more features.

## Model

**Model (supervised):** a set of numbers that captures how input features relate to output labels, learned through training.

## Training

**Training:** the process of repeatedly making predictions on labeled examples, measuring how far they are from the real label (the loss), and adjusting the model's parameters until that loss is as small as possible.

- Training stops when the loss stops improving.
- **Loss:** how wrong you are.
- **Weight:** how much an input matters.
- **Epoch:** one pass through the whole dataset. Training often runs many epochs.

### Gradient Descent

If training is: show examples, predict, compute loss, [update parameters], repeat until the loss is small, then gradient descent is the specific rule for the [update parameters] step.

- "Move each parameter a small step in the direction that lowers the loss."

### Bias, Learning Rate, and Parameters

- **Bias:** whatever value makes the predictions fit best.
- **Learning rate:** how big a step the model takes each time it updates the weight and bias (usually you set it yourself, not the model through training).

```
Prediction = weight * feature + bias
```

- **Parameters:** start random, and the model learns them through training (from the loss). Examples: weight, bias...
- **Hyperparameters:** you set them before training, and the model doesn't change them. Examples: learning rate, number of epochs, batch size...

The model's configurations and features can be edited during training → Evaluating.

## Evaluating and Testing

The dataset is divided into: Training, Evaluating, Testing.

| Training | Evaluating | Testing |
|---|---|---|
| The model learns from it and sees labels | Checks progress and guides changes | Gives the final score |
| Updates parameters automatically | Doesn't see labels, just compares predictions to them | Doesn't see labels, just compares predictions |
| Used many times, each epoch | Doesn't update parameters | Used only once, at the end |
| | Used to adjust settings | |
| | Used after each run | |

### What if the predictions are bad after testing?

- → We accept the result and report it as it is.
- → We find new data for testing, then go back and improve the model.

## Inference

**Inference:** putting the finished model to work. New data, no labels, let it predict.
