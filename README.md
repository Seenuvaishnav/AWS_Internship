# AWS_Internship
# Task 1: Create an IAM User with Specific Permissions

## 📝 Objective

> Create an IAM user with permissions only for EC2 and S3. Attach a custom policy that allows read access to S3 and full control over EC2.

---

## ✅ Task Steps

1. Created an IAM user named **`Internship_@_nullclass`**.
2. Attached a **custom inline policy** with:
   - ✅ Full access to **EC2**
   - ✅ Read-only access to **S3**
3. Enabled **MFA (Multi-Factor Authentication)** for the user for added security.

---

## 🔐 Custom Policy JSON

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:*",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": "*"
    }
  ]
}

