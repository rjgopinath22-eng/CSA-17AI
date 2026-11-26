# AI and Machine Learning Lab Programs (Experiments 32-41)

Titles, program links, representative output, and result for the ten requested experiments. Outputs for learned models may vary slightly across library versions, training runs, and environments. The TensorFlow MNIST program downloads its dataset on first run.

## Experiment 32 (CO2): WordPress Blog Demonstrating HTML Title and Anchor Tags

**Program:** [ex-32.html](ex-32.html)  
**Aim:** Demonstrate a blog page with a document title, headings, and anchor links for in-page navigation.

**Output:** A page titled “Learning Web Development | My Blog” displays the “My Learning Blog” heading, About and Articles navigation links, an article, and a “Return to the top” link. Selecting a navigation link jumps to its matching section.

**Result:** The sample blog demonstrates the HTML title element and working anchor navigation. To publish in WordPress, create a post, set its post title in the editor, and add the page body through a Custom HTML block; the document-level `<title>` is controlled by the theme/site metadata.

## Experiment 33 (CO4): Simple Linear Regression for Continuous Prediction

**Program:** [ex-33.py](ex-33.py)  
**Aim:** Fit a line to sample points using gradient descent and predict a continuous value.

**Representative output:**

```text
Model: y = 2.00x + 1.00
Prediction for x=5: 11.00
```

**Result:** Gradient descent recovers the linear relationship in the sample data and predicts 11 for x=5.

## Experiment 34 (CO5): K-Nearest Neighbors Classification

**Program:** [ex-34.py](ex-34.py)  
**Aim:** Classify a query point by majority vote among its three nearest labeled points.

**Output:**

```text
Predicted class: Blue
```

**Result:** The three nearest training points contain two Blue labels and one Red label, so the majority vote assigns Blue.

## Experiment 35 (CO3): Decision Tree Classification

**Program:** [ex-35.py](ex-35.py)  
**Aim:** Train a decision tree on a small AND-logic dataset and classify the input (1, 1).

**Output:**

```text
Predicted class: 1
```

**Result:** The trained tree predicts class 1 for (1, 1), matching the AND classification rule.

## Experiment 36 (CO3): TensorFlow Neural Network for MNIST Image Classification

**Program:** [ex-36.py](ex-36.py)  
**Aim:** Train a one-hidden-layer neural network to classify handwritten digit images.

**Output:** The program prints training progress, test accuracy, and the predicted digit for the first test image. The numeric accuracy and predicted digit are produced at runtime and can vary with TensorFlow version and training conditions; run the script to record the actual values.

**Result:** The neural network completes a one-epoch MNIST training run and evaluates digit classification on the test set. Record the measured test accuracy from your own run.

## Experiment 37 (CO3): Sentiment Analysis with TF-IDF and Naive Bayes

**Program:** [ex-37.py](ex-37.py)  
**Aim:** Classify a short review as positive or negative using TF-IDF features and a Naive Bayes classifier.

**Output:**

```text
Sentiment: Positive
```

**Result:** The model labels “excellent and enjoyable story” as Positive using the supplied labeled examples.

## Experiment 38 (CO4): Genetic Algorithm for Function Optimization

**Program:** [ex-38.py](ex-38.py)  
**Aim:** Maximize f(x) = -(x - 3)^2 + 9 with selection, crossover, mutation, and elitism.

**Output:** The program prints “Best x” and “Best fitness” to three decimal places. With the fixed random seed, the result is reproducible for the same Python implementation.

**Result:** The search approaches the function maximum at x=3, where the theoretical maximum fitness is 9. The printed best candidate is a discrete approximation because chromosomes encode a finite grid.

## Experiment 39 (CO4): Support Vector Machine Binary Classification

**Program:** [ex-39.py](ex-39.py)  
**Aim:** Train a linear SVM on two groups and classify a sample point.

**Output:**

```text
Predicted class: 0
```

**Result:** The linear SVM assigns the query point (2.5, 2.5) to class 0.

## Experiment 40 (CO4): Principal Component Analysis on the Iris Dataset

**Program:** [ex-40.py](ex-40.py)  
**Aim:** Standardize Iris features and reduce them to two principal components.

**Representative output:**

```text
Original shape: (150, 4)
Reduced shape: (150, 2)
Explained variance ratio: [0.73, 0.229]
```

**Result:** PCA maps the 150 four-feature samples to two components. Together, the first two components retain approximately 96% of the standardized data variance (exact rounded values may vary slightly by library version).

## Experiment 41 (CO5): User-Based Collaborative Filtering Recommendation

**Program:** [ex-41.py](ex-41.py)  
**Aim:** Estimate ratings for items not yet rated by a user using cosine similarity over shared ratings.

**Representative output:**

```text
Recommendations for Alice:
Book C: predicted rating 4.37
```

**Result:** Book C is the only unrated candidate for Alice and receives an estimated rating based on other users’ ratings weighted by similarity.

## Running the programs

Run a Python program from this directory with `python ex-33.py` (substitute the desired filename). Experiments 35, 37, 39, and 40 require scikit-learn. Experiment 36 requires TensorFlow and a network connection for the initial MNIST download. Experiment 32 is HTML and should be opened in a browser or added to a WordPress Custom HTML block.
