### GitHub Repository Description

---

# 🌟 Responsive E-Commerce Website with Docker & EKS 🚀

## Overview

Transform your e-commerce vision into reality! This project demonstrates how to create a responsive e-commerce website using Amazon Linux, Docker, and Kubernetes, with seamless integration into AWS services such as S3, ECR, and EKS. Deploy your site on an EKS cluster with NGINX and make it accessible via a Load Balancer. 🌐

## Objective

✨ **Build & Deploy** a fully functional e-commerce website featuring:
- 📱 **Responsive Design**: Perfect for all devices
- 🖼️ **AWS S3**: Store and serve your images
- 🐳 **Docker**: Containerize your application
- 🛠️ **AWS EKS**: Scale and manage your deployment
- 🌍 **Load Balancer**: Publicly accessible website

## Architecture Flow

1. **Amazon Linux**: 
   - Set up Docker
   - Create a project directory with `index.html` and other assets 🖥️

2. **AWS S3**: 
   - Create an S3 bucket
   - Upload images and update `index.html` with S3 URLs 🏞️

3. **Docker**: 
   - Build a custom Docker image
   - Push the image to Amazon ECR 📦

4. **Amazon ECR**: 
   - Manage and store your Docker image in ECR 🗂️

5. **Amazon EKS**: 
   - Deploy the Docker image on an EKS cluster with EC2 instances 🌟

6. **NGINX**: 
   - Serve the website using NGINX deployed via Kubernetes 🚀

7. **Load Balancer**: 
   - Expose the website and access it through a public URL 🌐

## Detailed Steps

### 1. Setting Up the Project on Amazon Linux

- Launch an EC2 instance with Amazon Linux
- Install Docker and tools
- Create a project directory:
  ```bash
  mkdir ~/PROJECT
  cd ~/PROJECT
  ```
- Add content to `index.html` and link images to S3 URLs 🖼️

### 2. Uploading Images to S3

- Create an S3 bucket via the AWS Console
- Upload your images
- Update `index.html` with the S3 URLs 📂

### 3. Creating a Dockerfile

- Create a `Dockerfile` in your project directory
- Build the Docker image:
  ```bash
  docker build -t my-website .
  ```
- Test the container with a public IP 🧪

### 4. Pushing the Docker Image to Amazon ECR

- Authenticate Docker to ECR:
  ```bash
  aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <account_id>.dkr.ecr.<region>.amazonaws.com
  ```
- Create a repository in ECR
- Tag and push your Docker image:
  ```bash
  docker tag my-website:latest <account_id>.dkr.ecr.<region>.amazonaws.com/my-website:latest
  docker push <account_id>.dkr.ecr.<region>.amazonaws.com/my-website:latest
  ```

## Deployment

- Deploy the Docker image on Amazon EKS
- Use NGINX for web serving via Kubernetes
- Access your website through a Load Balancer 🌐

