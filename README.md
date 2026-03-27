# MerchantFloat-AI
AI credit scoring API for Nigeria SMEs
Overview
MerchantFloat AI is an AI-powered credit scoring and loan recommendation system designed for POS merchants. It analyzes transaction behavior to determine creditworthiness, risk level, and loan eligibility in real time.

Problem
Many small and medium-sized merchants lack access to credit due to:
	•	No formal credit history
	•	Dependence on collateral
	•	Manual risk assessment

 Solution
MerchantFloat AI uses POS transaction data to:
	•	Generate credit scores (300–850 scale)
	•	Classify merchants into risk levels
	•	Recommend loan amounts dynamically
	•	Provide actionable business insights
  
Features
	•	AI-based credit scoring engine
	•	Risk classification (Low, Medium, High)
	• Loan recommendation system
	•	Merchant behavioral analysis
	•	Explainable insights

Tech Stack
	•	Python (FastAPI)
	•	Scikit-learn (K-Means Clustering)
	•	Pandas / NumPy
	•	REST API
	•	Frontend (Vercel deployment)
   System Architecture

Transaction Data → Backend (Bun.js) → FastAPI (AI Engine) → Scoring Output → Frontend Dashboard

API Endpoints
GET all merchants
/analyze
GET single merchant
/analyze/{merchant_id}
POST (Real-time analysis)
/analyze
Sample Request (POST)

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

Team
	• Onwukamuche Onyinyechi Lynda
	• David
	• 

Future Improvements
	•	Integration with payment APIs (e.g., Interswitch)
	•	Real-time streaming data
	•	Advanced ML models (XGBoost, Neural Networks)
	•	Fraud detection

Hackathon Goal

To provide an inclusive, data driven lending solution that empowers merchants and improves financial accessibility.
