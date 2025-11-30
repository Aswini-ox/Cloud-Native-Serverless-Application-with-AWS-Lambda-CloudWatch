AWS Serverless Application using Lambda & CloudWatch Monitoring
📌 Project Overview

This project demonstrates a complete serverless application on AWS using:

AWS Lambda (Python function)

API Gateway (HTTP endpoint to trigger Lambda)

CloudWatch Logs & Metrics (monitoring)

Optional: DynamoDB Integration

The application returns:
"Hello from Lambda!"

All actions are monitored in CloudWatch Logs & Dashboard.

🛠️ Technologies Used

AWS Lambda (Python)

Amazon API Gateway

AWS CloudWatch Logs

CloudWatch Metrics & Dashboard

IAM Permissions

📂 Lambda Function Code
def lambda_handler(event, context):
    print("Lambda function invoked successfully!")
    print("Event received:", event)
    return {
        "statusCode": 200,
        "headers": {"Content-Type": "application/json"},
        "body": "Hello from Lambda!"
    }

🚀 API Gateway Setup

Route: /

Method: GET

Integration: AWS Lambda

Invoke URL:

https://47ojx6yz9k.execute-api.eu-north-1.amazonaws.com/

📊 CloudWatch Monitoring
CloudWatch Logs Show:

Lambda execution

API request details

Duration, Init time, Memory usage

CloudWatch Metrics Used:

Lambda Invocations

Lambda Duration

Lambda Errors

API Gateway Request Count

API Latency

Dashboard Widgets:

Lambda Invocation Count

Lambda Error Count

Lambda Duration Graph

API Gateway 4XX / 5XX

API Request Count

🗂️Screenshots

<img width="1915" height="889" alt="Screenshot 2025-11-30 102831" src="https://github.com/user-attachments/assets/f0e7accc-6291-413e-8cd4-23cb5144bd4f" />

<img width="1919" height="862" alt="Screenshot 2025-11-30 102955" src="https://github.com/user-attachments/assets/d00c4521-f656-4ce6-8da2-c2976470ba95" />
<img width="1919" height="878" alt="Screenshot 2025-11-30 103102" src="https://github.com/user-attachments/assets/c5847f6e-3103-43a8-8323-2ef97f477030" />

<img width="1919" height="882" alt="Screenshot 2025-11-30 103146" src="https://github.com/user-attachments/assets/8093e3fb-a51c-4c1f-8746-97af9c5004ba" />
<img width="1919" height="888" alt="Screenshot 2025-11-30 103200" src="https://github.com/user-attachments/assets/1461a496-0342-4e94-af9f-e8bf22dd972c" />
<img width="1919" height="945" alt="Screenshot 2025-11-30 103212" src="https://github.com/user-attachments/assets/ecab8fe9-f060-4551-b606-8a830de5256a" />

<img width="1919" height="872" alt="Screenshot 2025-11-30 103410" src="https://github.com/user-attachments/assets/d8fbef2a-5281-4cdf-8795-2538f08d48b6" />
<img width="1918" height="881" alt="Screenshot 2025-11-30 103438" src="https://github.com/user-attachments/assets/a4d75f26-8ed5-4f42-aba5-7cb3818cabd3" />

📐 Architecture Diagram
Client → API Gateway → Lambda Function → CloudWatch Logs
                                   ↓
                             (Optional DynamoDB)

🔐 IAM Permissions

Attach to the Lambda execution role:

AWSLambdaBasicExecutionRole (required)

AmazonDynamoDBFullAccess (optional)

CloudWatchFullAccess (optional for dashboard)

📌 How to Run

Upload Lambda code

Create API Gateway HTTP API

Integrate API → Lambda

Deploy

Open Invoke URL

Monitor logs in CloudWatch

✔️ Output
"Hello from Lambda!"

📦 Conclusion

This project successfully demonstrates:

A fully serverless application

API Gateway → Lambda integration

CloudWatch logging & real-time monitoring

Clean architecture and dashboard visualization
