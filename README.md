# ai-financial-reconciliation-engine

# 💰 AI Financial Reconciliation Engine  
Enterprise-grade AI system that automates matching of invoices, receipts, and bank transactions using OCR + LLM Classification + Rule-based Matching + Anomaly Detection.

---

## 🚀 Features
✔ OCR extraction from PDFs (invoices, receipts)  
✔ CSV/Bank statement ingestion  
✔ LLM-powered transaction classification  
✔ Rule-based & fuzzy matching reconciliation  
✔ Anomaly detection (fraud, duplicates, mismatches)  
✔ Multi-agent validation pipeline  
✔ REST API using FastAPI  
✔ Enterprise-grade logging & modular architecture  

---

## 🏗 Architecture Overview
```
PDF/CSV → OCR → Classification Agent → Reconciliation Engine → Validator Agent → API → Output
```

Agents used:
- **Classifier Agent** → Identify transaction type, vendor, category  
- **Reconciliation Agent** → Match invoice ↔ bank transaction  
- **Validator Agent** → Validate correctness & flag anomalies  

---

## 🛠 Tech Stack
- Python 3.10  
- FastAPI  
- LangChain / Llama 3 / Groq  
- Tesseract OCR  
- Pandas  
- Scikit-learn  
- FuzzyWuzzy  

---

## ▶ Run Locally
```
pip install -r requirements.txt
uvicorn src.main:app --reload
```

API runs at:  
```
http://localhost:8000
```

---

## 📬 Example API Request
```
POST /reconcile
{
  "invoice_pdf": "path/to/invoice.pdf",
  "bank_csv": "path/to/bank.csv"
}
```

---

## 📄 Output Example
```
{
  "status": "reconciled",
  "matched_entries": [...],
  "unmatched": [...],
  "anomalies": [...]
}
```

---

## 🧠 Future Enhancements
- Add Graph-based fraud detection  
- Add Workday/SAP integration  
- Add invoice payment forecasting  
