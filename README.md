# Equity Index Telemetry Dashboard

**A simple real‑time monitoring system for a custom equity index**, tracking its value, data quality, and update status.

## 🚀 Tech Stack
- **Python**: data pipelines & logic  
- **Streamlit**: interactive dashboard  
- **SQLite**: lightweight telemetry storage  
- **Yahoo Finance API**: live market data  
- **Airflow**: scheduled updates  

## 🗂 Project Structure
```graphql

equity-index-telemetry-dashboard/
├── data/                     # raw or sample data files
│   └── dummy/                # optional: dummy CSVs for testing
├── db/                       
│   └── index.db              # SQLite database file for index values & telemetry
├── src/                      
│   ├── __init__.py           
│   ├── data_fetcher.py       # pulls stock prices
│   ├── index_calculator.py   # computes custom index
│   ├── telemetry_logger.py   # logs status & metrics
│   └── dashboard.py          # Streamlit app
├── airflow/                  
│   └── dags/                 
│       └── update_index.py   # Airflow DAG to run updates periodically
├── tests/                    
│   ├── test_data_fetcher.py  
│   ├── test_index_calculator.py
│   └── test_telemetry_logger.py
├── requirements.txt          
└── README.md                 
```
## ⚙️ Setup & Installation

1. **Clone repo**  
  ``` bash
   git clone https://github.com/yourusername/equity-index-telemetry-dashboard.git
   cd equity-index-telemetry-dashboard
```
2. **Create virtual env & install**
    ```bash
     python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```

3. **Initialize database**
   ```python
     python - <<EOF
    from src.telemetry_logger import init_db
    init_db()
    EO
    ```

## 🏃‍♂️ Usage
- Run locally
```bash
streamlit run src/dashboard.py
```

- Start Airflow
```
airflow standalone
# DAG equity_index_telemetry will run hourly

```


## 🧪 Testing
```bash
pytest tests/
```
## 📈 Features & Roadmap
 - Fetch live prices & compute index

 - Log updates & statuses

 - Interactive dashboard

 - Add anomaly detection alerts

 - User authentication & access logs

 - More sophisticated index rebalancing

### 🤝 Contributing

Feel free to open issues or PRs—happy to collaborate!
