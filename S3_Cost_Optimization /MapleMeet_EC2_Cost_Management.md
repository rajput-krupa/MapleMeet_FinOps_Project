🧭 Context: Maple Meet + EC2
Maple Meet is hosting a simple web platform for event booking. You created an EC2 instance to host that site.

But just launching an EC2 instance isn’t enough. In a real company, we need to:

🔹 Know how much it’s costing
🔹 Know if we’re wasting money
🔹 Know how to optimize it smartly
🔹 Monitor it daily
🔹 Document and report our cost-saving efforts

✅ EC2 FinOps Step-by-Step (Hands-On + Finance)


🟦 STEP 1: Check EC2 Cost in AWS Cost Explorer
🧠 Why? Before optimizing, measure how much your EC2 is costing.

🔧 What to Do:
Go to AWS Console → Cost Explorer

Select “Service” view

Filter by EC2: Running Hours, EC2-Other

Set date range: last 7 days

Note down:

Hourly usage pattern

Region

Instance type

Cost per hour (e.g. $0.0116/hour)

💡 Document this in a README.md or project report:
“EC2 t2.micro instance in us-east-1 running 24/7 costs approx. $8.35/month.”





🟦 STEP 2: Evaluate Instance Right-Sizing
🧠 Why? Maybe Maple Meet doesn’t need full compute power 24/7.

🔧 What to Do:
Go to EC2 → Monitor → CloudWatch Metrics

Check:

CPU Utilization (Is it always <10%?)
<img width="729" height="634" alt="image" src="https://github.com/user-attachments/assets/c95d3d9d-350d-486a-bbdf-ccc2b16ae512" />

Network/Storage usage

If underused:
Consider stopping during off-hours

Consider using a smaller instance (e.g., t3.nano)

Use Auto Stop Lambda or schedules (see next)

✅ FinOps value: Matching size to usage avoids overprovisioning = cost drop




🟦 STEP 3: Set Auto-Stop to Save Off-Hours Cost
Let’s say Maple Meet only needs this EC2 from 8am to 8pm (business hours). Why pay for 24 hours?

🔧 What to Do:
Go to AWS Instance Scheduler (or use Lambda + CloudWatch)
Or use this quick manual setup:

🔹 Manual Schedule (Simpler Way)

Go to CloudWatch → Rules → Create Rule

EventBridge (Scheduled)

Expression: cron(0 20 * * ? *) → stop at 8PM

Expression: cron(0 12 * * ? *) → start at 8AM

Target → EC2 instance ID → Action: Stop/Start

✅ Savings: Up to 60-70% saved if off at night/weekends



🟦 STEP 4: Use a Reserved Instance (RI) or Savings Plan (SP)
Once Maple Meet's traffic grows, it will need 24/7 uptime.

You should:

Monitor for 1 month

If always running → purchase Reserved Instance or Savings Plan

💰 RIs/SPs can save up to 72% compared to On-Demand EC2



🟦 STEP 5: Tag EC2 for Cost Allocation
🧠 Why? FinOps requires knowing which team or project owns which cost.

🔧 What to Do:
Go to EC2 → Select Instance

Click Tags

Key: Owner → Value: Krupa

Key: Project → Value: MapleMeet-Web

Key: Environment → Value: Dev / Prod

✅ Now your costs in Cost Explorer will be grouped by tags!

🟦 STEP 6: Enable Detailed Monitoring (Optional)
This allows 1-minute metrics in CloudWatch to make better cost decisions.

Go to EC2 → Monitoring tab

Enable Detailed Monitoring (note: small extra cost)




<img width="857" height="414" alt="image" src="https://github.com/user-attachments/assets/a5234f15-0c31-453a-9db5-5fcd9e86ff4c" />




