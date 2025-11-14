You nedd to run Powershell with  admin rights, it may give you some errors or just stop, close it and relaunch it, this time will launch without errors and will start tracking uptime


# Koii-Uptime-Tracker
Koii Uptime Tracker
This PowerShell script monitors the Koii Node process, tracks its uptime, CPU load, and memory usage, and logs this data to a file. Here’s what it does:

Main Features:
Ensures Execution Policy:

Sets the execution policy to RemoteSigned for the current user to allow the script to run.
Creates Necessary Log Folders:

The script ensures that the uptime directory exists at:
C:\Users\YOURUSERNAME\AppData\Roaming\KOII-Desktop-Node\uptime
If the directory doesn’t exist, it is created.
Tracks Uptime & Monthly Uptime:

Stores total uptime in uptime_data.json.
Tracks monthly uptime separately in monthly_uptime.json.
Monitors Koii Node Process:

Scans running processes for any related to Koii.
Retrieves process details such as:
Start time
CPU load
Memory usage
Calculates total uptime by adding previous uptime if the process restarts.
Updates the log file (uptime_log.txt) with the latest uptime data.
Handles Log File Size:

Keeps only the last 2000 entries to prevent excessive log file growth.
Highlights Important Tasks:

Looks for specific task names (like "SMART Task", "KPL token Miner", "Reverie Field Compute", etc.) in the command line.
Hides Certain Information (Per Your Request):

The executable path is commented out.
The command-line details are commented out.
Runs Continuously:

The script runs in an infinite loop (while ($true)) and checks every hour.
