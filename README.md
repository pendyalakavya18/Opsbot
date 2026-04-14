# OpsBot - Log Automator

A Python script designed to help IT teams quickly find security threats and errors in server logs. It filters through thousands of lines of data and creates a summarized alert report.

## How it Works
The script reads `server.log` and looks for three specific keywords:
- `CRITICAL`
- `ERROR`
- `FAILED LOGIN`

It ignores all other "INFO" messages to reduce clutter.

## Features
- **Auto-Filtering**: Skips routine logs and saves only the critical ones.
- **Tally System**: Counts the frequency of each error type.
- **Dated Reports**: Creates a unique text file with the current date (e.g., `security_alert_2026-04-14.txt`).
- **File Validation**: Reports the final size of the alert file.

## Usage
1. Make sure you have a `server.log` file in the same directory.
2. Run the script:
   ```bash
   python opsbot.py
   ```
3. Check the console for the summary and open the generated `.txt` file for the full report.

## Deliverables
- `opsbot.py`: The main logic script.
- `server.log`: Sample log file for testing.
- `security_alert_[date].txt`: The filtered output report.
