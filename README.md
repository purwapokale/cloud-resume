# ☁️ AWS Cloud Resume Challenge

Live Website: http://resume-purwa-2026.s3-website.ap-south-1.amazonaws.com

## 📖 About The Project
This project is a Serverless Cloud Resume website deployed on AWS. It demonstrates a full-stack cloud application using Infrastructure as a Service (IaaS) and Platform as a Service (PaaS) offerings.

Unlike a traditional resume, this project integrates a **Visitor Counter** that tracks how many people have viewed the site in real-time.

## 🏗️ Architecture
The application is built using a serverless microservices architecture:
* **Frontend:** HTML5, CSS3, JavaScript (Hosted on **AWS S3** with Static Website Hosting).
* **Backend:** Python 3.12 (Executed on **AWS Lambda**).
* **Database:** NoSQL Database (**AWS DynamoDB**) to store visitor counts atomically.
* **API:** RESTful API exposed via **AWS API Gateway** to bridge frontend and backend.
* **CI/CD:** Automated deployment pipeline using **GitHub Actions**.
* **Version Control:** Git & GitHub.

## 🚀 How It Works
1.  **Frontend:** The static website is stored in an S3 bucket.
2.  **Visitor Count:** When the page loads, a JavaScript function triggers an API call.
3.  **API Gateway:** Receives the request and securely triggers the Lambda function.
4.  **Lambda:** Retrieves the current count from DynamoDB, increments it, updates the database, and returns the new count to the frontend.
5.  **Automation:** Any change pushed to the `main` branch on GitHub automatically triggers a workflow that syncs the latest code to the S3 bucket.

## 🛠️ Tech Stack
| Component | Technology |
|-----------|------------|
| **Cloud Provider** | AWS (Amazon Web Services) |
| **Frontend** | HTML, CSS, JavaScript |
| **Compute** | AWS Lambda (Serverless) |
| **Database** | Amazon DynamoDB |
| **API** | Amazon API Gateway |
| **Storage** | Amazon S3 |
| **CI/CD** | GitHub Actions |

## 🎯 Key Learnings
* Configuring **AWS S3** for static hosting and bucket policies.
* Writing **Python** scripts for Lambda to interact with DynamoDB (boto3).
* Setting up **API Gateway** with CORS configurations.
* Implementing **CI/CD pipelines** to automate cloud deployments.
* Resolving **CORS** and permission issues between microservices.

---
*Built with ❤️ by Purwa Pokale*
