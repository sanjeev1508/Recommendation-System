# E-commerce Recommendation System

This project implements a real-time product recommendation system for an e-commerce platform using collaborative filtering techniques. The system recommends products to users based on their purchase history. The recommendation engine is built using **Truncated Singular Value Decomposition (SVD)** and **cosine similarity**.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Technologies Used](#technologies-used)
4. [Steps Involved](#steps-involved)
5. [Usage](#usage)
6. [Evaluation](#evaluation)
7. [License](#license)

## Project Overview

The goal of this project is to develop a recommendation system that provides personalized product recommendations to customers based on their previous purchase behavior. Collaborative filtering is used to identify similar users and predict product recommendations based on user similarity.

## Data Description

The dataset used in this project is sourced from Kaggle. The dataset contains the following columns:

- **Customer ID**: Unique identifier for each customer.
- **Age**: Age of the customer.
- **Gender**: Gender of the customer.
- **Item Purchased**: The name of the product purchased by the customer.
- **Category**: The category of the purchased product.
- **Purchase Amount (USD)**: The amount spent on the product.
- **Location**: The geographical location of the customer.
- **Size**: The size of the purchased product (e.g., Small, Medium, Large).
- **Color**: The color of the product.
- **Season**: The season in which the product was purchased (e.g., Winter, Summer).
- **Review Rating**: Customer rating for the product.
- **Subscription Status**: Whether the customer is subscribed to the platform.
- **Payment Method**: The method of payment used by the customer.
- **Shipping Type**: The shipping method selected by the customer.
- **Discount Applied**: Whether a discount was applied to the purchase.
- **Promo Code Used**: Whether a promo code was used during the purchase.
- **Previous Purchases**: The number of previous purchases made by the customer.
- **Preferred Payment Method**: The preferred method of payment for the customer.
- **Frequency of Purchases**: How often the customer makes a purchase.

## Technologies Used

- **Python**
- **Pandas**: For data manipulation and cleaning.
- **NumPy**: For numerical operations.
- **scikit-learn**: For implementing collaborative filtering and dimensionality reduction techniques.
- **Matplotlib**: For visualizing results (if required).
- **Jupyter Notebook**: For running and documenting the project.

## Steps Involved

1. **Data Preprocessing**: 
    - Data cleaning and selection of relevant features (`Customer ID`, `Item Purchased`, `Purchase Amount (USD)`).
    - Transformation of categorical data into numerical indices using `astype('category')`.

2. **Normalization**:
    - Normalization of the purchase amount to reduce skewness.

3. **User-Item Interaction Matrix**:
    - Creation of a user-item interaction matrix to represent customer purchases.

4. **Dimensionality Reduction**:
    - Use of **Truncated SVD** (Singular Value Decomposition) for dimensionality reduction, enabling the system to learn latent features in the user-item matrix.

5. **Collaborative Filtering**:
    - Implementation of collaborative filtering using **user similarity** based on the **Pearson correlation** between users' interactions.

6. **Recommendation Generation**:
    - Predict product ratings for users and generate product recommendations based on predicted ratings.

7. **Evaluation**:
    - Evaluation of the recommendation system using **Root Mean Squared Error (RMSE)** to assess prediction accuracy.

## Usage

1. **Clone the repository**:

    ```bash
    git clone https://github.com/your-username/ecommerce-recommendation-system.git
    cd ecommerce-recommendation-system
    ```

2. **Install dependencies**:

    Create a virtual environment and install required packages:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the code**:

    To run the recommendation system, execute the following script in a Jupyter Notebook or Python environment:

    ```python
    python recommendation_system.py
    ```

4. **Provide User Input**:

    After running the script, enter the user index when prompted to generate recommendations for a particular user. The system will return the top 5 recommended products for the user based on their purchase history.

## Evaluation

The recommendation system's performance is evaluated using **Root Mean Squared Error (RMSE)** and **Mean Squared Error (MSE)** to assess the accuracy of predicted ratings.

- **Mean Squared Error (MSE)**: A measure of how close the predicted ratings are to the actual ratings.
- **Root Mean Squared Error (RMSE)**: The square root of MSE, which gives a sense of the typical deviation between predicted and actual ratings.


