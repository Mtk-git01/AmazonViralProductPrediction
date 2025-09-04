# Amazon Viral Product_Prediction Model
- Data Source: Amazon Keepa, External Factors
- All Keepa product data should be stored in your folder (e.g., ./data/raw_data/*.pkl)  
- Use "keepa_advanced_data_downloader.ipynb" to download product raw data from keepa using your API key, token
## Objective
- To build a prediction model for identifying future viral Amazon products using historical product raw data extracted via the Amazon Keepa API.
- Viral Definition: SalesRank growth rate < - 30% in 30 days
<img width="1998" height="1125" alt="image" src="https://github.com/user-attachments/assets/af63e396-bb64-4f82-9e86-13e94a8422dd" />

## Background  

The retail and e-commerce industries struggle to adapt to rapidly changing market trends, especially with the rise of viral products. Failure to anticipate surges in demand, sales velocity, or price fluctuations can lead to missed opportunities and lost market share.
## Solution  

This project develops a predictive model to identify products with viral potential over 30-, 60-, and 90-day periods, enabling retailers to proactively adjust inventory, pricing, and marketing strategies to maximize profits.  

## Market Forcus: Pet Products  

- Market Research (Data Source: Amazon Keepa)  
<img width="1177" height="805" alt="image" src="https://github.com/user-attachments/assets/9b3576fb-a190-4222-89e8-a1e82fa1361f" />

## Amazon Product Historical Data  

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/5faccafc-9b15-492a-be0a-1c3fc47b0507" />  
<img width="1642" height="925" alt="image" src="https://github.com/user-attachments/assets/36cfe822-b0d1-4b1f-9b13-b068af3943a7" />

## Process  
### Exploratory Analysis  
<img width="2000" height="1123" alt="image" src="https://github.com/user-attachments/assets/f97a8b10-056a-489e-9aaa-665e42ed3773" />  

### Advanced Techniques   
<img width="1998" height="1125" alt="image" src="https://github.com/user-attachments/assets/dfe43e89-722d-4481-a3bd-c04f30332b6c" />  

## Data Pipeline and Dataset
- Source: Keepa data for the last 3 years, comprising 500 ASINs and 470,000 records.
- Training Set: 378,531 records.
- Test Set: 94,633 records.
![image](https://github.com/user-attachments/assets/3201552c-fe93-465b-bb2a-b1052d2e92b9)

## Model Update Strategy  
### Model was refined in two stages based on the analysis and feature engineering
![image](https://github.com/user-attachments/assets/ee45955f-8611-4718-b317-1b8c1c559bc8)

### Phase 1: Base Line Models
<img width="1698" height="939" alt="image" src="https://github.com/user-attachments/assets/643c7058-6bbe-4414-b2e6-0902052d8b9d" />

### Phase 2: Model Result table 
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
## Model Usability: Baby Products
- Confirmed the model’s usability for other product categories as well, such as Baby Products.
![image](https://github.com/user-attachments/assets/d1247944-fe6f-424f-8e27-966c581076d4)

## Causal Analysis with Propensity Score Matching
- Causal Effect Estimation to "is_sns" flag.
<img width="1719" height="967" alt="image" src="https://github.com/user-attachments/assets/515678b7-23c6-4aae-b39e-17a8da4999d2" />

<img width="1708" height="957" alt="image" src="https://github.com/user-attachments/assets/6279477a-5405-4146-a4b2-f60977f19272" />

## User Interaction
<img width="1690" height="931" alt="image" src="https://github.com/user-attachments/assets/949e8c13-7a53-4e86-b9e2-42a42e1094d1" />

## Item-based Recommendation
- Addressing Cold-Start problem (New Users)
<img width="1683" height="934" alt="image" src="https://github.com/user-attachments/assets/b640f1dd-2435-486b-afe6-28f067077d3f" />

## Appendix: Market Research For Potential External Factors
- Number of Pet Stores, Temperature
<img width="1671" height="923" alt="image" src="https://github.com/user-attachments/assets/56e6342c-a789-4f71-a7ff-d061630fcaf6" />

- Streaming Affection on Gen-G
<img width="1690" height="940" alt="image" src="https://github.com/user-attachments/assets/f4f39ac1-cb35-4687-9e20-4f24f37b4b9a" />
