# 100-page-machine-learning-book

## Chapter 1

### 1.1 What is Machine Learning

-Building algorithms which rely on collections of examples of some phenomenon
- Process of solving a problem by:
  - Gathering a dataset
  - Building a statistical model based on that dataset
    - This model is used to solve the practical problem

## 1.2 Types of Learning

- Supervised, semi-supervised, unsupervised, and reinforcement

### 1.2.1 Supervised Learning

- Dataset is the collection of `labeled examples`
- In the below example, `square footage` and `number of bedrooms` are features
- Each row represents a `feature vector` and there is a value that represents the correct output
  - So for each row, we have feature values for square footage and number of bedrooms
    - Example, `[1500, 3]`

| House ID | Square Footage (sq ft) | Number of Bedrooms | Price ($) |
|----------|------------------------|--------------------|-----------|
| 1        | 1,500                  | 3                  | 300,000   |
| 2        | 2,000                  | 4                  | 400,000   |
| 3        | 1,700                  | 3                  | 350,000   |
| 4        | 2,200                  | 5                  | 450,000   |
| 5        | 1,200                  | 2                  | 250,000   |

- The goal of supervised learning is to use the training set to produce a model that takes a feature vector x as input and outputs a `label`
  - For example, the model created using the dataset of people could take as input a feature vector describing a person and output a probability that the person has cancer

### 1.2.2 Unsupervised Learning

- Dataset is a collection of `unlabeled examples`
- Still have a feature vector but there are no labels
- For example, in `clustering`, the model returns the id of the cluster for each feature vector in the dataset
- In `dimensionality reduction`, the output of the model is a feature vector that has fewer features that the original input `x`
- In `outlier detection`, the output is a real number that indicates how x is "different" from the typical example in the dataset

### 1.2.3 Semi-Supervised Learning

- Dataset contains both labeled and unlabeled examples
- Usually the quantity of unlabeled examples is much higher than the  number of labeled examples
- Goal is same as supervised learning
  - Hope here is that many unlabeled examples can help the learning algorithm to find a better model

### 1.2.4 Reinforcement Learning

- Subfield of machine learning where the machine "lives" in an environment and is capable of perceiving the *state* of that environment as vectors of features
- The machine can execute *actions* in every state
- Different actions bring different *rewards* and could also move the machine to another state of the environment
- **Goal of a reinforcement learning algorithm is to learn a policy**
  - A policy is a function (similar to model in supervised learning) that takes the feature vector as input and outputs an optimal action to execute in that state
  - Action is optimal if it maximizes the *expected average reward*
- Reinforcement learning solves a particular kind of problem where decision-making is sequential, and the goal is long-term
  - Examples are game playing, robotics, resource management, or logistics
- *This is out of the scope of this book*

### 1.3 How Supervised Learning Works

- Most frequently used in practice
- Process starts with gathering the data
  - Data for supervised learning is a collection of pairs `(input, output)`
    - Input could be anything - emails, pictures, sensor measurements, etc
      - Outputs are usually real numbers or labels (spam/not_spam, cat/dog/mouse/rabbit)
        - In some cases, outputs are vectors (4 coordinates of rectangle around person in photo), sequences (ex: [adjective, adjective, noun] for input "big beautiful car") or some other structure
- 

## Terminology

- A `label` is the output variable or target value that you want your model to predict in the training set - it is a part of the training data