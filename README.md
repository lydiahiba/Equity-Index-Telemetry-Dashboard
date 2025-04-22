# Equity Index Telemetry Dashboard

**A simple real‑time monitoring system for a custom equity index**, tracking its value, data quality, and update status.

## 🚀 Tech Stack
- **Python**: data pipelines & logic  
- **Streamlit**: interactive dashboard  
- **SQLite**: lightweight telemetry storage  
- **Yahoo Finance API**: live market data  
- **Airflow**: scheduled updates  

## 🗂 Project Structure
equity-index-telemetry-dashboard/ ├── data/ # sample or raw data ├── db/ # index.db telemetry database ├── src/ # core modules │ ├── data_fetcher.py │ ├── index_calculator.py │ ├── telemetry_logger.py │ └── dashboard.py ├── airflow/ # scheduling DAG │ └── dags/update_index.py ├── tests/ # unit tests ├── requirements.txt └── README.md

bash
Copy
Edit

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
Run locally
```bash
streamlit run src/dashboard.py
Start Airflow
airflow standalone
```


# DAG equity_index_telemetry will run hourly
🧪 Testing
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

🤝 Contributing
Feel free to open issues or PRs—happy to collaborate!
