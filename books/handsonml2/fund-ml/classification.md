# 3. Classification

## Classification Metrics

Consider a binary classification problem, with 1 representing **positive**, and 0 representing **negative** class. A **true** (**false**) **positive** is an outcome where the model correctly (incorrectly) predicts the **positive** class. Similarly, a **true** (**false**) **negative** is an outcome where the model correctly (incorrectly) predicts the **negative** class.

**FP** (false positive) and **FN** (false negative) are often called **Type I Error** and **Type II Error**. We will get into details when we discuss **Confusion** **matrix** (a special type of **contingency table**).

{% hint style="info" %}
Note: I will mainly discuss binary classification problems as multi-class problems are generalizations of binary ones.
{% endhint %}

&#x20;While _binary_ classifiers distinguish between two classes, **multiclass** (also called **multinomial**) classifiers can distinguish between more than two classes. Some algorithms (such as _SGD_, _Random Forest_, and N_aive Bayes_ classifiers) are **capable** of handling multiple classes **natively**. Others (such as _Logistic Regression_ or _Support Vector Machine_ classifiers) are **strictly** _binary classifiers_. However, there are various strategies that you can use to perform multiclass classification with multiple binary classifiers. The two main approaches for multi-class classification problems that utilize binary classification are: **OvR** and **OvO**.

{% hint style="success" %}
* One vs Rest (**OvR**): It focuses on only **one** class at a time and the rest of the classes are called **other**. It is also called the one-versus-all (**OvA**) method.

**Example:** MNIST dataset(classes **0-9**): 0 - classifier, 1 - classifier, ..., 9 - classifier.
{% endhint %}

One way to create a system that can classify the digit images into 10 classes (from 0 to 9) is to train 10 binary classifiers (time complexity $$\sim \mathcal{O}(N)$$), one for each digit (a 0-detector, a 1-detector, a 2- detector, and so on). Then when you want to classify an image, you get the decision score from each classifier for that image and you select the class whose classifier outputs the **highest score.**

{% hint style="success" %}
* One vs One (**OvO**): Trains a binary classifier for every pair of classes, in total $$\dfrac{N × (N-1)}{2}$$ binary classification problems for N number of classes.

**Example:** MNIST dataset (classes **0-9):** 0 vs 1,..., 0 vs 9, 1 vs 2, ..., 1 vs 9, ... 8 vs 9
{% endhint %}

The main advantage of OvO is that each classifier will be trained only on the part of training set where two classes appear. So it is much **faster** and requires **less memory** than OvR, but the number of classifiers to be trained grows fast (time complexity $$\sim \mathcal{O}(N^2)$$). _Support vector machines,_ for example, scale **poorly** with _the size of the training_ set; hence, **OvO** is preferred and it is _faster_ and the training sets are _smaller_.

**Accuracy:** The most naive approach to measuring a model's performance in a binary classification problem is calculating the ratio of correct predictions, which is called **accuracy**.

&#x20;           $$\textbf{Accuracy} = \dfrac{\text{\# Correct Predictions}}{\text{\# \ \ Total \ \ Predictions}} = \dfrac{TP + TN}{TP+FP+TN+FN}$$&#x20;

{% hint style="danger" %}
**Caution:** Accuracy alone doesn't give enough information about the model's performance, as in **class-imbalanced** datasets, (such as in **anomaly detection** problems) there are significant disparity between the number of positive and negative labels. Consider a simple model that predicts all of the instances as normal, since the percentage of anomalies is much smaller than normal instances this naive model would yield a really high accuracy score, which is **misleading**.
{% endhint %}

{% hint style="danger" %}
**Example:** Consider a fraud detection (classification) problem, in which the percentage of fraudulent transactions is less than $$\leq 1\%$$ **,** then a _naive model_ predicting every transaction as **non-fraudulent** would yield an accuracy $$≥ 99 \%$$, which is overly optimistic for different datasets where the _data is more balanced_.
{% endhint %}

### Confusion Matrix

![Source: https://manisha-sirsat.blogspot.com/2019/04/confusion-matrix.html](../../../.gitbook/assets/confusionmatrix.jpg)

There are other metrics that are more useful for different types of problems, and more reliable than accuracy in general. Some of them are:

&#x20;                 $$\textbf{Precision} = \dfrac{TP}{TP + FP} \ \text{(PPV := Positive Predictive Value)}$$

&#x20;                   $$\quad \quad \quad \quad \quad \ \dfrac{TN}{TN + FN} \ \text{(NPV := Negative Predictive Value)}$$

&#x20;            $$\textbf{Recall (Sensitivity)} = \dfrac{TP}{TP + FN} \ \text{(TPR := True Positive Rate)}$$

&#x20;         $$\textbf{Specificity} = \dfrac{TN}{TN + FP} =1 - \dfrac{FP}{FP + TN} \ \text{(1 - False Positive Rate)}$$

Notice, similarly we can define $$\text{FPR (False Positive Rate)} = 1 - \textbf{Specificity}.$$These three metrics are very important as it is a common practice to visualize the scatter plot of **Precision** vs **Recall** and **TPR** (Recall, Sensitivity) vs **FPR** (1-Specificity), which is also called **ROC** (Receiver Operating Characteristic) curve, and calculating the area under the **ROC** curve, called **AUC**, in order to evaluate model's predictive power.

It is also often convenient to combine **precision** and **recall** into a single metric called the **F1-Score**, in particular, if you need a simple way to compare two classifiers. The F1-score is the _harmonic mean_ of _**precision**_ and _**recall**_. Whereas the regular mean treats _all values equally_, the harmonic mean gives _much more weight to low values_. As a result, the classifier will only get a **high** F1-score if _both recall_ and _precision_ are **high**.

$$\textbf{F1-Score} = \dfrac{2 * \text{Precision} * \text{Recall}}{\text{Precision} + \text{Precision}} = \dfrac{2}{\dfrac{1}{\text{Precision}} + \dfrac{1}{\text{Recall}}} = \textbf{HM(\text{P}, \text{R})}$$
