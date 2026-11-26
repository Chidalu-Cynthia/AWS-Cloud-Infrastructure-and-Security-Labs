
# AWS Serverless Computing with AWS Lambda

## 1. Project Overview and Objectives

This project focused on exploring serverless computing using AWS Lambda.

The objective was to create and deploy a Python-based Lambda function, understand its execution environment and IAM permissions, invoke the function, and inspect its execution logs through Amazon CloudWatch.

## 2. Architecture and Resource Design

The lab used AWS Lambda to execute Python code without provisioning or managing an EC2 server.

**Execution flow:**

`Test Event → AWS Lambda Function → Execution Role → CloudWatch Logs`

The Lambda function used an assigned IAM execution role to access the AWS resources required for its execution and logging.

## 3. AWS Services and Configurations

- **AWS Lambda:** Created the function `CloudSecurity-Lambda-Lab`.

  ![Created Lambda Function](screenshots/Created%20Lambda%20Function.png)

- **Runtime Configuration:** Selected Python 3.13 with the x86_64 architecture.

  ![Configured Lambda Runtime](screenshots/Configured%20Lambda%20Runtime.png)

- **IAM Execution Role:** Used an IAM execution role to provide the Lambda function with the permissions required for execution and CloudWatch logging.

  ![Configured Lambda Execution Role](screenshots/Configured%20Lambda%20Execution%20Role.png)

- **Lambda Function Code:** Deployed Python code containing the `lambda_handler` function.

  ![Deployed Lambda Function Code](screenshots/Deployed%20Lambda%20Function%20Code.png)

- **Amazon CloudWatch:** Used CloudWatch Logs to inspect the Lambda function's execution records.

  ![Verified Lambda CloudWatch](screenshots/Verified%20Lambda%20CloudWatch.png)

## 4. Implementation and Key Decisions

I created `CloudSecurity-Lambda-Lab` and configured its execution environment with Python 3.13 and x86_64 architecture.

I used an IAM execution role rather than embedding AWS credentials in the function code.

After deploying the Python `lambda_handler` code, I invoked the function using the Lambda console's test feature.

The function returned:

`Hello, Cloud Learner! Your first Lambda function is working.`

## 5. Security Considerations

- Used an IAM execution role to provide permissions to the Lambda function.
- Avoided embedding long-term AWS credentials in the function code.
- Used the assigned execution role for access to AWS services required by the function.
- Used CloudWatch Logs to inspect function execution activity.

## 6. Testing and Validation

I invoked the Lambda function through the AWS console test feature.

The execution completed successfully and returned the expected response:

`Hello, Cloud Learner! Your first Lambda function is working.`

The execution details showed:

- **Execution status:** Succeeded
- **Function version:** `$LATEST`
- **Execution duration:** 2.32 ms
- **Billed duration:** 97 ms
- **Configured memory:** 128 MB
- **Maximum memory used:** 34 MB

![Tested Lambda Function](screenshots/Tested%20Lambda%20Function.png)

I also accessed the function's CloudWatch Logs to inspect its execution records.

## 7. Troubleshooting and Findings

During the lab, I explored the Lambda console's test feature and learned how to invoke a deployed function and inspect its execution result.

The successful invocation confirmed that the deployed Python function executed and returned the expected response.

I also explored CloudWatch Logs as a way to inspect execution activity and support troubleshooting.

## 8. Lessons Learned

This project helped me understand how AWS Lambda executes code without requiring users to provision or manage servers.

I gained practical experience creating a Lambda function, configuring its runtime, assigning an IAM execution role, deploying Python code, testing the function, and inspecting its logs through CloudWatch.

I also learned how Lambda execution details provide useful information about function performance and resource consumption.
