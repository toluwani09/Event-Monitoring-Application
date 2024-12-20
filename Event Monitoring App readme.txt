
# Event Monitoring Application - README

This README provides step-by-step instructions to deploy and manage the Event Monitoring Application using the AWS CloudFormation stack.

## Overview

The Event Monitoring Application is designed to utilize AWS free-tier services to create an event-driven system. The stack provisions the following AWS resources:

- **S3 Bucket**: Stores event data.
- **SNS Topic**: Sends notifications for specific events.
- **IAM Role**: Grants required permissions for SNS.
- **S3 Bucket Policy**: Manages access to the bucket.

## Prerequisites

Before you begin, ensure you have the following:
1. An active AWS account.
2. Permissions to create and manage CloudFormation stacks, IAM roles, S3 buckets, and SNS topics.
3. (Optional) AWS CLI installed and configured on your machine.

## Deployment Steps

### Step 1: Obtain the CloudFormation Template
1. Download the JSON template file provided for the stack.

### Step 2: Deploy the CloudFormation Stack

#### Using the AWS Management Console:
1. Log into the AWS Management Console.
2. Navigate to the **CloudFormation** service.
3. Click on **Create Stack** and select **With new resources (standard)**.
4. Under **Specify template**, choose **Upload a template file**.
5. Upload the downloaded JSON template and click **Next**.
6. Provide a stack name, e.g., `EventMonitoringAppStack`.
7. Configure stack settings as needed and proceed through the wizard.
8. Review the configuration and click **Create Stack**.

#### Using the AWS CLI:
Run the following command, replacing `<template-file-path>` with the path to your JSON file:

```bash
aws cloudformation create-stack --stack-name EventMonitoringAppStack --template-body file://<template-file-path>
