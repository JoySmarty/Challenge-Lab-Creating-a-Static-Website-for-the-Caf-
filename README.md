# Challenge-Lab-Creating-a-Static-Website-for-the-Cafe

# ☕ Café Website on AWS S3 — Static Hosting, Data Protection & Disaster Recovery

## 📖 Project Overview
This project was built as part of an AWS **Challenge Lab** to design a **static website architecture** using **Amazon S3**.  

The scenario revolves around **Frank and Martha**, a couple who run a cozy café known for their pastries and coffee. Their daughter **Sofía** realized that despite the café’s great reputation, they lacked online visibility.  

To help, I stepped in to create a **simple and cost-effective website** hosted entirely on AWS — demonstrating how even small businesses can adopt **cloud technology** for visibility, reliability, and scalability.

---

## ☁️ Architecture Summary

### 🧩 1. Static Website Hosting
- Created an **S3 bucket** in `us-east-1` for website hosting.
- Uploaded `index.html` and an `/images` folder.
- Configured **static website hosting** and enabled **public read access** via a **bucket policy**.
  

### 🔐 2. Data Protection with Versioning
- Enabled **S3 Versioning** to prevent accidental overwrite or deletion of files.
- Verified version history by uploading multiple versions of the `index.html` file.

### 💰 3. Cost Optimization with Lifecycle Policies
- Configured two lifecycle rules:
  - Move older versions to **S3 Standard-IA** after 30 days.
  - **Delete** previous versions after 365 days to save storage costs.

### 🌍 4. Disaster Recovery with Cross-Region Replication (CRR)
- Created a **destination bucket** in another AWS Region.
- Enabled **Cross-Region Replication** to automatically copy files from the source bucket.
- Used the **CafeRole IAM role** to grant S3 permissions for replication.
- Confirmed new uploads replicated successfully while deleted versions remained in the DR bucket.

---

## 🧪 Testing & Validation
- Opened the **S3 website endpoint URL** to confirm the website loaded correctly.
- Verified that versioning worked by checking **“Show versions”** in S3.
- Confirmed lifecycle rules were active.
- Uploaded an updated `index.html` and confirmed replication to the second bucket.

---

## 🧠 Key Takeaways
- Amazon S3 is powerful enough to **host static websites** securely and affordably.
- **Versioning** + **Lifecycle rules** ensure data protection and cost efficiency.
- **Cross-Region Replication** provides a simple yet effective **disaster recovery** setup.
- This architecture is a great starting point for **small businesses** wanting to adopt cloud technologies.

---

## 🛠️ AWS Services Used
- **Amazon S3** – Storage, hosting, versioning, lifecycle, replication  
- **AWS IAM** – Permissions for replication roles  
- **CloudWatch Logs** – Monitoring and tracking activity  

---

## 🚀 Future Improvements
- Integrate **Amazon Route 53** for a custom domain.
- Add **Amazon CloudFront** for global content delivery and caching.
- Automate setup with **Terraform** or **AWS CLI scripts**.
- Add a **contact form** using AWS Lambda and Amazon API Gateway.

---

## 👩🏽‍💻 Author
**Joy Imarah**  
_Cloud & DevOps Enthusiast | AWS Learner_  
📍 Nigeria  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/joy-imarah-382b06260)  

---

### ⭐ If you found this project useful, please star the repo!

