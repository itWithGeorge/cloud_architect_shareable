# Static Web Front‑End AWS

[![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-FF9900.svg)](#)

<!-- Optional hero image -->
![Architecture cover](./aws_frontend_snufi.jpg)

## 📄 Architecture Artifact (PDF)
**View the original AWS design:** 👉 [AWS FRONTEND](./aws_frontend_snufi.pdf)

---

## 📝 Summary
This architecture documents a **previous implementation on AWS** that I originally ran under an **AWS project quota**. From a **financial perspective**, for my traffic profile and feature needs, I’m now migrating the **front‑end to Google Cloud (GCP)** because **Google provides a more affordable setup** in my use‑case while preserving performance and observability.

**Goals**
- Keep the simplicity and robustness of S3 + CDN hosting.
- Maintain full **edge caching**, **TLS**, and **log analytics**.
- Reduce recurring cloud spend for the front‑end stack.

---

## 🏗️ AWS Architecture
- **Route 53** — managed DNS and public records (A/AAAA/CNAME).  
- **CloudFront** — global CDN caching static assets; origin = **S3 static website**.  
- **S3** — static site bucket (immutable assets, versioning recommended).  
- **Access & Edge Logs** — **CloudFront logs** + **S3 access logs** exported to S3; 
  queried with **Athena** for traffic analytics and pattern recognition.  
  *(See the PDF diagram for the flow: Users → Route 53 → CloudFront → S3; exports → S3 → Athena).*

**Operational notes**
- DNS lookup lands at CloudFront; **origin requests** hit S3 only on cache miss.  
- Logging is centralized for **export / analyze / pattern recognition** via Athena.  

---

## 📬 Contact
For further information reach out via email/LinkedIn.