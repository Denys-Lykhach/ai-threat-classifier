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
- Open the notebook file   -  `notebook/ThreatClassifier.ipynb`
- Update the input path to your Sysmon log file:
  -  `SYSLOG = "/path/to/your/sysmon.log" `
- Update the output path for saving processed results:
  -  `OUT_DIR = Path("/path/to/save/results") `
- Run all cells in the notebook. 

## Expected Results
After execution, you should see results similar to these:

- Command Line Length Distribution
<img width="982" height="416" alt="length-distribution " src="https://github.com/user-attachments/assets/3aabc6dc-a7cf-4c1a-85be-4457ab808b27" />
- Anomalies Over Time
<img width="1023" height="385" alt="anomalies-over-time" src="https://github.com/user-attachments/assets/7951fe78-a3e0-42ec-a3ec-4e1ed57565c4" />
- Suspicious Commands
<img width="976" height="185" alt="suspicious-command" src="https://github.com/user-attachments/assets/377eb750-4870-4f78-8be0-1f2b10744cb7" />

## Disclaimer
This project was developed with the assistance of AI tools.
While the code and documentation were carefully reviewed, some errors or inconsistencies may still exist.
