
# WFP Somali Region – Process Monitoring Thematic Cleaner (Redeploy)

This redeployable package includes a **robust MoDA header detection** so your multi-sheet exports process reliably.

## Deploy locally
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scriptsctivate
pip install -r requirements.txt
streamlit run app.py
```

## Streamlit Cloud
1. Push this repo to GitHub.
2. On Streamlit Cloud, select the repo and `app.py`.
3. Ensure the Python version is 3.9+ and dependencies install from `requirements.txt`.

## Notes
- Header detection scans the first 50 rows in each sheet for typical MoDA columns (e.g., `starttime`, `endtime`, `_uuid`, `region`, `woreda`, `monitoring month`).
- Debug log shows **which sheets were processed** and their **row counts**.
- Outputs: `Wide_Cleaned`, `Fact_Long`, `Indicator_Mapping` (Excel, multi-sheet).
