# **What is CI/CD?**

- It helps us build, test, and release software applications much faster and much more reliably.

**Continuous Integration** 
---
- The practice of automatically **integrating code changes frequently,** allows for automatic + continuous checks for errors, reducing big messy merges

**Continuous Deployment/Delivery** 
---
- **Continuous Delivery:** Code is built/changed and tested and is ready for **manual deployment** if it passes checks 

- **Continuous Deployment:** Code is built/changed and tested and **automatically deployed** if it passes checks 

**How does it work?**
---
**1. Code Commit**

- A developer makes changes to the code. The changes are committed and pushed to the repository.

**2. Build Trigger**

- That commit automatically triggers the pipeline.

**3. Build**

- The code is compiled (converted into something the computer understands). 

- All required dependencies are assembled through libraries/frameworks 

- The team is notified whether the build succeeds or fails.

- *“Build” simply means: Turning your written code into something that can actually run and be deployed.*

**4. Automated Testing**

- Automated tests run to make sure the new changes don’t break existing features. Test results are shared with the team.

**5. Staging Deployment**

- If tests pass, the build is deployed to a staging environment. This is used for further testing and validation.

**6. Production Deployment**

- Once everything looks good, the code is deployed to production. Users can now access the new changes.

**Why CI/CD Is Important**
---

- **Fast delivery:** Automation lets teams release features and fixes much faster.

- **Better quality:** Bugs are caught early through continuous testing.

- **Reduced risk:** Small, frequent changes are easier and safer to deploy.

- **Better collaboration:** Frequent integration means fewer conflicts and better teamwork.


