# Books Recommendation System

## Project Motivation
The goal of this project is to develop a recommendation system for Arabic books available on Jamalon, an online bookstore. The objective is to suggest books to users based on attributes such as genre, price, and ratings, along with personal preferences. 

In **Phase 1**, we focused on understanding the problem, exploring the dataset, and performing initial data preprocessing. This included handling missing values, encoding categorical features, and visualizing the dataset to understand the relationships between key attributes.

## Dataset
We are using the **Jamalon Arabic Books Dataset**, sourced from [Kaggle - Jamalon Arabic Books Dataset](https://www.kaggle.com/datasets/dareenalharthi/jamalon-arabic-books-dataset?resource=download). The dataset contains detailed information about Arabic books available on Jamalon, including the following columns:

- **Unnamed: 0**: A placeholder column we ignore during analysis.
- **Title**: The title of the book.
- **Author**: The author of the book.
- **Description**: A brief description of the book.
- **Pages**: The number of pages in the book.
- **Publication year**: The year the book was published.
- **Publisher**: The publisher of the book.
- **Cover**: The type of the cover (e.g. hardcover, paper cover, etc.).
- **Category**: The primary genre of the book (e.g., Fiction, Non-Fiction, etc.).
- **Subcategory**: A more specific genre (e.g., Romance, Science, etc.).
- **Price**: The price of the book.


  
### 2. Preprocessing
The following preprocessing steps were performed on the dataset:
- **Handling Missing Values**: All missing values were dropped.
- **Categorical Encoding**: The `Category` and `Subcategory` columns, which are categorical, were encoded using **one-hot encoding** to allow the machine learning models to process them as numerical data.



### 3. Summary of the Dataset




The dataset exploration, preprocessing steps, and visualizations are documented in a Jupyter Notebook named `Dataset_Exploration_and_Preprocessing.ipynb`.
