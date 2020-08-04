# Automating cost controls by capping billing

## Overview

In this tutorial, you will learn to automate cost controls 
by setting up programmatic budget notifications. 
Programmatic budget notifications can be used to disable billing
, which will stop the usage of paid services for your project. 

You may choose to disable billing if you have a hard limit 
on how much money you can spend on Google Cloud. 
This may be the case for students, researchers, or 
developers working in sandbox environments.

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
+ An [active Cloud billing account](https://cloud.google.com/billing/docs/how-to/manage-billing-account#create_a_new_billing_account), where you are a billing admin
, or you have been granted the correct level of permissions to 
complete the steps in this tutorial.
