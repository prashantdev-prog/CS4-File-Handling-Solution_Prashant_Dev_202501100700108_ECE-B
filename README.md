# CS4-File-Handling-Solution_Prashant_Dev_202501100700108_ECE-B
Log File Analyzer System

Overview:
The Log File Analyzer System is a Python-based program developed to analyze and process system log data.

The program:
- Reads a log file containing system activity records
- Identifies different log levels (INFO, WARNING, ERROR)
- Counts occurrences of each log type
- Separates logs into different files based on categories
- Allows searching for specific keywords
- Demonstrates file pointer operations for better file handling understanding

Objectives:
- To understand file handling in Python
- To analyze structured log data efficiently
- To classify logs based on severity levels
- To implement search functionality within files
- To demonstrate file pointer operations (seek)
- To generate and manage multiple output files

Program Features:
- Reads data using read(), readline(), readlines()
- Displays total number of lines, first 2 lines, last 2 lines

Log Classification:
- Counts number of INFO, WARNING, ERROR logs
- Stores result in dictionary

File Generation:
- info_logs.txt -> INFO logs
- warning_logs.txt -> WARNING logs
- error_logs.txt -> ERROR logs

Search Feature:
- Accepts user input keyword
- Displays matching lines
- Saves results in search_result.txt

File Pointer Operations:
- Reads first 50 characters
- Moves pointer using seek():
  * Beginning: seek(0)
  * Middle: seek(len(file)//2)
  * End: seek(-100, 2)
- Displays content after each movement

Technologies Used:
- Programming Language: Python 3
- Built-in file handling functions
- Platform: Any Python IDE or Command Line

Concepts Applied:
- File Handling (Read/Write)
- String Searching
- Data Classification
- Dictionary Usage
- File Pointer Manipulation
- User Input Handling

Sample Working:
- Reads CS4.txt log file
- Displays total lines, first and last entries
- Counts INFO, WARNING, ERROR logs
- Creates separate log files
- Searches keyword entered by user
- Demonstrates file pointer movement

Output Files:
- info_logs.txt
- warning_logs.txt
- error_logs.txt
- search_result.txt

Conclusion:
This project helps understand log processing, file handling, and automation using Python.

Author Details:
Name: Prashant Dev
Roll No: 202501100700108
