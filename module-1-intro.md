# 📘 Module 1: Introduction to GitHub Actions

This folder contains notes and resources from **Module 1** of the **GitHub Actions Bootcamp** by [CódigoFacilito](https://codigofacilito.com/), taught by **@eduardo_gpg**.  
The module introduces the core concepts, structure, and use cases of GitHub Actions.

> 🗒️ *Note: Content was delivered in Spanish — summaries are written in English, but some files or examples may remain in Spanish.*

---

## 🧠 What Is GitHub Actions?

GitHub Actions is a CI/CD and automation tool that enables you to define custom workflows triggered by repository events.  
It helps automate tasks such as:

- ✅ Continuous Integration (CI)
- 🚀 Continuous Deployment (CD)
- 🧪 Automated testing
- 📦 Builds
- 🔔 Notifications
- 🔐 Security scanning

---

## 🧱 Key Concepts Introduced

### 🔁 **Workflows**
- Defined in `.yml` files inside `.github/workflows/`
- Describe the automation process

### ⚡ **Triggers**
- Events that initiate a workflow
- Declared using `on:`
  - Examples: `push`, `pull_request`, `merge`

### ⚙️ **Jobs**
- Independent units of work
- Run in parallel by default
- Defined using `jobs:`
- Each job runs on a **runner**

### 📋 **Steps**
- Tasks within a job (run sequentially)
- Can use shell commands or actions (`run` or `uses`)
- Can access environment variables

### 🖥️ **Runners**
- Virtual environments where jobs run
- GitHub provides managed runners:
  - `ubuntu-latest`, `windows-latest`, `macos-latest`
- Set using `runs-on`

---

## 🎯 Advantages of GitHub Actions

- Free for public repositories  
- No external CI/CD setup required  
- Integrated directly with GitHub  
- Vast library of reusable actions (10,000+)  
- Supports flexible, scalable automation

---

## 🧪 Example Workflow

```yaml
name: Hello World

on: [push]

jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
      - name: Say hello
        run: echo "Hello, GitHub Actions!"
