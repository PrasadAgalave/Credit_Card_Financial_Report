# Credit_Card_Financial_Report

Credit_Card_Transaction_Report and Credet_Card_Customer_Report Using Power Bi.

Project Objective : To develop a comprehensive credit 
                    card weekly dashboard that 
                    provides real-time insights into key 
                    performance metrics and trends, 
                    enabling stakeholders to monitor 
                    and analyze credit card operations 
                    effectively.

Overview YTD:
 • Overall revenue is 57M
 • Total interest is 8M
 • Total transaction amount is 46M
 • Male customers are contributing more in revenue 31M, female 26M
 • Blue & Silver credit card are contributing to 93% of overall 
transactions
 • TX, NY & CA is contributing to 68%
 • Overall Activation rate is 57.5%
 • Overall Delinquent rate is 6.06%

 
Dax Queries : AgeGroup = SWITCH(
                         TRUE(),
                        'public cust_detail'[customer_age] < 30, "20-30",
                        'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40, "30-40",
                        'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50, "40-50",
                        'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60, "50-60",
                        'public cust_detail'[customer_age] >= 60, "60+",
                        "unknown"
                         )
                                          
 IncomeGroup = SWITCH(
               TRUE(),
               'public cust_detail'[income] < 35000, "Low",
               'public cust_detail'[income] >= 35000 && 'public cust_detail'[income] <70000, "Med",
               'public cust_detail'[income] >= 70000, "High",
               "unknown"
               )
