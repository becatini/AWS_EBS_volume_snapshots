# EBS Volume Snapshots List Created on the Current Month

The script will create a .csv file from the EBS volume snapshots created on the current month.

The report will be generated based on the Value of the Tag Name.
If the script will be executed for a different environment, the flag *Name=tag:Name,Values=<snapshot_name>** has to be changed. (The "<>" must be removed).

**Steps:**

- Log in into AWS console.
- Select the desired region.
- Open Cloudshell.
- Run the script.
- Download the file snapshot_name.csv
