---
title: Dimensionality Reduction
date: 2022-11-14
---

---------------------------------------------------------------------------------------------------------
## Minimalism: The Less is More Mentality

![minimalism]({{ "/assets/img/minimalism.jpg" |}})

On a planet with a radius of 3,958.8 mi, 7 continents and 8 billion people, there exists more information than we know what to do with.
As we know, data must be *conceptualized*, *measured* by humans and *interpreted* (preferably without bias). Just as we know that not all data is required for a good predication. Horsepower is a good indicator for the top speed of a sportsbike, less so for predicting the driver comfort of a sedan.

There's always been a fundamental perspective of *minimalism*. The idea that there exists more satisfaction with less. Whether this be with lifestyle, work/life balance, social media, etc. 

There's no surprise that this ideaology has morphed into a technical approach when it comes to data. *Occam's Razor* states that the less moving parts a model has, the better the general performance. Primarily this concerns the model. Choosing a simple model that fits the data well, will capture more key insights and features without too much noise. Simplicity for general performance. The question is, does this *less is more* approach apply to the data itself?

## Does this apply to data?
One may think naively that the more information a model possesses, the better it can make predictions. There is a kernel of truth to that statement. However on the other end, the more irrelevant features we have, the higher the degradation of performance. Termed the **"Curse of Dimensionality"**. 

![curse]({{ "/assets/img/curse.JPG" |}})

Essentially, the higher the number of features, the more sparse the observations become in that exponentially increasing space. This higher *sparsity* leads to loss of predictive power, and higher difficulty in interpreting or visualizing the information. 




Ideally, we want a dataset such that:
1. There are a high number of observations 
2. Is diverse and representative subset of the population 
3. Features that are as independent of each other as possible, or low *multi-colinearity*

Having too many features can lead to higher accountancy of variance, which suggests the model is overfitting to the noise of the training data. 

## What can we do? Dimensionality Reduction!
In fields with deal with high-dimensional data, **dimensionality reduction** is a necessary process to understand. Briefly, it is the process of reducing the features of a given dataset, with the features being the variables (or columns). It's a process to convert higher-dimensional data into a lower-dimensional space while *retaining key insights and original variance*. 

![globe]({{ "/assets/img/globe.JPG" |}})

**Advantages:**
- Lower training time, lower computational resources used
- Avoids over-fitting and removal of noise
- Easier data visualization
- Ability to obtain linearly separable data from non-linear data

**Disadvantages:**
- Some possible data loss
- Some methods will produce unknown synthetic features. 

## Common Techniques:

#### Feature Selection and Elimination: 

A specific case of dimensionality reduction that keeps the original feature values. 

- **Domain Knowledge**: Manually selecting top the k-th features of a dataset using domain knowledge. Perhaps the conceptualization and operalization of the features in the data are not aligned with the desired metrics someone with the field background would do. 
- **Filter Methods**: These are generic set of methods that do not require a specific model or algorithm and are usually applied beforehand. As such, they are much faster than wrapper methods, and less prone to over-fitting. 
    - E.g. correlation, ANOVA, etc.

- **Wrapper Methods**: Involves searching for well-performing subsets of features, evaluated on a specific model or algorithm. These methods have a higher computational time than filter methods and more prone to over-fitting. 
    - E.g Backwards Elimination, Forward Selection, etc. 

- **Intrinsic or Embedded Methods**: Implicitly selects features within the algorithms. 
    - E.g. Lasso, Ridge, decision trees, random forests, etc.

#### Feature Extraction: 

Mapping or projecting from high dimensional space to lower dimensional space (linear or non-linear). Involves a transformation of original data into more signifanct and/or synthetic variables. Generally falls into linear methods, and non-linear methods.

- **Linear Methods**: Involves projecting the data into a lower-dimensional space through linear transformation. 
    - E.g. PCA , SVD, etc. 

- **Non-Linear Methods (Manifold Learning)**: Involves projecting into a lower-dimensional space, searching for a non-linear fold. 
    - E.g. Kernel PCA, t-SNE, Isomap, etc.

## Key Take-Aways:
1. More data, does not mean better performance. In fact, excessive features generally degrade performance.
2. Seek quality features over the quantity of features.
3. Balance between coverage & sparcity. A complex model will require many predictors, and therefore many more observations. 
4. Avoid decision paralysis! Part of learning is applying new techniques and drawing conclusions from underlying patterns. Try one method, then another and compare!



























