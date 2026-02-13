# ALGEBRA PROJECT: Book Analysis & Recommendation System 📚

This project implements a **Book Recommendation System** using Linear Algebra techniques, specifically **Singular Value Decomposition (SVD)**. The system analyzes user preferences to predict book ratings and suggest titles based on geometric similarity in a latent factor space.

## 👥 Authors
* **Biel Fernandez Herencia**
* **Izan Perez Sanchez**
* **Edgar Saez Lopez**

## 🚀 Project Overview
The system utilizes the **"goodbooks-10k"** dataset. Due to technical issues with the original movie dataset, this project successfully adapts the recommendation logic to a library of 10,000 books and 6 million ratings.

### Key Features:
* **Collaborative Filtering:** Predicting user interest based on the behavior of the community.
* **Noise Reduction:** SVD is used to filter out random rating variations (noise), capturing only the "signal" or main structure of the database.
* **Geometric Recommendations:** * **User-based:** Suggests the 3 closest unread books using Euclidean distance.
  * **Item-based:** Finds books that are geometrically similar to a specific title.
* **Visualization:** Includes interactive plotting of the reduced matrix to see how books and users cluster together.



## 📈 Mathematical Foundation: SVD
The core of this project is the decomposition of the utility matrix $A$ into three matrices:
1.  **U (User-Concept):** Represents how much users relate to specific latent themes (genres).
2.  **Σ (Strength):** Diagonal matrix containing singular values that indicate the importance of each theme.
3.  **Vᵀ (Book-Concept):** Represents how much books relate to those same latent themes.

By reducing the dimensionality (low-rank approximation), we can represent complex human tastes in a simplified 2D or 3D geometric space.

## 💻 Execution & Setup
This project is designed to be **self-contained**. No manual file downloads or external environment configurations are required.

1.  **Dependencies:** The first cells in the notebook automatically handle the installation of all required libraries:
    * `kagglehub` (for data fetching)
    * `pandas` & `numpy` (for data processing)
    * `matplotlib` & `plotly` (for visualization)
2.  **Data Acquisition:** The notebook uses the `kagglehub` API to fetch the "goodbooks-10k" dataset directly into your environment.
3.  **Workflow:** Simply open `book_recommendation.ipynb` and **Run All Cells**. The notebook will:
    * Check and install missing dependencies.
    * Download and load the CSV files.
    * Process the matrix and compute the SVD.
    * Display the interactive recommendation engine and plots.

---
