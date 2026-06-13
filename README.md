# SentinelIQ - Insider Threat Intelligence Dashboard

SentinelIQ is a specialized security dashboard designed to monitor, identify, and investigate potential insider threats and data access anomalies. It combines chronological event tracking, temporal access matrices (heatmaps), and structured incident reporting with interactive AI-driven forensic analysis.

## Features

- **Threat Overview**: Real-time stats on critical threats, high-risk events, flagged users, and department risk rankings.
- **Active Alerts**: Searchable and filterable dashboard of anomalous access attempts.
- **Event Timeline**: A detailed, date-grouped stream of access events and security logs.
- **Case Files**: Profiles of high-risk users automatically classified by anomaly scoring.
- **Access Heatmap**: A temporal matrix mapping access volume across hours and weekdays.
- **AI Analyst**: Interactive conversational assistant to assess individual threat profiles.
- **Reports**: Auto-generation of board-ready Executive Summaries, Compliance Reports (GDPR/SOX/NIST), and Forensic Incident files.

## Running the Code

1. Install the dependencies:
   ```bash
   npm install
   ```

2. Start the local development server:
   ```bash
   npm run dev
   ```

3. Build the application for production:
   ```bash
   npm run build
   ```

## Deployment

This project is intended for static deployment, and the GitHub Actions workflow will automatically deploy the `dist/` folder to GitHub Pages on push to `main` or `master`.

1. Push your code to the `main` or `master` branch.
2. The workflow in `.github/workflows/deploy.yml` will run `npm install` and `npm run build`, then publish `dist/` to the `gh-pages` branch.
3. In GitHub repository settings, enable GitHub Pages and select `gh-pages` as the source branch.

### Notes

- `src/imports/anomaly_predictions.json` and `src/imports/evaluation_metrics.json` are pre-generated for the static frontend.
- If you want updated pipeline data, run `python backend/run_pipeline.py` locally before `npm run build`.
