# Customer Support Ticket Analysis

This project performs an in-depth analysis of customer support tickets to uncover key insights, identify trends, and provide data-driven recommendations for improving customer service.

## Project Overview

The primary goal of this analysis is to understand the main drivers of customer support inquiries. By leveraging Natural Language Processing (NLP) and data visualization, the project aims to:

-   Identify the most common types of support tickets.
-   Analyze the sentiment of customer complaints.
-   Determine which products generate the most support requests.
-   Extract key topics and keywords from ticket descriptions.
-   Provide actionable recommendations to enhance product quality and customer support efficiency.

## Project Structure

The repository is organized as follows:

```
.
├── Dashboard/
│   └── dashboard.png
├── Dataset/
│   ├── customerSupportTickets.csv  # Raw dataset
│   └── Output/
│       └── cleanedSupportTickets.csv # Processed and cleaned dataset
├── Notebook/
│   └── analysis.ipynb      # Jupyter Notebook with the full analysis
├── Report/
│   ├── CustomerSupportTicketAnalysisReport.pdf
│   └── task2Summary.txt
└── README.md
```

##  Dataset

The dataset used is `Dataset/customerSupportTickets.csv`, which contains information about support tickets, including customer details, product information, and ticket specifics.

##  Analysis & Key Findings

The core analysis is performed in the `Notebook/analysis.ipynb` Jupyter Notebook. The key steps include:

1.  **Data Cleaning**: Handling missing values, removing duplicates, and parsing date/time fields.
2.  **Text Preprocessing**: Cleaning ticket subjects and descriptions using NLP techniques like tokenization and stopword removal.
3.  **Exploratory Data Analysis (EDA)**:
    -   Distribution of ticket types, priorities, and statuses.
    -   Analysis of products with the most support tickets.
4.  **Text Analysis**:
    -   **TF-IDF Vectorization**: To identify the most significant keywords in ticket descriptions.
    -   **Sentiment Analysis**: Using `TextBlob` to gauge customer sentiment.
5.  **Visualization**: Generating a dashboard (`Dashboard/dashboard.png`) that visualizes:
    -   Top ticket types and products.
    -   Ticket status and customer sentiment distributions.
    -   A word cloud of common complaint terms.

Key insights and recommendations are automatically generated and saved in `Report/task2Summary.txt`.

##  How to Run

To reproduce the analysis, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd FUTURE_DS_02
    ```

2.  **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Jupyter Notebook:**
    Open and run the `Notebook/analysis.ipynb` notebook in a Jupyter environment. The notebook will automatically download necessary NLTK data.

### Dependencies

You can install the necessary libraries with pip:

```
pip install pandas numpy matplotlib seaborn nltk scikit-learn wordcloud textblob jupyter
```