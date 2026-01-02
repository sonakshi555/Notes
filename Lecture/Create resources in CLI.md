Here's how to create AWS resources using the **AWS CLI**:

AWS interface open security credentials in account settings, their open create access key
you will get Access key ID and secret Access key

## 1. First, Configure AWS CLI (One-time setup)

```bash
aws configure  # in command prompt
```

Enter:

- **AWS Access Key ID:** (from IAM user)
- **AWS Secret Access Key:** (from IAM user)
- **Default region:** (e.g., `us-east-1`, `ap-south-1`)
- **Default output format:** `json` (or `table`, `text`)

## 2. Common Resource Creation Commands

### **Create S3 Bucket:**

```bash
aws s3 mb s3://your-unique-bucket-name --region us-east-1
```

### **Create EC2 Instance:**

```bash
aws ec2 run-instances --image-id ami-12345678 --instance-type t2.micro --key-name your-key-pair --security-group-ids sg-123456 --subnet-id subnet-123456
```

### **Create IAM User:**

```bash
aws iam create-user --user-name new-username
```

### **Create Security Group:**

```bash
aws ec2 create-security-group --group-name my-sg --description "My security group" --vpc-id vpc-123456
```

### **Create DynamoDB Table:**

```bash
aws dynamodb create-table --table-name MyTable --attribute-definitions AttributeName=ID,AttributeType=S --key-schema AttributeName=ID,KeyType=HASH --billing-mode PAY_PER_REQUEST
```

### **Upload File to S3:**

```bash
aws s3 cp myfile.txt s3://your-bucket-name/
```

### **Create RDS Database:**

```bash
aws rds create-db-instance --db-instance-identifier mydb --db-instance-class db.t3.micro --engine mysql --master-username admin --master-user-password mypassword --allocated-storage 20
```

## 3. Verify Your CLI Setup

Test if AWS CLI is working:

```bash
aws sts get-caller-identity
```

This shows your AWS account details if configured correctly.

## 4. Get Help for Any Command

```bash
aws <service> <command> help

# Examples:
aws s3 help
aws ec2 run-instances help
```

## Tips:

- Run these commands in **Windows Command Prompt** if managing AWS from your local machine
- Use `--region` flag to specify region if different from default
- Many commands return JSON output with resource IDs you'll need for further operations

What specific resource would you like to create? I can give you the exact command!