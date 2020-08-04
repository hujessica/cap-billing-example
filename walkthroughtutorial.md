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

## Before you begin

Before you attempt this tutorial, you will need the following 
resources:
+ An [active Cloud billing account](https://cloud.google.com/billing/docs/how-to/manage-billing-account#create_a_new_billing_account), where you are a billing admin, or you have been granted the correct level of permissions to complete the steps in this tutorial.

## Create a project

Caution: Using this method will remove Cloud Billing from your project, shutting down all resources. 
This may result in resources being irretrievably deleted, with no option to recover services. 

You can re-enable Cloud Billing, but there is no guarantee of service recovery and manual configuration is required. 
To ensure that services within that project might be removed with no guarantee of recovery in this tutorial, [create a new project](https://cloud.google.com/resource-manager/docs/creating-managing-projects#console) in Google Cloud Console for testing purposes. 
