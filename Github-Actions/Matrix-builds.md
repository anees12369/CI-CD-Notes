# **Matrix builds and Parallel Testing**

- A matrix build runs the **same job** using **different environments** (it carries out **all the steps** in the job)

- All jobs run in **parallel** across different environments 

- It is **useful for testing changes to code  across different environments.**

- e.g. Different **OS, language versions (Node, Python, Java) and configurations**

```yaml
# This is how you define the environments you want the job to run across

matrix:
  python-version: [3.8, 3.9, 3.10]

# This is how you use a matrix value

  ${{ matrix.python-version }}
```
**A simple example of a matrix build**
---
```yaml
name: Matrix Build Example

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        node-version: [16, 18, 20]

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node-version }}

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
      
# Condition that tells us if the setup and testing of the node application was successful across all different versions of node 

      - name: notify of success
        run: echo "tests passed on Node ${{ matrix.node-version }}
        if: success ()   
```

- Jobs across different environments can pass/fail independently 