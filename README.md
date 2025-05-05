# API Postman Newman Integration

This repository demonstrates how to use **Postman**, **Newman**, and **Swagger** for API testing, automation.

---

## 📚 Content

- [🚀 Getting Started](#-getting-started)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Install Dependencies](#2-install-dependencies)
  - [3. Run Tests with Newman](#3-run-tests-with-newman)
- [📄 Test Report](#-test-report)
- [📂 Project Structure](#-project-structure)
- [📜 Scripts](#-scripts)
- [🧾 .gitignore](#-gitignore)

---

## 🚀 Getting Started

#### 1. Clone the Repository

```bash
git clone https://github.com/OlyaSkr/api-postman-newman.git
```

#### 2. Install dependencies:

```bash
npm install
```

#### 3. Run tests with Newman:

```bash
npm run test:api
```

## 📄 Test Report

After running the tests, a detailed HTML report will be generated here:

```bash
./report/report.html
```

## 📁 Project Structure

```pgsql

api-postman-newman-actions/
├── .github/workflows/                  # GitHub Actions CI configuration
├── report/                             # HTML test reports
├── swagger.user.postman_collection.json  # Postman collection file
├── swagger.user.postman_globals.json     # Postman globals
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
```

## 📜 Scripts

In package.json:

```json
"scripts": {
  "test:api": "npx newman run swagger.user.postman_collection.json -r cli,htmlextra --reporter-htmlextra-export ./report/report.html --globals swagger.user.postman_globals.json"
}
```

## 🧾 .gitignore

Make sure the report/ folder is excluded from Git:

```bash
# .gitignore
report/
```
