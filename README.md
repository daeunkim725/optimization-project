# optimization-project

# House Price Modeling
You are given data about houses and are tasked with building a model to predict the sell price of these houses. For the data, you have 545 total samples with 11 features:

| Feature          | Description |
| ---------------- | ----------- |
| area             | the area in 1000s of square feet                                  |
| bedrooms         |  the number of bedrooms                                           |
| bathrooms        | the number of bathrooms                                           |
| stories          | the number of stores                                              |
| mainroad         | 1 if the house is connected to the main road and 0 otherwise      |
| guestroom        | the number of guestrooms                                          |
| basement         | 1 if the house has a basement and 0 otherwise                     |
| airconditioning  | 1 if the house has centralized AC and 0 otherwise                 |
| parking          | the number of extra parking spaces                                |
| prefarea         | 1 if the house is located in a 'preferred area' and 0 otherwise   |
| furnished        | 1 if the house comes prefurnished and 0 otherwise                 |

The data also contains a price column, which is the sell price of the house in millions of USD.
For modeling purposes, we split the data into a training and testing set with an 80/20 split.

To model prices, you decide to build a linear model. That is, your goal is to determine a vector of weights $\theta$ to approximately fit: $y \approx X \theta$, where $X$ is the matrix of features and $y$ is the vector of prices. However, your cousin is a realtor and told you that all these features contribute positively to the price of the house. You trust your cousin and you are including this information by enforcing that **all weights in the vector $\theta$ are nonnegative**.

For this project, we will fit the linear model and handle the nonnegativity in a few different ways.

Run the following cells to import the data. Note that after importing the data and separating out $X$ and $y$, we prepend a column of ones to the feature matrices in order to learn an offset.
