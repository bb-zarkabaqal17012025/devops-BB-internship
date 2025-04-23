This Python script uses Boto3 and OpenPyXL to extract information about available EBS volumes in two AWS regions and exports it to an Excel workbook.

Prerequisites
AWS credentials properly configured (e.g., via AWS CLI or environment variables).

Python packages: boto3, openpyxl

Install them using:
```pip install boto3 openpyxl```
What the Script Does
- Initialize EC2 Clients
```
ec2_ap_south_1 = boto3.client('ec2', region_name="ap-south-1")
ec2_us_east_1 = boto3.client('ec2', region_name="us-east-1")
```
- Creates two EC2 clients for: ap-south-1 (Mumbai), us-east-1 (N. Virginia)

2. Describe Volumes
```
response_ap_south_1 = ec2_ap_south_1.describe_volumes()
response_us_east_1 = ec2_us_east_1.describe_volumes()
```
Fetches details of all EBS volumes in both regions.

4. Create Excel Workbook
```
workbook = Workbook()
```
Starts a new Excel file using openpyxl.

6. Add Sheet for ap-south-1 Region
```
sheet_ap_south_1 = workbook.active
sheet_ap_south_1.title = 'ap-south-1'
sheet_ap_south_1.append(['Volume Type', 'Volume Id', 'Name', 'Size', 'State'])
```
Uses the default sheet.
Renames it to ap-south-1.
Adds column headers.

7. Append Available Volumes
```
for volume in response_ap_south_1['Volumes']:
    ...
    if volume['State'] == 'available':
        sheet_ap_south_1.append([...])
```
Iterates through volumes.
Extracts the Name tag (if present).
Appends volume details only if the state is available.
8. Add Sheet for us-east-1 Region
```
sheet_us_east_1 = workbook.create_sheet(title='us-east-1')
sheet_us_east_1.append(['Volume Type', 'Volume Id', 'Name', 'Size', 'State'])
```
Creates a new sheet for the us-east-1 region.
Adds column headers.
Append Available Volumes (Same logic as above)
9. Save the Excel File
```
workbook.save("available_volumes_sandbox.xlsx")
```
Saves the Excel workbook with two sheets (ap-south-1, us-east-1), each listing available volumes from their respective regions.
