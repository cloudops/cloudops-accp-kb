---
title: "ACCP User Guide"
slug: accp-user-guide
---

# Overview

Welcome to Alliance Cloud Connect Pilot \(ACCP\). This document will guide you through the process of configuring and connecting to your research apps in a Cloud Connect cloud deployment.

## Summary

The ACCP platform enables you to use Cloud Connect to configure and deploy specific research apps such as JupyterHub, Galaxy, and Magic Castle. In the ACCP interface, you can access the resources deployed in the public clouds, alongside Cloud Connect, which serves as the access point for your research apps.

In this guide, you will find an overview of the basic workflows and concepts in ACCP that you will need to get started, as well as the specific procedures for deploying and connecting to research apps.

## Workflow

The following are the high-level steps required to deploy one or more research apps:

1.  **Select a Cloud Connect deployment**

    The Cloud Connect deployment is where each set of research app deployments can be created, managed, and destroyed. A Cloud Connect deployment has already been created for your use.

2.  **Deploy research app**

    In this step, you will use Cloud Connect to deploy the desired research app in the cloud deployment you selected in the previous step.

3.  **Connect to research app**

    Using the credentials and endpoint that were generated during the deployment, you will now connect to your new research app.


## Basic concepts

-   **Organization**:

    A grouping of related end-users and resources. The services needed to enable Cloud Connect have already been assigned to the organization created for your team.

-   **Environment**:

    A logical unit within an organization that exposes the resources provided by Cloud Connect, and is used to further isolate and group resources securely. Access is controlled via a combination of environment roles and organization access controls.

    An environment has already been provided to you by your principal investigator \(PI\). The environment is named with the Resource Allocation Project Identifier \(RAPI\) associated with your project.

-   **User**:

    A user account is how an individual connects to ACCP.

-   **Member**:

    To access a given environment, a user normally must be made a member of that environment, either manually or automatically. However, some organization-level access controls will grant implied access to environments for certain users even if they aren't members.


## Accessing your environments

To access the platform, follow the procedure in the [Log into ACCP](#drac-onboarding-log-into-cloud-connect) section.

Navigate to **Services** &gt; **Cloud Connect** to see the pre-defined environment that has been created for your team, which might correspond to your RAPI. Within the environment is a Cloud Connect deployment, where you will deploy your research apps.

The user account that was created for you has the been assigned privileges to see all environments in your organization \(this is called the **Admin** system role\). Therefore, there is no need to add yourself as a member to the pre-defined environment.

You may also create new environments as needed. For details on this, as well as on how to access and manage the individual instances, storage, and other resources used by the research app deployments, see the ACCP Administration Guide.

## Troubleshooting

If any errors arise, ACCP includes tools that are helpful for troubleshooting:

-   **Activity log**

    To see a list of events that have been logged by the platform, click on the **Activity** button in the toolbar at the top of the ACCP interface. Each event includes a description and basic identifying properties. If more details are available, they may be viewed by clicking on the link labeled **Details** in the event. If there are any sub-events, click on the disclosure triangle to the left of the event details to see the child events.

-   **Terraform log**

    When deploying a research app, the output of the Terraform process can be accessed by navigating to your cloud deployment, clicking on the desired app, and viewing its details page.


# Log into ACCP

The ACCP platform is available at the following URL: [https://allianceaccp.cloudmc.ca/](https://allianceaccp.cloudmc.ca/)

In order to log into the system for the first time, will need to open the invitation email that was sent to you. Click on the link to set the password for your ACCP account.

![Screenshot of the email invitation](drac-onboarding-email-invitation.png)

The password requirements will be listed on this page. You will be asked to enter the password twice. If the invitation link has expired, please ask to have the invitation resent to you. Once the password has been saved, you will be redirected to the login page. You are ready to log into the system.

![Screenshot of the ACCP login page](drac-onboarding-accp-login-page.png)

Upon logging in, you are presented with the **Home** page for the system.

![](drac-onboarding-accp-interface.png)

1.  **Workspace**

    The workspace is the main section of all ACCP screens. The items that are visible in the workspace are determined by the context of where you are in the system.

2.  **Main navigation buttons**

    The row of buttons at the top centre of the screen is where you can navigate to all of the major features of the system, including the home page, **Services**, **Reporting**, the **Activity log**, and **Administration**.

3.  **Organization picker**

    ACCP is a multi-tenant platform. Use the organization picker to navigate between the organizations and sub-organizations you have access to.

4.  **Additional tools**
5.  This section contains three items: the help menu, the notifications menu, and the user menu.

# Deploy and Connect to JupyterHub

## Deploy JupyterHub

### Before you begin

-   You must already have a Cloud Connect deployment

### Procedure

1.  Navigate to **Services** &gt; **Cloud Connect** and click on your deployment from the list of cloud deployments.

2.  Click on the **JupyterHub** tab.

    It is also possible to click on your target cloud deployment, then from the sidebar on the left, click on **JupyterHub**. When deploying via this route, the cloud deployment will be pre-selected and not modifiable when deploying JupyterHub.

3.  Click on the **Deploy JupyterHub** button.

    The **Deploy JupyterHub** page appears.

4.  Enter a name for the deployment.

5.  From the **Cloud Deployment** popup menu, select the target cloud deployment.

6.  Click the **Submit** button.

    ![](drac-onboarding-deploy-jupyterhub.png)

7.  The **JupyterHub** tab reappears. The new JupyterHub deployment is being provisioned and will take several minutes.

8.  Once the deployment is complete, the **Notifications** panel will appear with the credentials and endpoint needed to connect to JupyterHub.

    Make a note of this information and store it securely. Once the notification disappears from the panel, it cannot be recovered.

    ![](drac-onboarding-credentials-jupyterhub.png)


### Results

-   Your JupyterHub app has been installed in the selected cloud deployment
-   You have securely stored the credentials and endpoint for the JupyterHub deployment

## Connect to JupyterHub

### Before you begin

-   You must have a [JupyterHub deployment](#drac-onboarding-deploy-jupyterhub) available
-   You must have the endpoint and credentials for the target JupyterHub deployment

### Procedure

1.  Navigate to the URL of the endpoint.

2.  With your credentials, log into JupyterHub.

    ![](drac-onboarding-jupyterhub-login.png)

3.  After the JupyterHub instance launches, you will be presented with the JupyterHub interface.

    ![](drac-onboarding-jupyterhub-interface.png)


# Deploy and Connect to Galaxy

## Deploy Galaxy

### Before you begin

-   You must already have a Cloud Connect deployment

### Procedure

1.  Navigate to **Services** &gt; **Cloud Connect** and click on your deployment from the list of cloud deployments.

2.  Click on the **Galaxy** tab.

    It is also possible to click on your target cloud deployment, then from the sidebar on the left, click on **Galaxy**. When deploying via this route, the cloud deployment will be pre-selected and not modifiable when deploying Galaxy.

3.  Click on the **Deploy Galaxy** button.

    The **Deploy Galaxy** page appears.

4.  Enter a name for the deployment.

5.  From the **Cloud Deployment** popup menu, select the target cloud deployment.

6.  Click the **Submit** button.

    ![](drac-onboarding-deploy-galaxy.png)

7.  The **Galaxy** tab reappears. The new Galaxy deployment is being provisioned and will take several minutes.

8.  Once the deployment is complete, the **Notifications** panel will appear with the credentials and endpoint needed to connect to Galaxy.

    Make a note of this information and store it securely. Once the notification disappears from the panel, it cannot be recovered.

    ![](drac-onboarding-credentials-galaxy.png)


### Results

-   Your Galaxy app has been installed in the selected cloud deployment
-   You have securely stored the credentials and endpoint for the Galaxy deployment

## Connect to Galaxy

### Before you begin

-   You must have a [Galaxy deployment](#drac-onboarding-deploy-galaxy) available
-   You must have the endpoint and credentials for the target Galaxy deployment

### Procedure

1.  Navigate to the URL of the endpoint.

2.  With your credentials, log into Galaxy.

    ![](drac-onboarding-galaxy-login.png)

3.  After the Galaxy instance launches, you will be presented with the Galaxy interface.

    ![](drac-onboarding-galaxy-interface.png)



# Deploy and Connect to Magic Castle

## Deploy Magic Castle

### Before you begin

-   You must already have a Cloud Connect deployment
-   If your cloud deployment resides in AWS, your environment must have its original default VPC

### Procedure

1.  Navigate to **Services** &gt; **Cloud Connect** and click on your deployment from the list of cloud deployments.

2.  Click on the **Magic Castle** tab.

    It is also possible to click on your target cloud deployment, then from the sidebar on the left, click on **Magic Castle**. When deploying via this route, the cloud deployment will be pre-selected and not modifiable when deploying Galaxy.

3.  Click on the **Deploy Magic Castle** button.

    The **Deploy Magic Castle** page appears.

4.  From the **Cloud Deployment** popup menu, select the target cloud deployment.

5.  Enter a name for the deployment.

6.  In the **Domain** text box, enter the domain name for your deployment.

    This is the domain name that will be used by Magic Castle for the Kerberos realm name when initializing FreeIPA, as well as the internal domain name for the cluster. It must be a fully-qualified domain name.

7.  From the **Management and Login Instance Type** popup menu, select the desired instance type for the management and login nodes.

    The system will deploy two instances of the selected type, one for management and one for login, where Magic Castle will be installed. The instance types will vary depending on whether the underlying platform is AWS or Azure.

8.  From the **Compute Node Instance Type** popup menu, select the desired instance type for the compute nodes where Magic Castle will be installed.

9.  In the **Count** text box, enter the number of Magic Castle compute nodes to deploy.

10. \(Optional\) The **Volumes** section allows you to add additional volumes to some or all of your Magic Castle instances. These volumes will be attached to each instance at deployment time. Click on the **Add** button to configure one or more sets of volumes for the tagged instances you select.

    1.  Enter into the **Name** text box the desired name for each volume. Each volume will have this name visible in the backend service.

    2.  Enter the desired size for each volume, in GB, into the **Size** text box.

    3.  The system will create and attach these volumes to the instance with the tags selected in the **Tags** popup menu. The supported tags are `login`, `mgmt`, and `node`. Note that if no tag is selected, the volumes will not be created.

11. \(Optional\) To enable login using SSH keys, use the **SSH Keys section**.

    1.  Selecting **None** will retain the default behaviour, when the Magic Castle cluster is deployed, the system will provide you with the password for the cluster's sudoer account.

    2.  Selecting **New SSH key** will cause a textbox to appear, where you can enter a name for the key, and another text box where you can enter your public SSH key. The key will be created on the backend service and installed into the cluster's sudoer account. No password will be provided to you when the cluster is deployed.

12. \(Optional\) Any other desired SSH keys to be installed directly onto the instances may be entered into the **Other SSH keys** text box. The keys will be created on the backend service and installed into the cluster's sudoer account.

13. Click the **Submit** button.

14. The **Magic Castle** tab reappears. The new Magic Castle deployment is being provisioned and will take several minutes.

15. Once the deployment is complete, a toast notification will appear to advise you that the Magic Castle cluster is ready.

    If you have not entered created a new SSH key for your cluster, the notifications panel will appear and provide you with the password that has been created for you. Copy it and store it in a safe place – once the notification disappears, the password cannot be retrieved.


### Results

-   Your Magic Castle cluster has been installed in the selected cloud deployment.
-   The requested number of compute nodes have been deployed
-   Any additional volumes have been created and attached
-   Your public SSH key has been installed into the cluster sudoers account, or you have been provided and securely stored the credentials for the Magic Castle cluster sudoers account
-   The security groups for the cluster have been configured to allow connections to port 22 for all inbound traffic \(`0.0.0.0/32`\)
-   The Terraform logs contains the endpoint for your cluster, and may be found by clicking on your deployment from the list of deployments on the **Magic Castle** page
-   To see and manage the individual instances, storage, and other resources used by this deployment, navigate to the backend service using the **Services** menu, and click on your environment
-   You may connect via SSH to your login node

## Connect to Magic Castle

### Before you begin

-   You must have a Magic Castle deployment available
-   You must have either the private SSH key installed in your SSH client for the public SSH key that was deployed to the cluster, or the password that was generated for the sudoers account of the cluster, usually `centos`.
-   You must have the IP address of the cluster endpoint, provided in the Terraform logs of the Magic Castle deployment

### Procedure

1.  Open your terminal or your SSH client.

2.  Open a connection to the cluster endpoint, using the username `centos`.

    Connecting with the private key from a Unix-based system: `ssh -l centos -i .ssh/<your_private_key> <IP_address_of_endpoint>`

    Connecting with a password from a Unix-based system: `ssh -l centos <IP_address_of_endpoint>`. The SSH client will ask for the password when the SSH connection is established.

3.  The command for the login node now appears.

# Feature Status

This section provides a summary of the development status of various features in the ACCP platform.

Last updated: 5 February 2025

|Feature|Status|Description|
|-------|------|-----------|
|Cloud Connect Cloud Deployment creation|Complete|Available for AWS and GCP. Azure and Arbutus are under development.|
|CILogon integration|Available with next update|Allows for logging into the AWS console from ACCP using single sign on.|
|JupyterHub basic deployment|Complete|Installs JupyterHub on AWS infrastructure.|
|JupyterHub user creation|In review|Allows user to specify a username and a password to be created in JupyterHub at deployment time.|
|JupyerHub instance and storage type|In review|Allows user to specify a machine type for their instances and storage type for their volumes.|
|Galaxy basic deployment|Complete|Installs Galaxy on AWS infrastructure.|
|Galaxy user creation|In review|Allows user to specify a username and a password to be created in Galaxy at deployment time.|
|Galaxy instance and storage type|In review|Allows user to specify a machine type for their instances and storage type for their volumes.|
|Galaxy instance power management|In review|Allows a Galaxy instance to be stopped, started, and destroyed from within Cloud Connect.|
|Magic Castle basic deployment|Complete|Installs Magic Castle on AWS and Azure infrastructure.|
|Magic Castle simplified deployment form|In review|The simpler form will ask only for machine type and number of compute nodes.|
|Cost reporting|Complete|Available for AWS and Azure deployments.|
|Linking to restricted OpenStack projects in Arbutus|In review|Allows user to link an environment in ACCP to a restricted project in Arbutus, using an ID and secret entered at the time of linking.|

Explanations of status:

-   **Under development**

    Feature is currently being worked on by the CloudOps development team.

-   **In review**

    Feature has been implemented and is currently under review for quality and completeness.

-   **Available with next update**

    Feature has been finalized and will be deployed with the next regularly scheduled software update.

-   **Complete**

    Feature is fully functional on the ACCP platform.


    # ACCP Nextcloud

Nextcloud is an open-source file sync and sharing software, similar to Dropbox, Google drive, etc. The official user documentation is available here: https://docs.nextcloud.com/server/latest/user_manual/en/

Most functions are self-explanatory. Users can login via CILogon using their institutional credentials to the ACCP Nextcloud instance running at: 
https://206-12-91-208.cloud.computecanada.ca/

The default storage quota is 50GB; users may also connect to their Arbutus cloud (or other S3 compatible object storage) using the directions provided below.

Note: this service is provided as part of the Alliance Cloud Connect Pilot (ACCP); therefore ensure that you have multiple copies of any valuable data and do not rely on this service for data backups.

## Accessing Arbutus Object Storage via Nextcloud

Pre-requisites: you must have a project with Object Storage access enabled on the Alliance’s Arbutus cloud (https://docs.alliancecan.ca/wiki/Cloud). Please e-mail cloud@tech.alliancecan.ca for support.

To access the Arbutus object storage, generate the storage access ID and secret key with the [OpenStack command line client](https://docs.alliancecan.ca/wiki/OpenStack_command_line_clients).
1.	Import your credentials with `source <project name>-openrc.sh`.
2.	Create the storage access ID and secret key with `openstack ec2 credentials create`.

To connect the Arbutus object with Nextcloud.

1.	Log into Nextcloud at https://206-12-91-208.cloud.computecanada.ca/ with CILogon with your institution’s username and password.

 ![A](nextcloud-01.png)

 ![A](nextcloud-02.png)

 
2.	Click on your profile in the top right corner and click on “Settings”

 ![A](nextcloud-03.png)
 
3.	Click on “External Storage” in the left side menu.

4.	Enter the name of the folder the Arbutus object storage is mounted to – e.g., Project ABC. Choose “Amazon S3” under the “External storage” column

 ![A](nextcloud-04.png)

5.	Choose “Access Key” under the “Authentication” column
6.	Under the Configuration enter the following information:
    <ol type="a">
    <li>Bucket: &lt;bucket name&gt;
    <li>Hostname: object-arbutus.cloud.computecanada.ca
    <li>Port: 443
    <li>Click on “Enable Path Style”
    <li>Leave “Enable SSL” and “Enable multipart copy” selected
    </ol>
 
 ![A](nextcloud-05.png)


7.	Click the checkmark on the right and enter your institution account’s password.
8.	Click on “Files” in the top left corner

 ![A](nextcloud-06.png)

 
9.	Click on the folder you created to access the files in your Arbutus object storage bucket – e.g., Project ABC
 
 ![A](nextcloud-07.png)


