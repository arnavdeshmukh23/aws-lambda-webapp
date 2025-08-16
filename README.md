# 🚀 Serverless Web App with AWS Lambda

This project demonstrates building a **serverless, event-driven web application** using **AWS Lambda**, **API Gateway**, and **DynamoDB**, without managing any servers.  

---

## 📌 Project Overview

| Component       | Description |
|-----------------|-------------|
| ⚡ Compute      | AWS Lambda (Python function) |
| 🌐 API Layer    | API Gateway (REST endpoints) |
| 🗄️ Database     | DynamoDB (NoSQL storage) |
| 📦 Deployment   | AWS Console / AWS SAM |
| 📸 Screenshots  | Proof of working APIs and DB |

---

## 🛠️ Tech Stack

- **AWS Lambda** – Serverless compute
- **Amazon API Gateway** – RESTful API management
- **Amazon DynamoDB** – NoSQL database
- **Python 3.9** – Lambda function runtime
- *(Optional)* AWS SAM / Terraform – Infra as Code

---

## 🧩 Application Flow

1. Client calls **API Gateway endpoint** (e.g., `/addNote`, `/getNotes`).
2. API Gateway triggers the **Lambda function**.
3. Lambda processes the request and interacts with **DynamoDB**.
4. Response is sent back via API Gateway.

---

## 🚀 Deployment Steps

### 1️⃣ Create Lambda Function
- Runtime: Python 3.9
- Handler: `lambda_function.lambda_handler`

Example:
```python
import json
import boto3
dynamodb = boto3.resource('dynamodb')
table = dynamodb.Table('NotesTable')

def lambda_handler(event, context):
    note_id = event.get('noteId', '1')
    note_text = event.get('noteText', 'Hello World')
    table.put_item(Item={'noteId': note_id, 'noteText': note_text})
    return {
        'statusCode': 200,
        'body': json.dumps(f"Note saved: {note_text}")
    }
