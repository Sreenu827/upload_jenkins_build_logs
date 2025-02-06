enkins Build Log Backup Script
This is a simple Bash script that automates the process of backing up Jenkins build logs to an AWS S3 bucket. The script iterates through Jenkins job directories, checks if the build log was created today, and if so, uploads the log file to a specified S3 bucket with the job name and build number as the filename.

Features:
Automated Backup: Automatically uploads Jenkins build logs to AWS S3.
Daily Backup: Only uploads logs created on the current date.
Easy Integration: Simply update the script with your Jenkins home directory and S3 bucket details.
Efficient Log Management: Keeps your Jenkins logs stored and organized in S3 for easy access and archiving.
Requirements:
AWS CLI: The AWS CLI must be installed and configured with the necessary credentials.
Jenkins: The script assumes Jenkins is installed and jobs are located in the default Jenkins home directory.
How to Use:
Install AWS CLI: Make sure the AWS CLI is installed and configured with your AWS credentials.
Modify Variables: Set the JENKINS_HOME variable to your Jenkins home directory and S3_BUCKET to your desired S3 bucket.
Run the Script: Execute the script to automatically upload today's Jenkins build logs to your S3 bucket.
./backup_jenkins_logs.sh
Example:
If a job named frontend has a build with number 42, the script will upload the log as:
"s3://your-s3-bucket-name/frontend-42.log"
