# 🛡️ Recon Board

> **A simple, private, browser-based recon workspace for security researchers and bug bounty hunters.**
> **Live site:** (https://umar1122.github.io/recon-manager/)

Recon Board helps you keep your reconnaissance work organized — **targets, scope, recon progress, notes, evidence, and findings — all in one place.**

No server. No database setup. No account required.

---

## ✨ Why I Built Recon Board

During recon, you collect a lot of small pieces of information:

- 🌐 Subdomains
- 🖥️ IP addresses
- 🔢 ASNs
- 🔗 URLs and endpoints
- 📜 JavaScript files
- 🔍 Hidden parameters
- 📁 Content discovery results
- 📝 Notes and observations
- 🐛 Security findings

It is easy to lose track of **what you already checked** and **what you discovered at each step**.

I built Recon Board to solve that problem.

Instead of having many random text files, terminal tabs, and notes, you can keep the whole recon process organized by program and by phase.

---

## 🔐 Why JSON Instead of a Database?

One of the main design decisions in Recon Board is:

### **You don't need a database.**

Your project is stored locally in your browser, and you can export everything into a **JSON file**.

Think of the JSON file as your personal project backup.

```text
Recon Board
     │
     ├── Your programs
     ├── Recon progress
     ├── Recon notes
     ├── Evidence / collected data
     └── Findings
             │
             ▼
        Export JSON
             │
             ▼
       Your own computer
```

### 💻 Your data stays local

Recon Board is designed as a local browser application. It does not need a backend server to store your recon project.

That means you don't have to create:

- ❌ MySQL database
- ❌ PostgreSQL database
- ❌ MongoDB database
- ❌ Backend server
- ❌ User account
- ❌ Cloud storage

For a personal recon tracker, this keeps the project lightweight and easy to use.

### 📦 JSON is portable

Your entire project can be exported as one JSON file.

You can keep that file on your computer, back it up, or move it to another machine.

Later:

```text
Open Recon Board
      ↓
Import JSON
      ↓
Your project comes back
      ↓
Continue where you stopped
```

This is especially useful when recon takes days or weeks.

---

## 🛡️ Privacy

Recon data can contain information you may not want sitting on somebody else's server.

Recon Board is designed around a **local-first** approach.

Your normal project data is stored in your browser's local storage rather than being sent to a Recon Board backend.

There is no Recon Board cloud database collecting your project data.

### ⚠️ Important

Local storage is **not the same thing as encryption**.

If somebody has access to your computer/browser profile, they may potentially be able to access locally stored data.

Also, if you clear browser storage, your local project data can be lost.

**Always export your JSON backup regularly.**

For sensitive research, protect the exported JSON file using your operating system's security, encrypted storage, or another appropriate backup method.

---

# 🚀 Features

## 📋 Recon Checklist

Work through your reconnaissance process phase by phase.

Current phases include:

| Phase | Area |
|---|---|
| `0x01` | Acquisitions |
| `0x02` | Find Subdomains |
| `0x03` | Live Subdomains |
| `0x04` | Internet Search Engines |
| `0x05` | URL Extraction |
| `0x06` | Hidden Parameters |
| `0x07` | Content Discovery |
| `0x08` | Wordlists |
| `0x09` | Dorking |

Mark tasks as completed and track your overall recon progress.

---

## 📝 Record What You Find

After every phase, you can save the useful information you discovered.

For example:

```text
Phase: Find Subdomains

api.example.com
dev.example.com
portal.example.com

IP:
203.0.113.10

Notes:
Found several hosts through certificate transparency
and passive enumeration.
```

This answers an important question:

> **"What did I actually find during this phase?"**

You don't have to remember it later.

---

## 🔄 Continue Where You Stopped

Recon doesn't always happen in one sitting.

You might work for two hours today and continue tomorrow.

Recon Board lets you:

```text
Day 1
  ↓
Create program
  ↓
Complete recon
  ↓
Record results
  ↓
Export JSON
  ↓
──────────────
Day 2
  ↓
Open Recon Board
  ↓
Import JSON
  ↓
Continue
```

Your checklist, notes, collected data, and findings can come back with the project.

---

## 💾 Export & Import

### Export

Before finishing your session:

**Export → Save JSON**

Keep the JSON file somewhere safe.

### Import

When you return:

**Import → Select your JSON file**

And continue working.

The JSON format also makes your project easy to back up and move because it is a standard, human-readable data format.

---

## 🐛 Findings

Record security findings alongside your recon work.

You can organize findings with:

- Severity
- Status
- Description
- Notes
- Evidence

This keeps reconnaissance and vulnerability tracking together.

---

# 🧠 Simple Workflow

```text
┌──────────────────────┐
│    Create Program    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│    Add Scope/Target  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Run Recon Phase    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Paste Your Results │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Mark Tasks Done    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Export JSON Backup │
└──────────┬───────────┘
           ↓
        Come Back
           ↓
┌──────────────────────┐
│    Import JSON       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Continue Recon       │
└──────────────────────┘
```

---

# ⚡ Getting Started

There is no complicated installation.

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the application

Open:

```text
recon-board.html
```

in your browser.

### 3. Create a program

Add your target, platform, scope, and notes.

### 4. Start recon

Work through the checklist.

### 5. Record your results

Paste useful output into the relevant phase.

### 6. Back up your project

Export your data as JSON.

### 7. Continue later

Import the JSON file and continue from where you stopped.

---

# 📁 Project Structure

```text
recon-board/
│
├── recon-board.html
└── README.md
```

The application is intentionally lightweight.

There is no backend required for normal use.

---

# 🎯 Design Goals

Recon Board is built around a few simple ideas:

**Simple**  
Open the HTML file and start working.

**Local-first**  
Keep your working project in your browser instead of requiring a cloud backend.

**Portable**  
Export the complete project to JSON.

**Resumable**  
Import the JSON later and continue your work.

**Organized**  
Keep recon progress and collected information together.

**Lightweight**  
No database or server setup for a personal workspace.

---

# 🔒 Security & Responsible Use

Recon Board is a project-management and note-taking tool for authorized security research and bug bounty work.

Only perform reconnaissance against systems, domains, applications, and infrastructure that you are authorized to test.

The tool itself does not grant permission to test any target.

---

# ⭐ If You Like It

If Recon Board helps you organize your security research:

- ⭐ Star the repository
- 🐛 Report bugs
- 💡 Suggest improvements
- 🔧 Contribute improvements

---
