# Books Recommendation System



1. Information About the Project

## Project Motivation

The Arabic book market is a huge market with many readers worldwide. This poses a challenge of finding the right book to read especially since there are limited Arabic-specific recommendation systems available. The goal of this project is to help users discover their next read, based on their interests, preferences, and reading history by building an intelligent recommendation system utilizing the Jamalon Arabic Books Dataset.



2. The Dataset

The primary goal of using the Jamalon Arabic Books Dataset is to help us develop a robust, AI-driven, personalized recommendation system for Arabic books, enabling more efficient book categorization and enhancing overall user experience. By leveraging this dataset which includes rich metadata such as titles, authors, and genres, the system will provide personalized suggestions, classify and categorize content efficiently, and process user inputs.

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

  
##General Information
Number of Observations (Rows)

•	Before Cleaning: 8,950 rows

•	After Cleaning: 3,517 rows

Number of Variables (Columns)

•	Before Cleaning: 9 Columns

•	After Cleaning: 3 Columns

 Remaining Columns (After Cleaning)

1️⃣ Title – The title of the book.

2️⃣ Author – The name of the book’s author.

3️⃣ Description – A short summary or description of the book.

Removed Columns (During Cleaning Process)

The following six columns were removed to streamline the dataset:
    

-Number of Pages – Removed due to inconsistency or limited impact on recommendation quality.

-Publication Year – Removed as it was deemed less relevant.

-Publisher – Excluded to simplify analysis.

 -Cover – Not essential for book recommendations.
 
-Category – Removed to focus on personalized recommendations rather than static classifications.

-Subcategory – Removed for the same reason.

  
### 2. Preprocessing
The following preprocessing steps were performed on the dataset:
- **Handling Missing Values**: All missing values were dropped.
- **Categorical Encoding**: The `Category` and `Subcategory` columns, which are categorical, were encoded using **one-hot encoding** to allow the machine learning models to process them as numerical data.



### 3. Summary of the Dataset

#### Sample of the Dataset
![Screenshot from 2025-02-08 12-40-49](https://github.com/user-attachments/assets/5b235759-e3a4-4ead-9b04-b7b9567e686f)


#### Missing value and percentage
![Screenshot from 2025-02-08 13-35-10](https://github.com/user-attachments/assets/7f7e0768-3356-438a-b9af-9c3e4fa6520a)
![Screenshot from 2025-02-08 13-34-54](https://github.com/user-attachments/assets/26fd3476-cf49-453b-a51a-9bd00c5e9bc1)

#### Count, Mean, Standard, Minimum, Maximum, and Variance
![Screenshot from 2025-02-08 13-34-12](https://github.com/user-attachments/assets/c72ab4c3-f61c-4c04-bc4b-1044cd5ac8ba)


The dataset exploration, preprocessing steps, and visualizations are documented in a Jupyter Notebook named `Dataset_Exploration_and_Preprocessing.ipynb`.
