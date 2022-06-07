# DATA ANALYSIS WITH R/PYTHON - FINAL PROJECT

## TOPIC: CUSTOMER SEGMENTATION BASED ON TRADITIONAL RFM, K-MEANS ALGORITHM AND GAUSSIAN: A CASE STUDY OF E-COMMERCE BRAZIL

Lecturer: Nguyen Phat Dat, MA

Group: Python

Member: 

| No. | Member                 | ID         | Role    | 
| --- | ---------------------- |:----------:|:-------:|
| 1   | Nguyen Hoang Anh Khoa  | K194111608 | Leader  | 
| 2   | Nguyen Thi Ngoc Anh    | K194111519 | Member  | 
| 3   | Nguyen Thanh Mong      | K194111613 | Member  | 
| 4   | Truong Nhat Hoang      | K194111608 | Member  | 
| 5   | Pham Thi Hong Nhung    | K194111620 | Member  | 

### Data used:

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

This is a Brazilian ecommerce public dataset of orders made at Olist Store. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers.

This is real commercial data, it has been anonymised, and references to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses.

### Introduction source code files:

- Languages: Python
- Number of files: 3
- Software used: Google Colab

During project implementation, we separate our source code into 3 different files, which are DataPreprocessing.ipynb, EDA.ipynb, BuildingModel.ipynb. 

Those files operate synchronously (running the lines of code in turn from top to bottom) and in the following order: 

1. DataPreprocessing.ipynb
2. EDA.ipynb
3. BuildingModel.ipynb. 

### Insight our code files:

**1/ DataPreprocessing.ipynb:**

*Things we did:*   
- Importing supported libraries
- Importing dataset
- Cleaning data
- Handling missing values
- Handling inconsistent data (both in types and values)
- Exporting data into new csv file with name: data_outlist_clean.csv

*How to import and run code:*
- Putting all csv files into a folder in Google Drive
- Mounting your Google Drive into our code file by using these code lines:

    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
- Changing raw_path string into your dataset folder path. For example, my folder path is '/content/drive/MyDrive/Tài liệu UPDRIVE/Data/' so I put it into raw_path variable and let the code below it import all the csv files.

    ```python
    raw_path = '/content/drive/MyDrive/Tài liệu UPDRIVE/Data/'
    olist_order = pd.read_csv(raw_path + 'olist_orders_dataset.csv')
    olist_item  = pd.read_csv(raw_path + 'olist_order_items_dataset.csv')
    olist_payment  = pd.read_csv(raw_path + 'olist_order_payments_dataset.csv')
    olist_product  = pd.read_csv(raw_path + 'olist_products_dataset.csv')
    olist_customer  = pd.read_csv(raw_path + 'olist_customers_dataset.csv')
    olist_review  = pd.read_csv(raw_path + 'olist_order_reviews_dataset.csv')
    olist_translate  = pd.read_csv(raw_path + 'product_category_name_translation.csv')
    ```

- In the end, we export a new csv file, which name is data_outlist_clean.csv. That file is saved on Google Colab after running this code line:

    ```python
    df_olist_clean.to_csv(raw_path + 'data_outlist_clean.csv', index = False, date_format = '%Y-%m-%d')
    ```
  make sure to download it because we will use data_outlist_clean.csv file for EDA.ipynb file. 

**2/ EDA.ipynb:**

*Things we did:*   
- Importing supported libraries
- Importing dataset
- Implementing exploratory data analysis for the dataset.

*How to import and run code:* In this file, we imported and used data_outlist_clean.csv file for analysis. To import this file, make sure to put it on Google Drive and input its path into raw_path variable. The way to do it is similar to the previous file, which is DataPreprocessing.ipynb

```python
from google.colab import drive
drive.mount('/content/drive')
raw_path = '/content/drive/MyDrive/Tài liệu UPDRIVE/Data/'
df = pd.read_csv(raw_path + 'data_outlist_clean.csv', parse_dates = ['order_purchase_timestamp'] )
```
**3/ BuildingModel.ipynb:**

*Things we did:*   
- Importing supported libraries
- Importing dataset
- Building RFM model using Traditional RFM method, Gaussian method and K-Means clustering.
- Visualizing all those models with scatter plot 3d, scatter plot and line plot and bar chart.

*How to import and run code:*
In this file, we imported and used data_outlist_clean.csv file for analysis. The steps included to import and run code is similar to the previous file, which is EDA.ipynb.

### [Link Google Drive Source Code](https://github.com/khoanguyn1411/OlistStoreDA-Python.git)
### [Link GitHub Source Code (for better view of README.md)](https://drive.google.com/drive/folders/1YIj5807YJTV78pPRjq6H-YduXWdWaJmz?usp=sharing) 

# THE END - THANK YOU FOR YOUR READING
