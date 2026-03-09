1️⃣ The Problem This Project Solves

In real companies, there may be hundreds or thousands of EC2 instances.

Each instance must have tags like:

Environment = Production
Environment = Dev
Environment = Test

Tags are important because they help with:

💰 Cost tracking (which team is using resources)

🔒 Security policies

📊 Monitoring and automation

🏢 Resource organization

Example
Instance	Environment Tag
i-101	Production
i-102	Dev
i-103	❌ Missing

If someone forgets to add the tag, it causes problems like:

Billing confusion

Automation failures

Governance issues

So companies want a system that automatically checks for missing tags.

2️⃣ The Goal of This Project

The project automatically detects EC2 instances missing the "Environment" tag and sends an alert.

Instead of a human checking manually.

3️⃣ The Architecture (Big Picture)
EC2 Instances
     │
     ▼
AWS Lambda Function
(check tags)
     │
     ▼
If tag missing
     │
     ▼
SNS Topic
     │
     ▼
Email Notification
