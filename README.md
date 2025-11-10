# AI-Threat-Classifier

A practical cybersecurity project that parses Windows Sysmon logs, builds behavioral features, and detects unusual process activity with an Isolation Forest model.

## Features
- Stream parses XML Sysmon logs into a structured table
- Feature engineering: command length, PowerShell/base64 detection, temp path, parent-child process
- Unsupervised ML (IsolationForest) to score anomalies
- Outputs:
  - `sysmon_with_anomaly_scores.csv` (full results with scores)
  - `suspicious_commands.txt` (triage list)
- Visualizations in the notebook:
  - Command length distribution
  - Anomalies over time

## How to run (locally)
```bash
pip install -r requirements.txt
jupyter lab  # or jupyter notebook

## Disclaimer
This project was developed with the assistance of AI tools.  
While the code and documentation were carefully reviewed, some errors or inconsistencies may still exist.
