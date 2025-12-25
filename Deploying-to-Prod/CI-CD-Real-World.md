# **CI/CD in the real-world**

![alt text](../Screenshots/image-6.png)

**Automated testing and linting**
---
- **Linting and automated testing** help us catch errors early and keep our codebase clean and reliable.

- **Linting:** A process of analyzing your code for any **syntax errors, bugs, and deviations,** it's like having a spell checker for your code. 

- **Automated testing:** The practice of running tests on your codebase automatically to ensure it works as expected. It involves writing test cases/apps that **verify different parts of your code** and running these tests automatically every time you make changes to the code. (e.g. python unittests)

- **Tools:** ESLint, PyLint, Unittest, Pytest etc 

![alt text](../Screenshots/image-7.png)

**Deploying to different environments**
---
- When working in a real environment, we typically deploy to 3 or 4 environments: **Development, Staging, and Production.**

- **Can be done in two ways:** **Manual** (moving code manually between environments) or **Automated** (uses scripts and tools to move code between environments)

- Automated = **faster, more reliable and less prone to human error**

- **Tools to manage deployment:** AWS, Azure. GCP

![alt text](../Screenshots/image-8.png)

**Best Practices for Secure Pipelines**
---
- **Secure your secrets:** Never hard-code sensitive information like **API keys, passwords, or tokens in your code.** Use GitHub Secrets or dedicated secret-management tools to store and access them securely, preventing accidental exposure.

- **Control access:** Apply the principle of least privilege by giving users **only the permissions they need.** Use role-based access control (RBAC) to reduce the risk of unauthorized access or accidental changes.

- **Scan for vulnerabilities:** Regularly scan your code and dependencies using tools like **Dependabot, Snyk, or similar security scanners.** Catching vulnerabilities early helps prevent security breaches.

- **Audit and monitor:** Enable **logging, auditing, and monitoring for your CI/CD pipelines.** Track actions, watch for suspicious behavior, and **set up alerts** so potential security incidents are detected and handled quickly.

**Common issues and solutions** 
---
**Common issues:**

- **Failed tests:** Tests may fail due to code issues or unexpected behavior, review the failing test and related code.

- **Dependency errors:** Caused by missing, outdated, or conflicting libraries and packages.

- **Configuration errors:** Often due to syntax mistakes in pipeline files (e.g., YAML indentation, spacing, or typos).

- **Permission issues:** Occur when workflows lack access to required resources, secrets, or directories.

**Common solutions:**

- **Review logs:** Logs are the first place to look, as they usually point directly to the root cause.

- **Rerun jobs:** Helps determine whether the issue was a temporary (transient) failure or a consistent problem.

- **Update dependencies:** Keeping dependencies up to date can resolve compatibility and conflict issues.

- **Verify configuration:** Double-check pipeline syntax, environment variables, and secrets to ensure everything is correctly set.
