# Banking Domain Project
# Banking Clients Analysis: EDA & Dashboard

### [Banking Domain Project.pdf](https://github.com/user-attachments/files/22645170/Banking.Domain.Project.pdf)


## 📖 Project Overview
This project analyzes a synthetic dataset of 3,000 bank clients to uncover patterns in customer demographics, financial behavior, and product holdings. The goal was to perform a thorough Exploratory Data Analysis (EDA) and build an interactive dashboard to provide actionable insights for the bank's management, helping in areas like client segmentation, risk assessment, and product strategy.

## 🎯 Business Objectives
- **Client Segmentation:** Understand different client groups based on income, loyalty, and banking products.
- **Risk Analysis:** Explore relationships between client attributes and risk weightings.
- **Product Analysis:** Identify patterns in the usage of credit cards, loans, deposits, and other financial products.
- **Wealth Management:** Analyze the distribution of assets like superannuation savings and properties owned.

## 📊 Dataset Description
The dataset (`Banking.csv`) contains **3,000 records and 25 columns**, including:
- **Demographics:** `Age`, `Nationality`, `Occupation`, `GenderId`
- **Financial Metrics:** `Estimated Income`, `Superannuation Savings`, `Credit Card Balance`, `Bank Loans`, `Bank Deposits`
- **Client Classifications:** `Loyalty Classification` (Jade, Silver, Gold, Platinum), `Fee Structure` (Low, Mid, High), `Risk Weighting`
- **Relationship Data:** `Banking Relationship (BRId)`, `Investment Advisor (IAId)`

## 🛠️ Tech Stack
- **Data Analysis & Visualization:** `Python`, `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`
- **Dashboarding:** `Tableau` / `Power BI` (Specify which one you used)
- **Environment:** Jupyter Notebook

## 📈 Exploratory Data Analysis (EDA) - Key Steps & Insights

### Data Overview & Cleaning
- Checked for missing values (none found) and data types.
- Converted `Joined Bank` to a proper datetime object.

### Univariate Analysis
- **Income Distribution:** Created an `Income Band` (Low, Med, High). Most clients fall into the 'Med' category.
- **Loyalty:** The majority of clients are classified as 'Jade'.
- **Credit Cards:** Most clients (1,922) have only 1 credit card.
- **Nationality:** The client base is predominantly European.

### Bivariate & Multivariate Analysis
- **Income vs. Products:** Clients with higher incomes tend to have higher bank deposits, checking accounts, and are more likely to use business lending.
- **Nationality Patterns:** European clients dominate across all banking relationships and product types.
- **Correlation Analysis:** Found strong positive correlations between:
  - `Bank Deposits` and `Saving Accounts`
  - `Checking Accounts` and `Saving Accounts`
  - `Estimated Income` and `Business Lending`

*For a detailed walkthrough of the analysis, see the [Jupyter Notebook](./notebooks/Banking_EDA.ipynb).*

## 📉 Interactive Dashboard

I developed a dynamic dashboard to visualize key metrics. The main features include:

- **Summary KPI Cards:** Total Clients, Total Deposits, Total Loans, Total Fees.
- **Filters:** Interactive filters for `Banking Relationship`, `Gender`, `Investment Advisor`, and `Joining Year`.
- **Visualizations:**
  - Breakdown of deposits and loans by nationality and income band.
  - Analysis of bank loans by occupation and risk profile.
  - Trends in client engagement over time.

**Dashboard Preview:**
![Dashboard Screenshot](./images/dashboard_screenshot.png) *(You should add a screenshot here)*

*View the interactive dashboard here: [Link to your Tableau Public/Power BI Service dashboard]*

## 🚀 How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/banking-clients-eda-dashboard.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd banking-clients-eda-dashboard
    ```
3.  **Install the required Python packages:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook notebooks/Banking_EDA.ipynb
    ```

## 📂 Repository Structure
banking-clients-eda-dashboard/
│
├── notebooks/
│ └── Banking_EDA.ipynb # Main Jupyter Notebook with full analysis
├── data/
│ └── Banking.csv # Dataset (add .gitignore if private)
├── images/
│ └── dashboard_screenshot.png # Screenshot for the README
├── dashboard/
│ └── Banking_Dashboard.twbx # Or .pbix file if using Power BI
├── requirements.txt # Python dependencies
└── README.md # This file
## 💡 Key Takeaways
- The bank's client base is diverse but with clear segments (e.g., high-income "Private Bank" clients vs. retail clients).
- Product usage is highly correlated, suggesting opportunities for cross-selling.
- The dashboard provides a powerful tool for non-technical stakeholders to explore the data and make data-driven decisions.

## 🔮 Future Work
- Build a predictive model to forecast client churn.
- Perform cohort analysis to understand client lifetime value.
- Integrate the dashboard with a live data source.
