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

### April 17
- Deep dived into studyingAWS Security hub.
- Completed the documentation about AWS Security Hub.
- The documentation: https://bigbasket.atlassian.net/wiki/x/EYAI5w
- Studied Updates and Rollbacks in CKA course

### April 21
- Studied HPA and manual scaling in CKA Course
- Working on a Grafana dashboard to represent inefficient PDBs.
- Created a panel to showcase ineffiecient PDBs.
- Working on representing min_replicas as well.

### April 22
- Created panels for PDB dashboard.
- Created panels for representing min_replica, max_replica, current_Replicas.
- Working on panels of PDBs.
- Studied about VPA and difference between HPA and VPA.

### April 23
- Studied CKA course.
- Working on studying the bb-iac repository.
- Working on replicating eks cluster using terraform and running kube-bench on it.

### April 24
- Went through the code of bb-iac-resources.
- Understood the base-infra.
- Working on replicating the base-infra of the cluster.
- Studied Backup and restore in CKA.

### April 25
- Worked on node associations in replica cluster.
- Made changes in the service infrastructure.
- Created target groups in replica cluster.
- Facing issues in RBAC, will work on it.

### April 28
- ncountered an issue where nodes were stuck in Pending state; castai-agent and controller pods were not deploying.
- Manually created node groups so that controller and castai-agent could be scheduled.
- Faced a CrashLoopBackOff issue; identified and resolved by increasing the IMDSv2 hop limit.
- After fixing, cluster successfully connected to CAST AI.
- Deployed CoreDNS, kube-bench, EBS-CSI, and EFS-CSI drivers.
- Generated the kube-bench report and are now working on remediating errors and warnings.

### April 29
- Investigated failure of kube-bench check 3.2.7 — Ensure that the --eventRecordQPS argument is set to 0 or a level which ensures appropriate event capture.
- Tried to rectify by passing the flag as kubelet args and kubelet extra args.
- Tried multiple variations including --kubelet-extra-args, --kubelet-args, and inline flag injection.
- Verified using ps -ef | grep kubelet; the --eventRecordQPS flag is not present in the running kubelet process.
- Contacted AWS team for support.
- Identified that the bootstrap script is running twice, likely overwriting the initial kubelet arguments.
- Currently working on a workaround to prevent duplicate bootstrap execution.

### April 30
- After AWS call, one node was showing "--event-qps=0".  To check if it was also visible in other new nodes, we cordoned a node and drained it. When the new node came, it did not show the "event-qps" flag.
- We realised that there were two bootstrap scripts running, and the kubelet took the arguments from the first bootstrap file.
- Talked to  CAST AI team about this. They said that we will have to add a block of code in order to send the extra kubelet args.
- The sample code provided by the CAST AI team was failing because function calls can not be in .tfvars, they have to be in .tf.
- Modified the code and added the extra code in locals and in terraform.tfvars.
- In terraform.tfvars, added the kubelet config:
```
ha_node_configuration = {
      worker_name_tag_suffix = "worker:HA"
      tags_override          = {}
      bootstrap_arguments    = "--kubelet-extra-args '--register-with-taints=HA=true:NoSchedule --node-labels=HA=true,environment=dev-qa'"
      kubelet_config =  {
          "eventRecordQPS" : 0
      }
    }
```
- In locals.tf, we added:
``` 
 kubelet_config       = jsonencode(lookup(value, "kubelet_config", { "event-qps" = 0 }))
```
- This addition worked successfully, the kubelet can successfully pick up the eventRecordQPS flag.
- Cordoned and drained the ndoes to get the new nodes with the new configuration. Ran kube-bench again and it shows 13 pass and 0 fails.
- Checking on warns, documenting those.

## May 2025

### May 2
- Going through the warnings and found the following, I have also documented them in detail. Here is the link for the document: https://bigbasket.atlassian.net/wiki/x/wQGs5w
- system:masters group and eks:addon-manager user are bound to cluster-admin role.
- efs-csi-external-provisioner-role-describe-secrets ClusterRole allows listing and watching secrets.
- Roles like cluster-admin, eks:addon-manager, and eks:cloud-controller-manager contain wildcards (*) in permissions.
- Roles like admin, edit, and system:controller:job-controller allow pod creation.
- Pods in castai-agent and kube-bench are using the default service account with token automount.
- Several system and CAST AI pods auto-mount service account tokens.
- cluster:admin ClusterRoleBinding uses the system:masters group.
- ClusterRoles like admin, edit, and system:aggregate-to-edit contain bind/impersonate/escalate verbs.
- Pods like aws-node, ebs-csi-node, efs-csi-controller, and kube-proxy run with privileged: true.
- Also studied about TLS certificates in CKA course

### May 5
- Went through the warnings and found out the following:
- Pods using hostNetwork: true were found, including aws-node, efs-csi-node, and kube-proxy pods, indicating they share the host’s network namespace.
- Multiple containers do not explicitly set allowPrivilegeEscalation to false, which is a security risk; affected containers include castai, kube-bench, aws-node, ebs-csi, efs-csi, and kube-proxy.
- The cluster uses amazon-k8s-cni with aws-network-policy-agent, which supports NetworkPolicy, but kube-bench may not recognize this.
- No NetworkPolicies are defined in any namespace, which leaves workloads unprotected at the network level.
- Several pods reference secrets via environment variables instead of mounted files, including pods in the castai-agent and kube-system namespaces.
- No external secrets operators (e.g., external-secrets CRDs) were detected, indicating secrets are managed entirely within the cluster.
- Some containers are missing a defined securityContext, which is essential for enforcing runtime security; affected pods belong to castai-agent, kube-bench, etc.
- Many service accounts across various namespaces, including core system components, do not have associated IAM roles via eks.amazonaws.com/role-arn.
- The EKS control plane endpoint is publicly accessible from 0.0.0.0/0, making it vulnerable to external threats.
- Public access to the cluster is enabled, violating best practices for secure EKS deployments which recommend private-only endpoints.

### May 6
- Completed the Warns document: https://bigbasket.atlassian.net/wiki/spaces/~71202062ec8967a5434c45a95a9bad22d6fca5/pages/3886809537/Warnings+for+kube-bench
- Facing some issues as a few warnings are coming even when there is no reason for warnings.
- Studied Generation of ssl certificates for Kubernetes.

### May 7
- Discussed the kube-bench findings with the whole team.
- Have to make some changes in the base-infra to mitigate some warnings.

### May 8
- Ammended the code for cluster qa-eks-msvcs-2-poc and disabled the enable_public_access, but in the cluster, it is still showing as enabled, so, working on that.
- Installed Trivy on an ec2 instance
- Tried to scan an outdated docker image in order to check if it shows vulnerability.
- A precise report is getting displayed.
- Studying  how to integrate it in Jenkins job and firstly generate a report.



### May 9
- Created a Jenkins job in my own Jenkins server in order to check if Trivy is working in Jenkins.
- Created a new Jenkins job in build.bigbasket.com according to the structure of "supernovas-search-BuildImage" job.
- Used Trivy to print the vulnerabilities report to the console.
- Working on saving the generated report to a file.

### May 12
- Trying to get  a clear, readable format of trivy report.
- Studying about Clair and how it compares to Trivy
- Clair has some of issues: the releases also have not been updated from last yea. Will check on it.
- Explored another image scanning tool called Grype.
- Installed it and tried to generate a vulnerability report in an ec2 instance.
- Here is the documentation: https://bigbasket.atlassian.net/wiki/x/sQGc6

### May 13
- Tried to parse the Trivy output and send a Slack message.
- It is working and the summary of vulnerabilities can be sent to Slack channel.
- Tried to abort the scan in case critical vulnerabilities were more than a specific number(here:5).
- It is also working and I was able to abort the script if the Critical vulnerabilities were more than 5.
- Here is the doc: https://bigbasket.atlassian.net/wiki/spaces/~71202062ec8967a5434c45a95a9bad22d6fca5/pages/3846897828/Trivy

### May 14
- Figuring out the version of ubuntu in search image.
- Commited the kube-bench code in msvcs-3
- Raised PR for that


### May 15
- Started exploring the tool kubescape.
- Studied how it works under the hood and what does it use for posture hardening, image scanning and runtime protection.
- Installed it as a CLI tool in the poc cluster (which was used for kube-bench).
- Generated a report and a compliance score against the NSA framework.
- Ran kube-bench successfully in msvcs-3

### May 16
- Documented how to accept risks and exceptions
- Started studying about Kubescape operator
- Installed Kubescape operator but some CRDs are missing, working on that.
- Found image vulnerabilities using kubescape operator

### May 19
- Working on the script to generate p80 p90 cpu p100 p110 memory per day min replica, max replica, cpu req, cpu limit, mem req, mem limit report.
- Generated p80 and p90 for cpu in staging. Validating that.
- Facing an error as too many API calls are being made

### May 20
- Generated some metrics for hqa.
- Facing issues with percentile metrics.
- Some namespaces and deployment names arent getting populated, I am looking into that.

### May 21
- Tried the script to scrape metrics.
- Some data is getting populated correctly, some data is missing.
- Completed the script for checking trusted relationship ARN in IAM roles, waiting for the ARN role.

### May 22
- Could not find the CRDs.
- Repeatedly installed and uninstalled kubescape operator to check if scanning CRDs are getting installed or not.
- Tried to run the cis benchmark check using kubescape CLI.
- I have also updated the document: https://bigbasket.atlassian.net/wiki/x/DYBR6Q
- Also worked on the automation script.

### May 23
- Tried to scan the images fro vulnerabilities using Kubescape.
- Only CVE IDs can be seen and no descriptive title for the vulnerabilities.
- Updated the doc: Kubescape

### May 26
- Working on scheduled scanning in Kubescape.
- Working on runtime threat detection in kubescape.
- Facing some errors.
---

This document serves as a detailed log of my internship progress, capturing the skills and tools I have worked on so far. It will be continuously updated as I progress further.

