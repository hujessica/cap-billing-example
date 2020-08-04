# Automating cost controls by capping billing

## Overview

In this tutorial, you will learn to automate cost controls by setting up programmatic budget notifications. 
Programmatic budget notifications can be used to disable billing, which will stop the usage of paid services for your project. 

You may choose to disable billing if you have a hard limit on how much money you can spend on Google Cloud. 
This may be the case for students, researchers, or developers working in sandbox environments.

As you complete this guide, you will learn the following skills: 
+ Creating a budget
+ Setting up a Pub/Sub topic
+ Connecting a billing account to a Pub/Sub topic
+ Deploying a function

After completing this tutorial, you can explore other examples
of automating cost controls using the skills learned:
+ [Sending notifications to Slack](https://cloud.google.com/billing/docs/how-to/notify#send_notifications_to_slack)
+ [Selectively controlling usage of resources](https://cloud.google.com/billing/docs/how-to/notify#selectively_control_usage)

**Time to complete:** About 10 minutes

## Getting started 

### Before you begin

Before you attempt this tutorial, you will need:
+ An [active Cloud billing account](https://cloud.google.com/billing/docs/how-to/manage-billing-account#create_a_new_billing_account), where you are a billing admin, or you have been granted the correct level of permissions to complete the steps in this tutorial.

### Select a project

Caution: Using this method will remove Cloud Billing from your project, shutting down all resources. 
This may result in resources being irretrievably deleted, with no option to recover services. 
You can re-enable Cloud Billing, but there is no guarantee of service recovery and manual configuration is required. 

For this tutorial, [create a new project](https://cloud.google.com/resource-manager/docs/creating-managing-projects#console) in Google Cloud Console for testing purposes. 

<walkthrough-project-setup></walkthrough-project-setup> 

## Setup

Set up a default project ID so that you do not need to provide them in commands where those values are required. Replace {{project-id}} with your project’s ID. 

```sh   
gcloud config set project {{project-id}}  
```

Set up names for your budget, Pub/Sub topic, and function.
```sh
export BUDGET_NAME=billing_cap_budget
export TOPIC_NAME=budget-notification
export FUNCTION_NAME=stop_billing
``` 