# Automated_Tcpdump_Collection_python_Script
Python script continuously monitors a log file for specific error strings. Upon finding these errors, it triggers the capture of diagnostic data such as TCPDUMP , top processes, I/O usage, system activity reports, memory and CPU utilization, and processes in 'D' state. Additionally, it triggers tcpdump for 10 minutes to capture network traffic when an error is detected. The script can runs for pre-determined time to monitor the script .

Requirements
Python 3.x
sudo privileges for running tcpdump
Ensure necessary command-line tools (ps, sar, iotop, top) are available
Usage
Set the log file path and define error strings to monitor within the script.
Run the Python script:
bash
Copy code
python log_monitor.py

Description
run_tcpdump(): A function to trigger tcpdump for 10 minutes to capture network traffic.
top_collection(), iotop_collection(), sar_collection(), ps_memory_collection(), ps_cpu_collection(), dstate_collection(): Functions to collect various system diagnostic information.
watch_log_and_tcpdump(): Monitors the log file for error strings, triggers diagnostic data collection when errors are detected.
File Output
error_log.txt: Stores lines containing error strings found in the monitored log file.
capture_tcpdump_YYMMDD-HH:MM:SS: Captured network traffic during error occurrences.
Various diagnostic data files like top_output.txt, iotop_output.txt, etc., capturing system resource usage at the time of error.
Note: Ensure to modify the script as per specific log file paths, error strings, and file naming conventions.
