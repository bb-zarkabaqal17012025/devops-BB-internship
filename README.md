# Internship Progress Updates

## January 2025

### January 28
- Completed VPC setup, successfully creating a VPC with public and private subnets.
- Progressed in learning IAM.

### January 29
- Revised VPC concepts.
- Studied IAM and S3 policies.
- Installed Jenkins on a local system.

### January 30
- Learned the basics of Jenkins and job creation.
- Created two basic Jenkins jobs.
- Configured a job to trigger the build of a demo pipeline.

## February 2025

### February 3
- Learned about parameterized builds in Jenkins.
- Created a job with parameters.

### February 4
- Successfully set up Jenkins on an EC2 instance.
- Installed the Active Choices plugin.
- Learned about:
  - Active Choices Parameter
  - Active Choices Reactive Parameter
  - Active Choices Reactive Reference Parameter
  - String Validation Parameter

### February 5
- Successfully set up RBAC in Jenkins.
- Created a user and a role called `dev`.
- Configured role-based access to allow only job builds while restricting configuration changes.
- Installed Jenkins Job Builder (JJB).
- Studied JJB and templates.

### February 6
- Created a Jenkins job using JJB to run a Python script from a GitHub repository.
- Designed a JJB template to create multiple jobs running Python scripts from different repositories.
- Gained an overview of `bb-capture` and understood its workflow and folder structure.

### February 7
- Understood the workflow in `bb-capture` for Jira ticket creation.
- Studied how to access private Google Sheets.
- Created a private Google Sheet and used Google Drive API and Google Sheets API to access data.
- Wrote Python code to fetch and print data from the private Google Sheet.

### February 10
- Created a script to generate a new Google Spreadsheet.
- Performed CRUD operations on the created spreadsheet.
- Gained an overview of Grafana.

### February 11
- Created a Grafana dashboard with six panels:
  - CPU requests (any cluster, any namespace across regions).
  - CPU utilization (any cluster, any namespace across regions).
  - Delta panel (CPU requests vs. CPU utilization).
  - Memory requests (any cluster, any namespace across regions).
  - Memory utilization (any cluster, any namespace across regions).
  - Delta panel (Memory requests vs. Memory utilization).

### February 12
- Enhanced the Grafana dashboard by adding pie charts.
- Developed a Python script to retrieve Kubernetes events where `REASON == FailedToRetrieveImagePullSecret` and `acr-login` appears in the message.

### February 13
- Improved the Python script to refine the CSV output.
- Successfully retrieved the required data in CSV format.
- Enhanced the Grafana dashboard:
  - Implemented `x-projects` filtering.
  - Made legends more detailed and readable.
- Planned further improvements to the Python script.

### February 14
- Completed `x-project` filtering for Grafana dashboard.
- Awaiting validation.

### February 17
- Finalized filtering requests per project in Grafana.
- Created an additional dashboard for tracking requests per project.

### February 18
- Added a ratio panel for further insights.
- Integrated additional requirements.
- Awaiting validation.

### February 19
- Began studying Kubernetes.
- Tweaked Grafana dashboard to finalize ratio metrics and identify inefficient projects.

### February 20
- Created a new Grafana dashboard displaying:
  - Total requests over the past 14 days.
  - CPU requests.
  - Memory requests.
  - CPU utilization as a percentage of requests.
  - Memory utilization as a percentage of requests.
- Started writing a document on dashboard insights.

### February 21
- Modified the document for clarity.
- Created a cleaner, less cluttered Grafana dashboard for identifying inefficient projects.

### February 24
- Updated the Grafana dashboard document to outline the steps for identifying inefficient projects.
- Studied Kubernetes architecture.

### February 25
- Started with Falco
- Progressed in learning Kubernetes

### February 26
- Set up eks cluster and learnt to scale down the node group using CLI.
- Progressed in Kubernetes.

### February 27
- Successfully set up falco and integrated it with Slack.
  
### February 28
- Completed core concepts of Kubernetes and completed one practice test

## March 2025

### March 3
- Completed ReplicaSets, Deployments, Services and namespaces in the second chapter of the CKA course. Also completed their practice tests.

### March 4
- Studied about custom metrics in Prometheus and wrote a script for a custom metric which can then be queried by PromQL and can be used to create Grafana dashboard.
- Exploring how to connect the python script with Prometheus configuration.
- Studied Manual Scheduling in CKA course and completed its practice test.

### March 5
- Wrote a script to read csv files from s3 uri and make custom metrics on the basis of the csv.
- Started studying kube bench

### March 6
- Deployed kube-bench in a pod in eks cluster.
- It generated reports and saved it in .txt format, trying to get a better understanding of the reports.
- Studied taints and tolerants in CKA

### March 10
- Studied about pushgateway
- Wrote a script for custom jenkins metrics through pushgateway
- Wrote a deployment and service yaml file for pushgateway to inform prometheus to scrape metrics from a specific port
- Studied node affinity in CKA

### March 11
- Modified custom metrics script.
- The custom metrics script is now working and can be queried through grafana
- Installed kube-bench as a helm.
- Working on storing the reports generated by kube-bench into s3.


### March 12
- Successfully deployed kube-bench in qa environment in devops-qa namespace
- Documentation for kube-bench: https://bigbasket.atlassian.net/wiki/external/OTI2ODk0OWQ4M2NiNDYwNzllNDgxNDNhYzZhNjVmNjY
- Working on debugging apps script for spot to cast api calls


### March 13
- Debugged the spot to cast api calls script and got the necessary data.
- Started studying Trivy tool.
- Studied multiple schedulers in Kubernetes. 

### March 17
- Worked on writing the script to generate cost per namespace from cast API
- Studied Admission Controllers in CKA

### March 18
- Modified script to generate cost per team from two APIs.

### March 19
- Further modified the scripts to generate data appropriately for report generation in cost generation of cast ai, now have to create allocation groups
- Studied about Validating and Mutating Admission Controllers.

### March 20
- Wrote the generateReport function to write in the sheet in the format provided.
- Validated correct data is returning from the API

### March 21
- Successfully modified the script to automatically generate weekly cost using CAST API.
- Successfully created a Grafana dashboard to display critical metrics for CAST AI.

### March 24
- Started studying about Terraform.
- Modified the CAST AI Grafana dashboard to include Eviction & rebalancing events, cost per namespace.
- Wrote a script to automate the creation of allocation groups using CAST APIs in various clusters in CAST AI. Waiting for review.

### March 25
- Created allocation groups for qa and staging cluster in CAST AI.
- Wrote a script to generate weekly cost aggregation of qa cluster by using CAST API.
- Created, modified and deleted an EC2 instance using Terraform.
- Analysed the diff if we manually change the EC2 instance and then use "terraform apply".

### March 26
- Tried creating an ec2 instance using Terraform and Jenkins job.
- Successfully created a script to generate a weekly cost aggregation report of clusters: prod, hqa, qa, uat.

### March 27
- Create a Jenkins pipeline to read terraform configuration files from a git repo and create an ec2 instance.
- Learned about variables and outputs in Terraform
- Completed the CAST AI cost aggregation project and transfered its ownership to devops-bot from Sentinels

## April 2025

### April 1
- Created a daily efficiency report for workloads using Cast API for clusters: prod, uat, hqa, qa and staging. Waiting for review.
- Working on Terraform diff through Jenkins job.

### April 2
- Created multiple jobs that create resources using Terraform code in github repo.
- Created a main Jenkins job that triggers these multiple jobs and sends a slack notification in case of a diff.
- Working on modifying it to be more efficient. 

### April 3
- Completed the script to get the complete detailed output for Terraform diff and completed the documentation.
- Documentation: https://bigbasket.atlassian.net/wiki/x/QIFj5g?atlOrigin=eyJpIjoiNTE1ODFkYTY1ZjU1NDY2NjgzM2I1ODk0MmYwYzhkZTUiLCJwIjoiYyJ9
- Working on the Learning Document

### April 7
- Fine tuned the diff-checker job to send diffs.
- Triggered the diff-checker job in qas-iac successfully. It is sending the diff notifications on slack,

### April 8
- Triggered the job for various jobs in non-prod.
- Working on providing a summary for various jobs and their diffs.
- Learning about tfstate.

### April 9
- Triggered the job in qa-iac and created an excel sheet to store summarised drifts.
- Wrote the diff-checker-trial in prod-iac and created an excel sheet to store summarised drifts.
- Studied about modules.

### April 10
- Studied remote backends in Terraform.
- Studied Provisioners and null_resource.
- Will work on understanding the IaC repo.

### April 11
- Successfully wrote Terraform config files for installing Kube-bench helm chart.
- Successfully set up kube-bench using Helm Chart in sandbox eks cluster.
- It is generating reports correctly.
- Working on how to skip or bypass some rules by modifying the values.yaml file.

### April 14
- Standardised the Terraform script to install kube-bench as a helm, will work on making it compatible with bb-iac repo.
- Working on loops, prioritisation of variables, import statement etc

### April 15
- Modified the terraform code to install Kube-bench as a helm according to bb-iac-resources repo.
- Will push the code into a testing branch to check if it works correctly or not.
- Completed the documentation for installation of Kube-bench using Terraform. The document is given below:
https://bigbasket.atlassian.net/wiki/x/J4LC5g
- Will start studying Security Hub for the next task.

### April 16
- Created vpc, route tables, internet gateway, public and private subnets using Terraform.
- Successfully used for_each loop for creation of subnets.
- Studied logging in CKA course.
- Studying Security Hub in detail.








---

This document serves as a detailed log of my internship progress, capturing the skills and tools I have worked on so far. It will be continuously updated as I progress further.

