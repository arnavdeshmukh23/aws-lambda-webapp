# 🌐 Serverless Web App on AWS

This project demonstrates deploying a **completely serverless web application** using **AWS Management Console**.
The app is built with:

-   **Frontend** hosted on **S3 + CloudFront**
-   **API Gateway** as HTTP endpoint
-   **Lambda** function for business logic
-   **DynamoDB** for persistent storage

All resources were provisioned directly via the AWS console — **no local coding required.**

---

### 📌 Project Overview

| Component | Service Used | Purpose |
| :--- | :--- | :--- |
| 🌍 Frontend | S3 + CloudFront | Static HTML hosting + CDN distribution |
| ⚡ Backend Logic | Lambda | Serverless function triggered via API |
| 🚪 API Endpoint | API Gateway | Exposes Lambda as RESTful HTTP endpoint |
| 🗄️ Database | DynamoDB | Stores request data with unique IDs |
| 🔒 IAM | Roles + Policies | Permissions for Lambda to access DynamoDB |

---

### 🧩 Workflow

1.  User accesses the **frontend** hosted on **S3**, distributed via **CloudFront**.
2.  Clicking **Call API** triggers a request to **API Gateway**.
3.  API Gateway invokes the **Lambda function**.
4.  Lambda writes a unique item into **DynamoDB**.
5.  Response is sent back and displayed on the webpage.

---

### 🛠️ Steps Taken

-   **IAM Role** → Created with trust policy for Lambda + DynamoDB + CloudWatch access.
-   **DynamoDB Table** → Created to store requests with unique IDs.
-   **Lambda Function** → Deployed inline using Node.js, connected with DynamoDB.
-   **API Gateway** → Configured as trigger for Lambda with ANY method.
-   **S3 Bucket** → Hosted static HTML frontend (enabled public access + static website hosting).
-   **CloudFront** → Added distribution for HTTPS + global access to S3 content.

---

### 📸 Screenshots

-   Lambda console with inline code
-   API Gateway trigger connected to Lambda
-   Successful test response (Item stored successfully!)
-   DynamoDB table showing stored records
-   S3 static website hosting screen
-   CloudFront distribution settings
-   Final browser view of the web app

---

### 📆 Folder Structure

serverless-webapp/
├── screenshots/          # AWS console screenshots
├── README.md             # Project documentation

---

### 💡 Learnings & Outcomes

-   ✅ Designed and deployed a **serverless architecture** entirely from AWS console
-   ✅ Integrated **Lambda + DynamoDB** for persistence
-   ✅ Used **API Gateway** to expose serverless functions
-   ✅ Hosted and distributed static frontend using **S3 + CloudFront**
-   ✅ Practiced IAM roles, permissions, and service integrations

---

### 👤 Author

-   Arnav Deshmukh
-   GitHub: [arnavdeshmukh23](https://github.com/arnavdeshmukh23)
-   LinkedIn: [linkedin.com/in/arnav-deshmukh-7984781bb](https://www.linkedin.com/in/arnav-deshmukh-7984781bb)

---

⭐ Star this repo if you found the project helpful!
