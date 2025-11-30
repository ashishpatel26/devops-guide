# AWS CLI Cheat Sheet

The AWS CLI allows you to manage AWS services from the command line.

## Configuration

```bash
aws configure
```

You will be prompted for:
*   AWS Access Key ID
*   AWS Secret Access Key
*   Default region name (e.g., us-east-1)
*   Default output format (json)

## Common Commands

### S3 (Simple Storage Service)

```bash
# List buckets
aws s3 ls

# Copy file to bucket
aws s3 cp myfile.txt s3://my-bucket/

# Sync directory
aws s3 sync ./local-folder s3://my-bucket/
```

### EC2 (Elastic Compute Cloud)

```bash
# List instances
aws ec2 describe-instances

# Start an instance
aws ec2 start-instances --instance-ids i-1234567890abcdef0

# Stop an instance
aws ec2 stop-instances --instance-ids i-1234567890abcdef0
```