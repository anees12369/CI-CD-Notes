# **Conditions and Expressions in GitHub Actions**

**Conditions**
---
- control when a job or step runs by using `if:`
- The job/step will only run if the condition is **true** 

**For example**
```yaml
# Using a condition within a step 

- name: Run tests
  run: python -m unittest
  if: success() # This means: Only run this step if everything before it was successful.”
```

**Expressions**
---

- Allow you to get data (like branch name, user, event), compare values, print dynamic messages, perform calculations and control the behavior of your workflow 

- The syntax for an expression is: `${{ ... }}`

- Anything inside the `${{  }}` is an expression

**For example**
```yaml
- run: echo "Running on branch ${{ github.ref }}"
# Reads the current branch name
# Prints it in the workflow log
```

**GitHub provides built-in variables you can reference within expressions such as:**

- `github.ref` → branch or tag name
- `github.event` → event that triggered the workflow
- `github.actor` → who triggered it



