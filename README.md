# Amazon Viral Product_Prediction Model
- All Keepa product data should be stored in your folder (e.g., ./data/raw_data/*.pkl)  
- Use "keepa_advanced_data_downloader.ipynb" to download product raw data from keepa using your API key, token
## Viral Definition: SalesRank growth rate < - 30% in 30 days
![image](https://github.com/user-attachments/assets/c740b666-e95d-4c74-835a-142b32da2314)
## Data Pipeline and Dataset
- Sample Product Category: Pet Products
![image](https://github.com/user-attachments/assets/3201552c-fe93-465b-bb2a-b1052d2e92b9)
## Model Update Strategy
- Model was refined in two stages based on the analysis and feature engineering
![image](https://github.com/user-attachments/assets/ee45955f-8611-4718-b317-1b8c1c559bc8)
- 2nd phase Model Result table 
![image](https://github.com/user-attachments/assets/f0651f63-943c-48bd-83e1-98d316097f18)
## Model Selection Definition and Final Model 
- Final Model: XGBoost
![image](https://github.com/user-attachments/assets/da103a71-fd34-4755-8d06-d9ae4db1312c)
## Monetary Calculation and Confusion Matrix
- Since amazon doesn't show actual sales unit, used a formula from prior research to estimate Weekly sales unit based on SalesRank  
*Since this formula works best for mid-rank products around SalesRank:1000, used detected products ranked between 500 and 1500
![image](https://github.com/user-attachments/assets/2fc0845c-ba55-46d8-b3ca-63aa481770aa)
## Conclusion
- If we assume profit is 10% of sales, we can expect an additional $4,400 in profit per week.
## Model Usability
- Confirmed the model’s usability for other product categories as well, such as Baby Products.
![image](https://github.com/user-attachments/assets/d1247944-fe6f-424f-8e27-966c581076d4)



