## **SmartBasket: Market Basket Analysis with Snowflake, Alteryx, and Streamlit**

### **Project Overview**
This project demonstrates an end-to-end Market Basket Analysis pipeline using modern data tools including **Snowflake**, **Alteryx**, and **Streamlit**, with a focus on real-time product recommendation and association rule mining.  
The goal is to leverage transactional grocery data to identify product pairings, improve basket size, and deliver personalized product suggestions through an interactive web application.

---

### **Project Components**

1. **Flyer (Project Overview)**  
   A concise, visually engaging project flyer that highlights:
   - The problem statement and business value
   - Tools and technologies used (Snowflake, Alteryx, Streamlit)
   - Key takeaways from the analysis and modeling process

2. **Instacart Streamlit Application (`instacart.py`)**  
   - Fully interactive product recommendation app developed using **Streamlit**.
   - Allows users to input products and view recommended pairings based on association rules.
   - Powered by the market basket analysis results generated through Alteryx workflows.
   - Designed for easy deployment on the web for stakeholder access.

3. **Demo Video**  
   - Walkthrough of the project pipeline.
   - Demonstrates the application in action.
   - Explains the business use-case, data flow, and key results.

4. **End-to-End Pipeline (Snowflake → Alteryx → Streamlit)**  
   - **Data Storage:** Grocery transaction data is stored and accessed through **Snowflake**.
   - **Data Preprocessing and Modeling:**  
     Alteryx workflows handle:
     - Data extraction from Snowflake
     - Preprocessing and cleaning
     - Market Basket Analysis (Association Rules: Support, Confidence, Lift)
     - Product mapping and rule generation
   - **Data Utilization in Streamlit App:**  
     The same output data (association rules) from Alteryx is fed into the Streamlit app to provide product recommendations dynamically.

---

### **Alteryx Workflow File**
- Contains the full data preparation, modeling, and product mapping logic.
- Organized into **separate containers** for:
  - Data extraction (via Snowflake connection)
  - Data cleaning and preprocessing
  - Market Basket modeling
  - Result generation and export for the Streamlit application.
- Modular design for easy updates or scale-up to larger datasets.

---

### **How to Run the Project**
1. **Snowflake Setup:**
   - Store your transaction data in Snowflake.
     Data link: https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis
   - Configure Alteryx In-DB tools with appropriate credentials.
   - (Alternatively download files from kaggle and then read it directly on alteryx if you don't want to create connection with snowflake).

2. **Alteryx Workflow Execution:**
   - Run the Alteryx workflow to preprocess data and generate association rules.
   - Export the final results (CSV / Parquet) for use in the Streamlit app.

3. **Streamlit Application:**
   - Use `instacart.py` to run the Streamlit app:
     ```bash
     streamlit run instacart.py
     ```
   - Ensure the data file generated from Alteryx is available in the app’s expected path.

---

### **Key Tools and Technologies**
| Tool          | Purpose                                 |
|---------------|-----------------------------------------|
| **Snowflake** | Cloud-based data warehousing & storage  |
| **Alteryx**   | Data preprocessing, Market Basket Analysis (Apriori), product mapping |
| **Streamlit** | Web-based interactive product recommendation application |
| **Python**    | Fuzzy matching, data handling, and recommendation logic |

---

### **Additional Notes**
- The project focuses on **recommendation insights for grocery products** using association rule mining.
- Ensures scalability by leveraging Snowflake’s cloud architecture.
- Supports flexible data updates without needing major changes in the Streamlit application.
