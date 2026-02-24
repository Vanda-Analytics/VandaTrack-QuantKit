# VandaTrack Quant Starter Kit

This repository provides a starter kit for accessing and analysing **VandaTrack retail flow data** via:

- REST API  
- Official Python SDK  
- Sample datasets (S3)
- Rerence Data

---

## Documentation

Full documentation is available at:

- REST API: https://docs.vanda-analytics.com/
- Python SDK (`vanda-api`): https://pypi.org/project/vanda-api/

The API documentation includes:
- Authentication instructions  
- Endpoint specifications  
- Pagination details  
- Supported intervals and asset classes

---

## Installation (Python SDK)

```bash
pip install vanda-api
```

Optional (with pandas support):

```bash
pip install vanda-api[pandas]
```

---

## Authentication

All API requests require a Bearer token.

You may authenticate by:

- Using an API token directly  
- Logging in with email/password via the SDK (which retrieves a token)  

Refer to the API documentation for full authentication instructions.

For production usage, store tokens securely (e.g., environment variables).

---

## Sample Data (S3)

Sample datasets are available for offline exploration and backtesting.

**S3 Bucket:**

```
vanda-analytics-samples
```

**Folder:**

```
vandatrack/
```

### Directory Structure

```
vandatrack/
└── equity/
    ├── sample=all/
    ├── sample=nasdaq100/
    ├── sample=russell3000/
    └── sample=sp500/
        ├── interval=10min/
        └── interval=1d/
            ├── bulk.csv
            └── year=YYYY/
```

Each sample is partitioned by:

- Universe (e.g., S&P 500, Nasdaq 100)  
- Interval (e.g., 10min, 1d)  
- Year  

---

## Included Notebooks

### Retail Cash Flows (REST API & Python SDK)
### Real Use Case - Nasdaq 100 Sector Aggregation 


## What This Starter Kit Covers

- Single Security & Aggregate timeseries retrieval 
    - Cash
    - All Frequencies (10min, 30min, 1H, 1D, 1W, 1M)
    - REST API & Python SDK

- Reference Data
    - Aggregate ID - Name mappings

## Coming Soon

Additional analytics capabilities will be added in future releases. Stay tuned. 

For any further questions, please refer to the full REST API documentation or contact sales@vanda.com

---
