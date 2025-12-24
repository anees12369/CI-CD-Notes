# **Secrets & Encrypted Variables**

**What are GitHub Actions secrets?**
---
- Secrets are encrypted variables used to store sensitive data, such as: **API keys, Passwords, Access tokens, Database credentials**

- Secrets keep sensitive data **out of GitHub, out of logs, and out of commits.**

- Don’t: Print secrets, Commit secrets, Use secrets in client-side code, Hardcode credentials

- You can create secrets on GitHub within you repo and then reference it in your workflow 