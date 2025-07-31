✅ STEP 2: Enable Versioning (Optional + Smart)
🎯 Goal: Prevent accidental data loss but control version bloat
🛡️ Use Case: Maple Meet might upload contracts, policies — you want backup if they get overwritten

🔧 What to Do:
Go to bucket → Properties

Enable Versioning

If using versioning, also setup a lifecycle rule to:

Expire noncurrent versions after 30 or 60 days

💡 FinOps Insight:
**Versioning = Safe but adds cost**

Expiring old versions keeps you safe + efficient
