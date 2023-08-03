# Models

## Evaluation Metrics for Imbalanced Classification Models

There are different evaluation metrics for our problem :

- Accuracy: The proportion of the total number of predictions that were correct.

- Precision (Positive Predictive Value): The proportion of positive cases that were correctly identified.
The higher the accuracy, the more the Machine Learning model minimizes the number of False Positives.
When accuracy is high, this means that the majority of the model's positive predictions are well-predicted positives.

- Sensitivity or Recall : The proportion of actual positive cases which are correctly identified.
The higher it is, the more the Machine Learning model maximizes the number of True Positives. When the recall is high, it means it won't miss any positives. However, this gives no indication of its predictive quality on negatives.

- F1 Score: The F1 score can be interpreted as a harmonic mean of the precision and recall, 
F1 Score = 2 * (precision * recall) / (precision + recall)

We our in a special case of imbalanced data, if we use the accuracy and the model overfit in a big family, the model will always predict the same family which will give a good accuracy. In this case, it is easy to get high accuracy without actually making usefull predictions. Accuracy as an evaluation metrics makes sense only if the class labels are uniformly distributed.

The confusion matrix presents all its elements in a single graphical representation, giving us an idea of the scores achieved. It is therefore a good tool for this task.

So, we've seen the different tools that can be used to score our model. However, we're in the middle of a special task, since we're dealing with data whose classes are not evenly distributed, and there are even extreme cases. We've just seen that in such cases, Accuracy is not a good measure for scoring the model. What's more, given that we're not in a medical or fraud detection context, we're not interested in certain classes more than others, so we're going to choose the macro-f1-score because it treats all the different types of sector equally.

## Baseline

In a machine learning project, a baseline model is essentially a simple model that serves as a reference. Its primary function is to contextualize trained model findings. Baseline models are often simple and have limited predictive value.

We will then use the multinomial naive bayes as a baseline, as it is the simplest model and will serve as a reference for the other models we will compare it to.

## Hyperparameter tunning 

Hyperparameters directly control model structure, function and performance. 

For example, if the value of a parameter is too high, the model may converge too quickly with sub-optimal results, and then an underfitting will occur. Conversely, if the value is too low, the training process will take a long time and results may overfit. There are three technics in order to tune the hyperparameters, we will only apply one :

- Grid search
With grid search, you specify a list of hyperparameters and performance measures, and the algorithm examines all possible combinations to determine the best match.

- Random search
Although based on the same principles as grid search, random search will randomly select groups of hyperparameters on each iteration.

- Bayesian optimization
Bayesian optimization is a technique based on the Bayesian theorem, which describes the probability of an event occurring based on current knowledge. When applied to hyperparameter optimization, the algorithm constructs a probabilistic model from a set of hyperparameters that optimizes a particular index.

We will then perform a manual search to understand how the different parameters work, and then set up a grid search.



## Cross-validation

In order to select the best algorithm and optimize its parameterization, we can use cross-validation. This method, also known as cross-validation, estimates the reliability of a model by randomly partitioning observations into groups of (approximately) equal size. In our case, it will proceed by making five divisions into two sub-samples. For each of these divisions, she will train the algorithm on the first sub-sample, the training set, then test it on the second, the test set. At the end of these five processes, it will obtain five scores that can be averaged.

The aim of this process is to avoid overfitting, i.e. to prevent the single division we make from misrepresenting our data, which would give a distorted result.

So, for each parameter to be tested, we apply this cross-validation, which will enable us to select them in a robust way.