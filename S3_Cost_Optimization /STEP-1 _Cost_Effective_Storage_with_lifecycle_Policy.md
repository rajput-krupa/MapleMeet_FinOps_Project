✅ STEP 1: Enable Cost-Effective Storage with Lifecycle Policies
🎯 Goal: Move old/inactive data to cheaper storage like S3 Infrequent Access or Glacier
📦 Use Case: Maple Meet stores event photos, forms, user docs. But not all data needs frequent access.

🔧 What to Do:
🔹 Create a Lifecycle Rule:
Go to your S3 bucket → Management tab
<img width="934" height="419" alt="Screenshot 2025-07-31 162951" src="https://github.com/user-attachments/assets/6cf5a4fb-6d21-498c-916b-faf6f41a7d6a" />

Click "Create lifecycle rule"
<img width="937" height="460" alt="Screenshot 2025-07-31 163004" src="https://github.com/user-attachments/assets/cdf1c46d-ebb9-4a16-8461-a3ad2043aadd" />

Name: ArchiveOldData

Choose:

Apply to all objects (or by prefix like /images/, /backups/)
<img width="917" height="786" alt="Screenshot 2025-07-31 163220" src="https://github.com/user-attachments/assets/0e86723c-45a4-475b-bedd-ac3bb572cbe0" />

Transition settings:

After 30 days → move to Infrequent Access (IA)

After 90 days → move to Glacier Deep Archive
<img width="931" height="656" alt="Screenshot 2025-07-31 163305" src="https://github.com/user-attachments/assets/2eff69f6-7e7e-4af1-b47f-c17ebdf55a1c" />


**This saves up to 80% on storage cost long-term.**



📘 Explanation:
🎉 Maple Meet might keep event images for records.

But old data doesn’t need instant access → so we optimize cost using lifecycle policies.

FinOps principle: Reduce cost without deleting useful data.

<img width="947" height="477" alt="image" src="https://github.com/user-attachments/assets/49a98197-3d5b-4de8-98d7-2fd8586a625b" />
