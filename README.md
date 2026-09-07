# 🌐 Static Website Hosting on AWS using Amazon S3

## 📌 Project Overview

This project demonstrates how to host a **static website on Amazon S3** using HTML, CSS, and JavaScript.

The website files were uploaded to an Amazon S3 bucket, static website hosting was configured, and the required bucket permissions were set to make the website accessible through the S3 website endpoint.

This project helped me gain hands-on experience with **Amazon S3, static website hosting, bucket policies, permissions, and basic AWS cloud deployment**.

---

## 🏗️ Architecture

```text
                 Internet
                    │
                    ▼
             ┌─────────────┐
             │  Web Browser │
             └──────┬──────┘
                    │
                    ▼
          ┌─────────────────────┐
          │     Amazon S3       │
          │                     │
          │  Static Website     │
          │  Hosting            │
          │                     │
          │  ├── index.html     │
          │  ├── style.css      │
          │  └── script.js      │
          └─────────────────────┘
```

---

## ☁️ AWS Services Used

* **Amazon S3** — Storage and hosting of static website files
* **S3 Bucket Policy** — Configured access permissions for the website
* **S3 Static Website Hosting** — Enabled website hosting functionality

---

## 🛠️ Technologies Used

* HTML
* CSS
* JavaScript
* Amazon S3
* AWS IAM / S3 Permissions
* AWS Management Console

---

## 🚀 Project Implementation

### 1. Create an S3 Bucket

Created an Amazon S3 bucket to store the static website files.

The bucket was configured specifically for hosting the website.

**Screenshot:**

![S3 Bucket](screenshots/01-s3-bucket.png)

---

### 2. Upload Website Files

Uploaded the static website files to the S3 bucket.

The project contains:

```text
website/
├── index.html
├── style.css
└── script.js
```

The `index.html` file acts as the main entry point for the website.


![Uploaded Website Files](screenshots/02-uploaded-files.png)

---

### 3. Enable Static Website Hosting

Enabled **Static Website Hosting** from the S3 bucket properties.

Configured the website's index document so that Amazon S3 knows which file to serve when visitors access the website.


![Static Website Hosting](screenshots/03-static-website-hosting.png)

---

### 4. Configure Bucket Policy

Configured an S3 bucket policy to provide the required permissions for accessing the website objects.

This allowed users to retrieve the website files through the S3 website endpoint.

**Screenshot:**

![S3 Bucket Policy](screenshots/04-bucket-policy.png)

> ⚠️ **Security Note:** For production applications, public access to S3 should be carefully evaluated. Modern AWS architectures commonly use CloudFront with an appropriate S3 access configuration rather than making the bucket publicly accessible.

---

### 5. Test the Website

After completing the configuration, accessed the S3 website endpoint through a web browser and verified that the website loaded successfully.

**Screenshot:**

![Live Website](screenshots/05-live-website.png)

---

## 📂 Project Structure

```text
aws-s3-static-website/
│
├── README.md
│
├── website/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
└── screenshots/
    ├── 01-s3-bucket.png
    ├── 02-uploaded-files.png
    ├── 03-static-website-hosting.png
    ├── 04-bucket-policy.png
    └── 05-live-website.png
```

---

## 🔐 Security Considerations

During this learning project, S3 permissions were configured to allow website access.

For a production environment, I would consider a more secure architecture such as:

```text
User
  │
  ▼
CloudFront
  │
  ▼
Amazon S3
```

This can provide benefits such as:

* HTTPS
* Content caching
* Better performance
* Reduced direct access to the S3 bucket
* Improved security controls

---

## 🎯 Key Learning Outcomes

Through this project, I gained hands-on experience with:

* Creating and configuring an Amazon S3 bucket
* Uploading website files to S3
* Understanding S3 objects and bucket structure
* Enabling static website hosting
* Working with S3 bucket policies
* Understanding AWS permissions and public access
* Deploying a static website using AWS
* Accessing a hosted website through an S3 endpoint

---

## 🔮 Possible Improvements

The project could be extended by:

* Adding **Amazon CloudFront** for CDN and HTTPS
* Using **Route 53** with a custom domain
* Automating deployment using **GitHub Actions**
* Managing the infrastructure using **Terraform**
* Adding CI/CD for automatic website deployment

---

## 📸 Project Screenshots

### S3 Bucket

![S3 Bucket](screenshots/01-s3-bucket.png)

### Website Files

![Website Files](screenshots/02-uploaded-files.png)

### Static Website Hosting

![Static Website Hosting](screenshots/03-static-website-hosting.png)

### Bucket Policy

![Bucket Policy](screenshots/04-bucket-policy.png)

### Hosted Website

![Hosted Website](screenshots/05-live-website.png)

---

## 👨‍💻 About This Project

This project was created as part of my hands-on learning in **AWS and Cloud Computing**. It helped me understand the fundamentals of deploying and hosting web content using AWS services.

**Focus Areas:** AWS • Amazon S3 • Cloud Computing • Static Website Hosting • Permissions • Bucket Policies
