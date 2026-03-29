# MerchantFloat-AI

AI powered credit scoring and loan recommendation system for SMEs using POS transaction data.

Overview

MerchantFloat AI is a data driven scoring system that evaluates the financial health of merchants based on transaction behavior. It transforms raw POS data into actionable insights, including credit scores, risk classification and loan recommendations in real time. 

Problem

Many small and medium sized enterprises(SMEs) struggle to access credit due to:
	•	Lack of formal credit history
	•	Heavy reliance on collateral
	•	Manual and inefficient risk assessment processes.

 Solution
 
MerchantFloat AI leverages transaction level data to:
	•	Generate credit scores (300–850 scale)
	•	Classify merchants into risk levels(Low, Medium, High)
	•	Recommend loan amounts dynamically
	•	Provide explainable, data driven insights
  
Features

	•	AI-powered credit scoring engine
	•	Risk classification system
	•   Loan recommendation logic
	•	Merchant behavioral analysis
	•	Explainable insights for decision making
	
Technical Approach

Feature Engineering

Transaction data is aggregated into merchant level metrics such as
    •	Average revenue
	•	Revenue volatility
	•	Customer retention rate
	•	Settlement delays
	•	Transaction activity

Machine Learning

	•	K-Means clustering for behavioral segmentation
	•	StandardScaler for normalization
	•	Hybrid approach combining ML + rule-based scoring

Scoring System

	•	Weighted scoring model based on:
	•	Revenue strength
	•	Consistency
	•	Customer loyalty
	•	Transaction volume
	•	Output normalized to a 300–850 credit score range

System Architecture

Transaction Data → Backend (Bun.js) → FastAPI (AI Engine) → Scoring Output → Frontend Dashboard


Tech Stack

	•	Python (FastAPI)
	•	Scikit-learn (K-Means Clustering)
	•	Pandas / NumPy
	•	REST API
	
   System Architecture

Transaction Data → Backend (Bun.js) → FastAPI (AI Engine) → Scoring Output → Frontend Dashboard

API Endpoints

Method       Endpoint                          Description
GET          /analyze                        Get all merchants
GET          /analyze/{merchant_id}          Get single merchant
POST         /analyze                        Analyze transaction data

Sample request

{"transaction":[
{"merchant_id": "M_TEST",
"transaction_date": "2025-01-01",
"daily_revenue": 80000,
"transaction_count": 18,
"refund_count": 1,
"avg_settlement_delay_hours": 12,
"returning_customer_ratio": 0.55,
"peak_sales_hour": 15,
"business_category": "Retail"
}
]
}

My Contribution

As the Data Scientist on this project, I:
	•	Designed and generated the dataset
	•	Built the feature engineering pipeline
	•	Implemented clustering (K-Means)
	•	Developed the credit scoring logic
	•	Created the risk classification system
	•	Built the AI API using FastAPI

Future Improvements
	•	Integration with payment platforms such as Interswitch
	•	Real time streaming data processing
	•	Advanced ML models (XGBoost, Neural Networks)
	•	Fraud detection capabilities

Project Goal

To enable inclusive, data driven lending by using real transaction behavior instead of traditional credit history.
