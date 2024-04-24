# soc_noc_ggh
Title: Simulator Trace Analyzer
Description:
This Python script analyzes simulator output data to calculate average read latency, average write latency, average latency, and bandwidth.
Requirements:
Python 3.x (https://www.python.org/downloads/)
Installation:
There are no external dependencies to install. Simply clone or download this repository.
Usage:
Prepare Simulator Output:
Run your simulator and ensure it generates trace data containing timestamps and transaction types (read/write).
The script assumes the trace data is stored in a list of lists, where each inner list represents a line from the simulator output.
Adjust the code (particularly process_simulator_output) if your data format differs.
Run the Script:
Open a terminal or command prompt and navigate to the directory containing the script (simulator_analyzer.py).
Execute the script with your simulator output data (replace your_trace_data.py with the actual filename or data structure):python simulator_analyzer.py your_trace_data.py
Alternatively, modify the script to directly accept the trace data as a function argument.
# Assuming your simulator output data is stored in a Python file
trace_data = [
    ["cycle:10", "Rd"],
    ["cycle:20", "Wr"],
    # ... more lines from your simulator output ...
]
Output:
The script will print the calculated average read latency, average write latency, average latency, and bandwidth.
Additional Notes:
Modify the data_width variable in the process_simulator_output function to reflect the actual data width (bytes per transfer) used in your simulation.
The script assumes timestamps are in cycles and uses a regular expression to extract them. Adapt the pattern if your simulator output format differs.

