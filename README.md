# Log-File-Processor-with-Time-Based-Aggregation
This project simulates the work of a Data Engineer analyzing system logs. It includes:

- Log generation using synthetic data  
- Data cleaning and transformation  
- Aggregation of events by time (hourly)  
- Identification of top users by activity  
- Visualizations and data export  

---

## Project Structure

```
log_file_processor/
├── data/
│   └── logs.csv                ← Raw synthetic log data
├── output/
│   ├── summary_by_hour.csv     ← Hourly event counts
│   ├── top_users.csv           ← Most active users
│   └── events_per_hour.png     ← Bar chart of events
├── generate_logs.py            ← Generates fake log file
├── log_processor.py            ← Processes & analyzes logs
├── requirements.txt            ← Python dependencies
└── README.md                   ← Project documentation
```

---

## How to Run

1. **Install dependencies**:

```bash
pip install -r requirements.txt
```

2. **Generate the logs**:

```bash
python generate_logs.py
```

3. **Process the logs**:

```bash
python log_processor.py
```

The cleaned results and visualizations will be saved in the `output/` folder.

---

## Cleaning Steps

- Standardize `event_type` text (strip & lowercase)
- Drop missing or malformed entries
- Convert timestamps to datetime format

---

## Analysis & Algorithms

| Task                        | Tools Used                          |
|-----------------------------|-------------------------------------|
| Event count per hour        | `defaultdict` from `collections`    |
| Top 5 active users          | `Counter` + `heapq.nlargest()`      |
| Sorting for visualization   | Pandas `sort_values()`              |
| Visualization               | `matplotlib`                        |

---

## Outputs

- `summary_by_hour.csv` – Number of events per hour  
- `top_users.csv` – Top 5 users based on activity  
- `events_per_hour.png` – Bar chart for quick insights  

---

## Future Enhancements

- Add daily/hourly heatmaps  
- Generate event type breakdown pie charts  
- Export reports to Excel or PDF  
- Build a Streamlit/Dash dashboard for interaction  

---

## Author

**Osama Mohamed Ali**  
Data Engineering & AI Trainee – Digital Egypt Pioneers  

- [GitHub](https://github.com/osamagetmu)  
- [LinkedIn](https://www.linkedin.com/in/osama-m-ali2/)
