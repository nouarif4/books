# Books Recommendation System



## Project Motivation

The Arabic book market is a huge market with many readers worldwide. This poses a challenge of finding the right book to read especially since there are limited Arabic-specific recommendation systems available. The goal of this project is to help users discover their next read, based on their interests, preferences, and reading history by building an intelligent recommendation system utilizing the Jamalon Arabic Books Dataset.

students' names:
رغد المطيري |
شوق القريشي |
هيفاء السديري |
بتول الفوزان |
نوره العريفي |


## Dataset

The primary goal of using the Jamalon Arabic Books Dataset is to help us develop a robust, AI-driven, personalized recommendation system for Arabic books, enabling more efficient book categorization and enhancing overall user experience. By leveraging this dataset which includes rich metadata such as titles, authors, and genres, the system will provide personalized suggestions and explanations by integrating machine learning and generative AI, classify and categorize content efficiently, and process user inputs

The goal of this project is to develop a recommendation system for Arabic books available on Jamalon, an online bookstore. The objective is to suggest books to users based on attributes such as genre, price, and ratings, along with personal preferences. 

In **Phase 1**, we focused on understanding the problem, exploring the dataset, and performing initial data preprocessing. This included handling missing values, encoding categorical features, and visualizing the dataset to understand the relationships between key attributes.


We are using the **Jamalon Arabic Books Dataset**, sourced from [Kaggle - Jamalon Arabic Books Dataset](https://www.kaggle.com/datasets/dareenalharthi/jamalon-arabic-books-dataset?resource=download). 

In the Jamalon Arabic Books Dataset, each row represents a book. The dataset consists of 11 columns (variables) and approximately 8980 observations (books).  

Dataset Variables:
- Unique ID: A unique identifier for each book (*Numerical*).
- Title: The name of the book (*Text*).
- Author: The author's name (*Text*).
- Description: A brief description of the book (*Text*)
- Pages: The total number of pages in the book (*Numerical*)
- Publication Year: The year the book was published (*Numerical*)
- Publisher: The name of the publisher (*Categorical*).
- Cover: The cover type, such as *Paperback* or *Hardcover* (*Categorical*).
- Category: The main category of the book (e.g., *Literature*, *Islamic Books*) (*Categorical*).
- Subcategory: A more specific classification under each category (*Categorical*).
- Price: The price of the book (*Numerical*).

The Category and Subcategory columns act as classification labels, organizing books into different genres. These labels are useful for building the recommendation model based on user preferences.



### 2. Preprocessing Techniques 
The following preprocessing steps were performed on the dataset:
- **1- Handling Missing Values**: We checked for any null values in the dataset and deleted the rows containing them. Removing rows with missing data helps maintain data integrity and ensures that analysis and models are based on complete information.

- **2- Duplicate Detection and Removal**:We identified duplicate rows and applied a strategy 
Deduplication Strategy:
-For duplicates, the entry with the lowest non-zero price is kept.
-If prices are all zero, the most recent publication year is prioritized.
-If publication years are the same, the entry with the longest description is retained.
to retain the most relevant entry. Removing duplicates avoids data redundancy, improves data quality, and ensures accurate analysis.

- **3- Unnecessary Column Removal**: We removed columns like Unnamed: 0 and Cover as they were not needed for analysis. The Unnamed: 0 column was removed because it simply numbered the rows, which is unnecessary since the dataset already has automatic indexing. The Cover column was removed because it only indicated the type of book cover (e.g., paperback, hardcover, electronic), which was not relevant to our analysis.

- **4- Language Filtering**:We detected English titles using regular expressions (regex) and removed them from the dataset. Since the focus is on Arabic books, removing English titles ensures the dataset is relevant to the project’s objectives.

- **5- Category Mapping**:We mapped book categories to binary-like codes (e.g., "الأدب والخيال" → 0000000000001). This mapping standardizes categories, making them easier to process in machine learning models.

- **6- Encoding Categorical Features**:We applied Label Encoding to the Author, Publisher, and Subcategory columns to convert text data into numerical values. Machine learning models require numerical input; encoding categorical features ensures compatibility with these models.

- **7- Discretization**:We discretized the Pages column into bins (e.g., 0–50, 50–100, etc.) to categorize books based on page ranges. Discretization helps in analyzing trends across different ranges and simplifies complex numerical data.

- **8- Text Cleaning (Titles & Descriptions)**:We cleaned the text data by removing Arabic diacritics (Tashkeel), special characters, punctuation marks, and extra spaces. Cleaning text data improves consistency and quality, which is especially important for text analysis and natural language processing (NLP) tasks in phase 2.

### 3. Summary of the Dataset

#### Sample of the Dataset
![Screenshot from 2025-02-08 12-40-49](https://github.com/user-attachments/assets/5b235759-e3a4-4ead-9b04-b7b9567e686f)

#### Distribution of Numerical Variables
![image](https://github.com/user-attachments/assets/439e7cc1-e348-4f46-8509-4f197fde12e9)

#### Missing values
![Screenshot from 2025-02-08 13-35-10](https://github.com/user-attachments/assets/7f7e0768-3356-438a-b9af-9c3e4fa6520a)
![Screenshot from 2025-02-08 13-34-54](https://github.com/user-attachments/assets/26fd3476-cf49-453b-a51a-9bd00c5e9bc1)

#### Count, Mean, Standard, Minimum, Maximum, and Variance
![image](https://github.com/user-attachments/assets/4dbe106b-2c6c-43b2-9ed0-68d64e9cf1cb)



