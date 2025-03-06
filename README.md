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

### March 3
- Completed ReplicaSets, Deployments, Services and namespaces in the second chapter of the CKA course. Also completed their practice tests.

### March 4
- Studied about custom metrics in Prometheus and wrote a script for a custom metric which can then be queried by PromQL and can be used to create Grafana dashboard.
- Exploring how to connect the python script with Prometheus configuration.
- Studied Manual Scheduling in CKA course and completed its practice test.

### March 5
- Wrote a script to read csv files from s3 uri and make custom metrics on the basis of the csv.
- Started studying kube bench
---

This document serves as a detailed log of my internship progress, capturing the skills and tools I have worked on so far. It will be continuously updated as I progress further.

