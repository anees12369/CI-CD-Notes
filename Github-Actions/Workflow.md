# **GitHub Actions CI/CD Workflow**

- **Write Code:** Developers write new features or fix bugs in the codebase.

- **Commit Code:** Changes are committed to the GitHub repository. This triggers **a GitHub Actions workflow.**

- **GitHub Actions Workflow:** Defined in a **YAML file** in the repo. Specifies what actions to run when certain events (like commits) occur. 

**Common Use Cases for GitHub Actions**
---

**1. Continuous Integration (CI)**

- Automatically **builds and tests code, catches bugs early** and keeps the codebase stable, whenever changes are pushed 

- Example: Run **unit tests on every pull request** to ensure new code doesn’t break existing features.

**2. Continuous Deployment (CD)**

- Automatically deploys code after all tests pass. Reduces manual work and speeds up releases.

- Example: Deploy a web app to AWS, Azure, or GCP after successful tests.

**3. Workflow Automation**

- Automates repetitive tasks **beyond build and deployment.** Saves time and keeps projects organized.

- Example: Automatically moving issues or pull request cards on a GitHub project board.
 