# EC2 Tag Automation Script

This Python script helps automate the process of checking and updating missing or invalid tags on EC2 instances based on an Excel file. The script checks the `running` EC2 instances across specified AWS regions and compares their tags with the required tags specified in the input file (`missing_tags_instances.xlsx`). If any required tags are missing or contain invalid values, the script updates the instances with the correct tags.

## Features

- Loads an input Excel file (`missing_tags_instances.xlsx`) containing EC2 instance IDs and their corresponding required tags.
- Validates EC2 instance IDs and tag formats.
- Scans EC2 instances across multiple AWS regions (`ap-south-1`, `us-east-1`).
- Updates instances with missing or invalid tags based on the input data.
- Handles instances with invalid or overly large tag values (greater than 256 characters).

## Prerequisites

- Python 3.x
- AWS credentials configured (via AWS CLI, environment variables, or IAM roles)
- Required Python libraries:
  - `boto3`: AWS SDK for Python.
  - `openpyxl`: Python library for reading and writing Excel files.
  
To install the required libraries, run:

```bash
pip install boto3 openpyxl
```

## Input Excel File

The script reads an Excel file named `missing_tags_instances.xlsx`. The file should have the following columns, starting from the second row:

| InstanceId        | InstanceType | Name     | application_module | team    | patch | os    | ssm        | State   |
|-------------------|--------------|----------|--------------------|---------|-------|-------|------------|---------|
| i-0abc123def456   | t2.micro     | WebServer| module1            | dev     | patch1| linux | ssm-key-1  | running |

### Columns:

- `InstanceId`: The EC2 instance ID (e.g., `i-0abc123def456`).
- `InstanceType`: EC2 instance type (e.g., `t2.micro`).
- `Name`: Name of the EC2 instance.
- `application_module`: Application module tag.
- `team`: Team associated with the instance.
- `patch`: Patch version or tag.
- `os`: Operating system of the instance.
- `ssm`: SSM key used for automation (should be a tag with key `ssm-key-automation`).
- `State`: The current state of the instance (e.g., `running`).

The script uses this file to determine the expected tags for each instance.

## How It Works

### Load Input Data

The script loads the input Excel file (`missing_tags_instances.xlsx`) and validates each EC2 instance ID format. If any instance ID is invalid, a message is printed.

```python
input_data = {}
for row in input_sheet.iter_rows(min_row=2, values_only=True):
    instance_id = row[0]
    if instance_id and instance_id_pattern.match(instance_id):
        input_data[instance_id] = { ... }
    elif instance_id:
        print(f"Invalid instance ID format: {instance_id}")
