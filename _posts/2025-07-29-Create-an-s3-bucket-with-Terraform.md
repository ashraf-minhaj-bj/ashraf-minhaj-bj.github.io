---
layout: post
title: "Create an S3 Bucket with Terraform"
date: 2025-07-29
thumbnail: /assets/img/s3-bucket-thumb.png
---

# 🚀 Create an S3 Bucket with Terraform

This example demonstrates how to create a basic Amazon S3 bucket using Terraform.

---

## 🛠 Prerequisites

- Terraform installed (>= 1.0)
- AWS CLI configured (`aws configure`)
- IAM user/role with permission to manage S3

---

## 📁 Files

```
├── main.tf
└── README.md
```

### The Terraform Code

main.tf file -
```terraform

---

## 📜 main.tf

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_s3_bucket" "my_bucket" {
  bucket = "my-unique-bucket-name-123456" # Replace with a unique name
  acl    = "private"
}
```

### Steps to deploy

```bash
# Initialize Terraform
terraform init

# Preview the changes
terraform plan

# Apply the changes
terraform apply
```
