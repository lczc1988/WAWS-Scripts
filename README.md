# WAWS-Scripts
Sample Script (Powershell, X-CLI, RestAPI, etc) related to Windows Azure Websites

##NodeCrashDump 
Powershell script can be run as webjob. It will attach to the node.exe automatically and monitoring for exceptions/crashes.

This can also be used for w3wp.exe and php-cgi.exe.

###Usage
Download the zip, change the deploy user name and password. Zip it again ,and then upload the zip as triggered webjobs. For more about deploy credential:
https://github.com/projectkudu/kudu/wiki/Deployment-credentials

###Note
When using this, it's better:
1. Enable Always-On feature
2. Set the WEBJOBS_IDLE_TIMEOUT to a value which is longer enough

##MonitorProcesses 
Powershell script can be run as Continuous webjob. It uses Kudu Rest API to get the processes info like name, ID, and resoruces usage into CSV file.

Whenever there is a problem, we can analyze this CSV output for:
1. resource usage
2. Process restart

