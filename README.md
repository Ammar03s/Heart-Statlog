# Heart Disease Analysis Repository

## Table of Contents
- [Dataset](#Dataset)
- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Data Visualization](#data-visualization)
  - [Key Visualizations and Insights](#key-visualizations-and-insights)
- [MLP and CNN Models](#mlp-and-cnn-models)
  - [Results](#results)
- [Optimization Techniques](#optimization-techniques)
  - [Results](#optimization-results)
- [Swarm Optimization](#swarm-optimization)
  - [Results](#swarm-results)
- [Conclusion](#conclusion)
- [Accuracy Summary](#accuracy-summary)

##Dataset
https://www.kaggle.com/datasets/mexwell/heart-disease-dataset

## Project Overview

This repository contains a comprehensive analysis and machine learning modeling and some optimization algorithms for a heart disease dataset. The project is divided into several parts:
1. **Data Visualization**: Exploratory data analysis and visualization to understand our dataset.
2. **MLP and CNN Models**: Implementation and comparison of Multi-Layer Perceptron (MLP) and Convolutional Neural Network (CNN) models.
3. **Optimization Techniques**: Application of various optimization algorithms: Genetic Algorithm (GA), Simulated Annealing (SA), Gradient Descent (GD), and Hill Climbing to improve the models.
4. **Swarm Optimization**: Utilizing Swarm Optimization to update the weights of a neural network with one hidden layer.

## Repository Structure

- `Visualizing_Dataset.ipynb`: Contains code for data visualization and exploratory analysis.
- `Mlp_vs_Cnn.ipynb`: Implementation and comparison of MLP and CNN models.
- `neural_network_weight_optimization.ipynb`: Various optimization techniques applied to neural network models.
- `swarm_optimization.ipynb`: Swarm Optimization for neural network weight updates (not included).

## Data Visualization

The dataset used in this analysis is the heart disease dataset which includes various features such as age, sex, chest pain type, resting blood pressure, cholesterol, and more.

### Key Visualizations and Insights

- **Target Distribution**: Distribution of the target variable indicating the presence of heart disease.
- **Age vs. Max Heart Rate**: Scatter plot showing the relationship between age and maximum heart rate, colored by the presence of heart disease.
- **Correlation Heatmap**: Heatmap revealing correlations between different features.
- **Sex and Heart Disease**: Comparison of heart disease prevalence between males and females.

## MLP and CNN Models

We implemented and compared the performance of MLP and CNN models on the heart disease dataset. and found out that even that the MLP got slightly higher accuracy but its not actually better because when we check the graph in the end of the notebook we can see that the validation and the training got a gap between them which means its overfitting therfefore CNN is better

## Optimization Techniques

Various optimization techniques were applied to improve the neural network models:

- **Genetic Algorithm (GA)**
- **Simulated Annealing (SA)**
- **Gradient Descent (GD)**
- **Hill Climbing**

### Optimization Results

The optimization shows that Gradient Descent (GD) and Randomized Hill Climbing (RHC) performs almost the same with high accuracy and balanced specificity and sensitivity. While in Simulated annealing (SA) got the highest sensitivity, indicating its ability to correctly identify the positive cases, which is important for applications where false negatives are costly. However, Simulated annealing 's (SA) specificity is slightly lower, suggesting a higher rate of false positives. On the other hand, we got Genetic Algorithm (GA) shows the poorest and worst performance among all with low accuracy and sensitivity, despite its high specificity, indicating it is better at identifying true negatives but fails to capture the true positives effectively even the AUC for it is considered as low. Keep in mind that GD, SA, and RHC all show reasonably high AUC %, which demonstrates their effectiveness in distinguishing between the classes.
Overall, while GD and RHC are considered both good choices for our application, GA is the least effective one, especially in tasks requiring high sensitivity like our heart dataset which makes it unsuitable for us. Which takes us to SA, which stands out to be the best Algorithm we got out of all of them for our application.


## Swarm Optimization

Swarm Optimization was used to update the weights of a neural network with one hidden layer. This approach aimed to find the optimal weights that minimize the error in predictions.
In this file we’ll be training a neural network using particle swarm optimization and For this we’ll be using the standard pyswarms. for optimizing the network’s weights and biases. This aims to demonstrate how the API is capable of handling custom-defined functions. we will be trying to classify the 3 iris species in the Iris Dataset.

## Conclusion

This project demonstrates the effectiveness of various machine learning models and optimization techniques in predicting heart disease. The use of data visualization helped in understanding our dataset better, and the optimization techniques significantly improved our model performance.



## Accuracy Summary

| Model/Technique              | Accuracy |
|------------------------------|----------|
| MLP Model                    | 90%      |
| CNN Model                    | 89%      |
| Genetic Algorithm (GA)       | 89%      |
| Simulated Annealing (SA)     | 88%      |
| Gradient Descent (GD)        | 88%      |
| Hill Climbing                | 87%      |
| Swarm Optimization           | 91%      |