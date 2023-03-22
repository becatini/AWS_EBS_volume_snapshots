# EBS Volume Snapshots List Created on the Current Month

The script will create a .csv file from the EBS volume snapshots created on the current month.

The report will be generated based on the Value of the Tag Name.
If the script will be executed for a different environment, the flag *Name=tag:Name,Values=snapshot_name** has to be changed.

**Steps:**

- Log in into AWS console.
- Select the desired region.
- Open Cloudshell.
- Run the code below.
- Download the file ebs_snapshots.csv
```
aws ec2 describe-snapshots --filters Name=tag:Name,Values=snapshot_name*  --query 'Snapshots[].[Tags[?Key==`Name`]|[0].Value]' --output text |grep `date +%y-%m-` >ebs_snapshots.csv
```
