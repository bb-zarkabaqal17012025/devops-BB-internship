# EC2 Tag Compliance Checker

This script scans running EC2 instances across multiple AWS regions and reports any instances that are missing required tags. It outputs the results in a structured Excel file with one sheet per region.

## Overview

Maintaining proper tagging across EC2 instances is important for cost tracking, automation, and compliance. This script automates the validation process to ensure that all required tags are present on every running instance.

## Features

- Scans EC2 instances in specified AWS regions.
- Filters only instances in the `running` state.
- Checks for presence of required tags.
- Outputs results to an Excel file (`task2.xlsx`).
- Organizes non-compliant instances into separate sheets per region.

## Prerequisites

- Python 3.x installed
- AWS credentials configured (via AWS CLI, environment variables, or IAM roles)
- Required Python libraries:
  - boto3
  - openpyxl

Install dependencies with:

```bash
pip install boto3 openpyxl
```
Required Tags
Each instance is expected to have the following tags:

patch

ssm-key-automation

application_module

os

team

Name

How It Works
Region Setup
The script targets the following AWS regions:

ap-south-1

us-east-1

Workbook Initialization
A new Excel workbook is created. The default sheet is removed to maintain clarity.

Instance Discovery
For each region:

All EC2 instances are fetched using describe_instances.

Only instances in the running state are processed.

Tag Validation
Each instance's tags are compared against the required tags. If any are missing, the instance is flagged.

Excel Output
Non-compliant instances are written to a new sheet named after the region. The following fields are included:

InstanceId

InstanceType

Name

application_module

team

patch

os

ssm (from tag: ssm-key-automation)

State

Missing tag values are represented as . or left blank.

Save File
The workbook is saved as task2.xlsx in the current working directory.

Output Example
Each sheet will contain a table like:


InstanceId	InstanceType	Name	application_module	team	patch	os	ssm	State
i-0abc123def456	t2.micro	No name	.	.	.	.	Not tagged	running
Running the Script
bash
Copy
Edit
python script.py
Notes
This script is designed for internal compliance audits.
