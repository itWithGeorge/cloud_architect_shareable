# GCP Backend — Firebase + Express + AI

[![Cloud](https://img.shields.io/badge/Cloud-Google%20Cloud-4285F4.svg)](#)
[![Backend](https://img.shields.io/badge/Backend-Firebase%20%7C%20Express%20(Node.js)-10B981.svg)](#)
[![Messaging](https://img.shields.io/badge/Messaging-Pub%2FSub%20%7C%20Scheduler-6366F1.svg)](#)
[![AI](https://img.shields.io/badge/AI-Rule--based%20%2B%20LLM%20gateway-111827.svg)](#)

> **FE stack:** SEO‑friendly **WordPress** + fully customizable, cross‑platform **Flutter** apps.  
> **BE focus:** Firebase‑centric with a large **Express** app for business logic and automation.

---

## 🗺️ Architecture (at a glance)
![GCP backend architecture](./gcp_be_snufi.pdf)

- **Firebase Auth** for users and admins; **Firestore** as the operational DB; **Cloud Storage** for assets.
- **Cloud Functions (Node.js + Express)** host core domain logic:
  - custom **rule‑based AI** (domain heuristics),
  - **unified LLM gateway** (Gemini / OpenAI / Anthropic) for *privileged* users.
- **Pub/Sub** for async tasks and cross‑service decoupling.
- **Cloud Scheduler** (cron) triggers marketing & ops jobs (reminders, market analyses).
- **GA4 + Looker Studio** for product & marketing analytics.
- **Twilio / SendGrid** for marketing campaigns (SMS / email).

---

## 🔑 What this backend delivers
- **Decision speed:** near‑real‑time events via Pub/Sub and Functions.
- **Flexibility:** Express routes centralize complex business rules in one codebase.
- **Governance:** role‑gated access to LLM features; logs/metrics for auditability.
- **Portability:** clients = WordPress site, Flutter web/admin, and Flutter mobile.

---

## 🔐 External API (historical note)
The API was exposed to **paying customers via AWS API Gateway**. With the rise of LLM usage, these **public endpoints were shut down**. The system now prioritizes **first‑party** access and gated features.

---

## 📬 Contact
For further information reach out via email/LinkedIn.