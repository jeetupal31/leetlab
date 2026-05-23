# LeetLab — Competitive Coding Platform

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

> A LeetCode-style competitive coding platform where users can browse problems, write solutions in the browser, run test cases, and track their progress — built full-stack from scratch.

## Features

- 📝 **Problem library** — curated list of DSA problems with difficulty tags (Easy / Medium / Hard)
- 💻 **In-browser code editor** — write, run and test solutions without leaving the page
- ✅ **Auto-judge** — submit your solution and see pass/fail per test case instantly
- 📊 **Progress tracking** — solved / attempted count per user
- 🔐 **User accounts** — signup, signin, personal dashboard
- 🏷️ **Tag filtering** — filter problems by topic (Arrays, Trees, DP, Graphs…)

## Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | React, Monaco Editor (VS Code engine) |
| Backend | Node.js, Express |
| Database | MongoDB + Mongoose |
| Auth | JWT, bcrypt |
| Code Execution | Sandboxed Node.js eval / Judge0 API |

## System Design

```
User submits code
      │
  POST /submit
      │
  Judge Service
  ├── Runs code against test cases
  ├── Captures stdout / stderr
  └── Returns verdict (AC / WA / TLE)
      │
  Save result to DB
      │
  Update user progress
```

## Local Setup

```bash
git clone https://github.com/jeetupal31/leetlab.git
cd leetlab
npm install

# Set env vars
cp .env.example .env   # add MONGO_URI, JWT_SECRET

npm run dev
```

---

Made by [Jeetu Pal](https://github.com/jeetupal31)
