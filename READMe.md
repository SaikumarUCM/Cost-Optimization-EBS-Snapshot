# 🧹 AWS EBS Snapshot Cleanup Lambda

This project contains an AWS Lambda function written in Python using **boto3** that automatically identifies and deletes **unused EBS snapshots**. These are snapshots that are either:

- Not associated with any **EBS volume**
- Associated with **volumes that are no longer attached to any EC2 instance**
- Associated with **volumes that have been deleted**

By regularly cleaning up these snapshots, you can reduce unnecessary storage costs in your AWS account.

---

## 📁 Project Structure

```bash
.
├── handler.py          # Main Lambda function logic
├── requirements.txt    # Python dependencies
└── serverless.yml      # (Optional) Serverless Framework config for deployment
