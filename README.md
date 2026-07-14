# M_Faaiz_PROJECT_1_DECODELAB
# Data Cleaning & Preprocessing Pipeline

This project contains a Python-based data cleaning and preprocessing pipeline designed to handle e-commerce sales data. Using a Jupyter Notebook (Google Colab), the script cleanses, validates, and formats raw order data to make it ready for downstream data analytics or machine learning tasks.

## 🚀 Features & Data Cleaning Steps

The pipeline performs the following essential preprocessing tasks on the dataset:

1. **Initial Data Profiling**: Loads the dataset (`Dataset for Data Analytics.xlsx`) and reviews its structure, total rows, and columns.
2. **Handling Missing Values**: Identifies missing entries across all features and fills null values in the `CouponCode` column with a default value (`"No Coupon"`).
3. **Duplicate Detection**: Searches for completely duplicate rows and checks for duplicate `OrderID`s to ensure data uniqueness, retaining only the first occurrence.
4. **Data Formatting & Standardization**: 
   * Converts the `Date` column into a standardized datetime format.
   * Cleans text columns (strips leading/trailing spaces and standardizes data types).
5. **Data Integrity Validation**: Calculates expected total prices (`Quantity * UnitPrice`) and validates them against the actual `TotalPrice` column to detect any mathematical anomalies.
6. **Export**: Saves the sanitized, clean dataset as a new Excel file: `Cleaned_Dataset_Project_1.xlsx`.

## 📊 Dataset Structure (Raw vs. Clean)

The dataset contains **1,200 rows** and **14 columns**, covering key transaction features:
* **Identification**: `OrderID`, `CustomerID`, `TrackingNumber`
* **Temporal**: `Date`
* **Product Details**: `Product`, `Quantity`, `UnitPrice`
* **Transactional**: `PaymentMethod`, `OrderStatus`, `ItemsInCart`, `CouponCode`, `ReferralSource`, `TotalPrice`
* **Demographics**: `ShippingAddress`

## 🛠️ Requirements & Setup

### Prerequisites
Make sure you have Python installed along with the following libraries:
```bash
pip install pandas numpy openpyxl
