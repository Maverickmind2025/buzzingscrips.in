# BuzzingScrips.in

This repository powers the BuzzingScrips.in website.

## Files
- `nse_companies.json` → Static NSE company list (replace with full file)
- `realtime_hits.json` → Auto-updated with trending matches
- `latest.json` → Auto-updated with hourly spikes
- `scripts/generate_json.py` → Script that fetches & matches Google Trends terms
- `.github/workflows/update-json.yml` → GitHub Actions workflow for auto updates

## Setup
1. Replace `nse_companies.json` with your full file (from CSV→JSON conversion).
2. Push repo to GitHub.
3. Add GitHub Secrets:
   - `FTP_SERVER` = ftp.buzzingscrips.in
   - `FTP_USERNAME` = your Hostinger FTP username
   - `FTP_PASSWORD` = your Hostinger FTP password
4. GitHub Actions will run every 30 minutes during NSE hours and upload new JSONs to `/public_html/data/`.
