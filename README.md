# Credit_Card_Financial_Report

Credit_Card_Transaction_Report and Credet_Card_Customer_Report Using Power Bi.

Project Objective : To develop a comprehensive credit 
                    card weekly dashboard that 
                    provides real-time insights into key 
                    performance metrics and trends, 
                    enabling stakeholders to monitor 
                    and analyze credit card operations 
                    effectively.


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
