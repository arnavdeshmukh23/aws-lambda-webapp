# 🌐 Serverless Web Application with AWS Lambda & DynamoDB  

This project demonstrates building a **completely serverless web application** using **AWS Lambda**, **API Gateway**, and **DynamoDB**, with static frontend hosting on **S3 + CloudFront**. The application scales automatically without managing any servers, providing a cost-efficient and highly available architecture.  

---

## 📌 Project Overview  

| Task                | Description |
|---------------------|-------------|
| ☁️ Compute          | **AWS Lambda** (Node.js/Python functions) |
| 🔗 API Layer        | **Amazon API Gateway** (REST endpoints) |
| 🗄️ Database         | **DynamoDB** (NoSQL database for persistence) |
| 🖼️ Frontend         | Static web hosting on **S3 + CloudFront** |
| ⚙️ Infrastructure   | Provisioned using **Terraform / SAM** |
| 🔍 Monitoring       | **CloudWatch** logs & metrics |

---

## 🛠️ Technologies Used  

- **AWS Lambda** – Serverless compute  
- **Amazon API Gateway** – REST API endpoints  
- **Amazon DynamoDB** – Scalable NoSQL database  
- **Amazon S3** – Static site hosting  
- **Amazon CloudFront** – CDN for global delivery  
- **Terraform / AWS SAM** – Infrastructure as Code  
- **CloudWatch** – Logging and monitoring  

---

## 🚀 Architecture  

1. **Frontend**: Static HTML/JS website hosted on **S3 + CloudFront**.  
2. **API Layer**: **API Gateway** routes client requests to Lambda.  
3. **Backend Logic**: **AWS Lambda** functions handle business logic.  
4. **Database**: **DynamoDB** stores and retrieves persistent data.  
5. **Monitoring**: **CloudWatch** captures logs, metrics, and triggers alerts.  

---

## 📂 Folder Structure  

serverless-web-app/
├── backend/               # Lambda function code
│   ├── handler.js         # Main Lambda handler
│   ├── package.json       # Dependencies
│   └── node_modules/      # Installed packages
├── infrastructure/        # IaC (Terraform / SAM templates)
│   └── main.tf
├── api/                   # API Gateway definitions
│   └── api-gateway.yaml
├── database/              # DynamoDB schema or seed scripts
│   └── schema.json
├── frontend/              # Static website (HTML, CSS, JS)
│   └── index.html
├── screenshots/           # Architecture diagrams / test outputs
├── README.md              # Full project documentation

---

## 🧩 Workflow  

1. User accesses the **frontend** hosted on **S3 + CloudFront**.  
2. Requests are sent to **API Gateway**.  
3. API Gateway triggers the **Lambda** function.  
4. Lambda queries **DynamoDB** for data persistence.  
5. Response is sent back to the client.  

---

## 💡 Learnings & Outcomes  

- ✅ Designed and deployed a **serverless architecture**  
- ✅ Automated provisioning with **Infrastructure as Code**  
- ✅ Connected Lambda with DynamoDB for persistence  
- ✅ Used CloudFront + S3 for global static hosting  
- ✅ Learned best practices for **monitoring and logging** with CloudWatch  

---

## 👤 Author  

**Arnav Deshmukh**  
GitHub: [arnavdeshmukh23](https://github.com/arnavdeshmukh23)  
LinkedIn: [linkedin.com/in/arnav-deshmukh-7984781bb](https://www.linkedin.com/in/arnav-deshmukh-7984781bb)  

---

✨ *Star this repo if you found the project helpful or insightful!*  
