## **Module Checklist \- CI/CD with GitHub Actions**

### **What You Should Know by Now**

* **CI/CD fundamentals:** Continuous Integration (frequent code merging) combined with Continuous Deployment/Delivery (automated releases) forms the backbone of modern DevOps workflows  
* **CI/CD benefits:** Faster delivery, improved quality, reduced risks, stronger collaboration, and reliable automation of testing and deployments  
* **DevOps pipeline stages:** Source control → CI/CD → Monitoring and Logging, with feedback loops ensuring continuous improvement  
* **GitHub Actions basics:** Integrated CI/CD platform within GitHub, uses YAML-based workflows and a marketplace of pre-built reusable actions  
* **Workflow structure:** Defined by `name`, `on` (triggers), `jobs`, and `steps` — stored under `.github/workflows/`  
* **Common triggers:**  
  * `on: push` → runs on commits  
  * `on: pull_request` → runs on PR creation or update  
  * `on: schedule` → runs at set intervals using cron syntax  
* **Job configuration:** Define environments with `runs-on: ubuntu-latest`, `windows-latest`, or `macos-latest`; jobs run in parallel unless configured otherwise  
* **Essential steps:**  
  * `actions/checkout@v2` → checks out the repository  
  * `actions/setup-python@v2` (or Node.js/Java) → sets up runtime environments  
* **YAML syntax:** Uses key-value pairs, `-` for lists, indentation for hierarchy, and `#` for comments  
* **Events, jobs, steps:** Events trigger workflows; jobs group related steps, and steps execute sequentially within each job

**Matrix builds:**  
Use a matrix strategy to test across multiple configurations:

 `strategy:`  
  `matrix:`  
    `python-version: [3.7, 3.8, 3.9]`

* **Conditionals:** Use `if: success()` to run steps only after success, or `if: failure()` for error-handling steps  
* **Expressions:** Access workflow context with `${{ github.ref }}` or matrix values with `${{ matrix.python-version }}`  
* **Secrets management:** Store credentials under *Settings → Secrets*, access with `${{ secrets.SECRET_NAME }}`  
* **Environment variables:** Define globally with `env:` and access via `$MY_VAR` or `${{ env.MY_VAR }}`  
* **Manual triggers:** Add `workflow_dispatch:` to run workflows manually with custom input parameters  
* **Custom actions:** Build reusable logic with JavaScript, Docker, or composite actions to standardise workflows  
* **Action publishing:** Create an `action.yml` file to document metadata and publish on the GitHub Marketplace  
* **Real-world practices:** Automate tests, linting, security scans, and deploy to multiple environments seamlessly  
* **Security best practices:** Avoid hardcoding secrets, follow least privilege access, and regularly scan for vulnerabilities  
* **Debugging workflows:** Inspect logs, rerun failed jobs, and use `set -x` in bash for detailed debugging output  
* **Common issues:** Permission errors, dependency conflicts, YAML syntax mistakes, or timeouts from long-running jobs  
* **Docker integration:** Automate Docker image builds, authenticate with registries, and use multi-stage builds for efficiency  
* **Deployment strategies:** Deploy to staging or production using blue-green, rolling, or canary deployment models

### **Try This Before Moving On**

* **Repository setup:** Create a GitHub repository, add a `.github/workflows/` folder, and build a simple “Hello World” workflow  
* **Python CI pipeline:** Implement a workflow that checks out code, installs dependencies, and runs automated tests  
* **Matrix strategy:** Test across Python versions 3.7–3.9 using a matrix configuration to ensure compatibility  
* **Secrets configuration:** Add Docker Hub credentials in *Settings → Secrets* and use them for automated Docker authentication  
* **Manual workflow:** Create a workflow with `workflow_dispatch` to manually trigger builds for different environments  
* **Custom action creation:** Develop a small JavaScript-based custom action, publish it to a separate repository, and reference it  
* **Docker automation:** Configure a workflow to build and push Docker images to Docker Hub on every `main` branch commit  
* **Error handling:** Intentionally break workflows to practise debugging, fix syntax and permission issues  
* **Conditional logic:** Add `if:` statements to ensure deployment only occurs when tests pass or on specific branches  
* **Real-world project:** Build a full CI/CD pipeline that runs tests, builds images, and deploys to staging or production environments  
* **Bonus practice:** Complete OverTheWire *Bandit* challenges to strengthen your Linux and automation command skills

### **Next Steps**

* **Master advanced CI/CD:** You’re ready to explore enterprise-grade CI/CD pipelines, dynamic environments, and automated infrastructure provisioning  
* **Apply to real projects:** Implement CI/CD across all your applications — automated testing and deployments are now industry standards  
* **Integrate with cloud platforms:** Combine GitHub Actions with AWS, Azure, or GCP to automate complete DevOps pipelines  
* **Build your DevOps portfolio:** Showcase CI/CD projects that demonstrate reliability, scalability, and automation proficiency  
* **Prepare for senior roles:** Strong automation skills distinguish senior DevOps engineers \- you’re now building that expertise