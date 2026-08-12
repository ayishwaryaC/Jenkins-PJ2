# Jenkins PJ2

A simple Jenkins CI flow for a GitHub repository.

## Flow Overview

```text
[GitHub] --> [Jenkins Checkout] --> [Workspace] --> [Execute Shell] --> [Console Output] --> [Build Success]
```

This README shows the main steps in the build pipeline.

---

## Step-by-step Flow

1. **GitHub**: source code is stored in the repository.
2. **Jenkins Checkout**: Jenkins retrieves the latest `main` branch.
3. **Workspace**: files are placed in the Jenkins workspace.
4. **Execute Shell**: Jenkins runs the configured shell commands.
5. **Console Output**: build logs are shown.
6. **Build Success**: Jenkins reports the final status.

---

## Repository files

```
Jenkins-PJ2/
├── README.md
└── index.html
```

---

## Jenkins job details

- **Job name:** Jenkins-PJ2
- **Type:** Freestyle project
- **SCM:** Git
- **Branch:** `main`
- **Repo:** `https://github.com/ayishwaryaC/Jenkins-PJ2`

---

## Build commands

```sh
echo "Successfully the jenkins Downloaded the project and deployed"
ls
```

- `echo` prints a message in the console log.
- `ls` lists the repository files in the workspace.

---

## Simple box flow

```text
┌──────────────┐   git pull  ┌─────────────────┐
│  GitHub repo │ ----------> │ Jenkins checkout│
└──────────────┘             └──────┬──────────┘
                                      │
                                      ▼
                                ┌──────────────┐
                                │ Workspace    │
                                │ README.md    │
                                │ index.html   │
                                └──────┬───────┘
                                      │
                                      ▼
                                ┌──────────────┐
                                │ Execute Shell│
                                │ echo + ls    │
                                └──────┬───────┘
                                      │
                                      ▼
                                ┌──────────────┐
                                │ Console Log  │
                                │ build output │
                                └──────┬───────┘
                                      │
                                      ▼
                                ┌──────────────┐
                                │ Build Success│
                                └──────────────┘
```

---

## What this shows

- GitHub + Jenkins integration
- Git checkout and workspace setup
- Shell command execution inside Jenkins
- Console output for validation
- Successful pipeline completion

---

## Why it is useful

This project is a basic CI example that proves:

- Jenkins can fetch code from GitHub
- the workspace contains the repository files
- shell commands run correctly
- console output reports success

---

## Expected result

After the build, Jenkins should show:

- `README.md`
- `index.html`
- `Finished: SUCCESS`

This confirms the repository was checked out and the build step completed.

---

## Notes

This is a minimal demonstration of Jenkins CI, not a full production deployment. The current build step only prints a message and lists files.

GitHub
   ↓
Git Checkout
   ↓
Jenkins Workspace
   ↓
Shell Execution
   ↓
File Verification
   ↓
Build SUCCESS

A real deployment would require additional deployment infrastructure.

🚀 Evolution to Real CI/CD

This practical is the foundation for the next stages:

                 CURRENT
                    │
                    ▼
        ┌────────────────────┐
        │ GitHub → Jenkins   │
        │ Checkout → Build   │
        └─────────┬──────────┘
                  │
                  ▼
              NEXT LEVEL
                  │
                  ▼
        ┌────────────────────┐
        │ GitHub Webhook     │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Jenkins Pipeline   │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Build + Test       │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Docker Image       │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Docker Hub / ECR   │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Deployment         │
        │ EC2 / Kubernetes   │
        └────────────────────┘
🛣️ Project Roadmap
                     Jenkins Learning Path

        ┌──────────────────────────────┐
        │  ✅ Practical 1              │
        │  Jenkins Basic Job           │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  ✅ Practical 2              │
        │  GitHub Integration          │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  🔜 Practical 3              │
        │  GitHub Webhook              │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  🔜 Practical 4              │
        │  Jenkins Pipeline            │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  🔜 Practical 5              │
        │  Jenkinsfile + Git           │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  🔜 Practical 6              │
        │  Docker CI/CD                │
        └──────────────┬───────────────┘
                       │
                       ▼
        ┌──────────────────────────────┐
        │  🚀 Final Project             │
        │  Jenkins + Docker + AWS      │
        │  + Kubernetes Deployment     │
        └──────────────────────────────┘
🏆 Skills Demonstrated
Jenkins
   │
   ├── Job Configuration
   ├── Git SCM Integration
   ├── Workspace Management
   ├── Build Steps
   ├── Shell Execution
   └── Console Log Analysis

Git
   │
   ├── Repository Integration
   ├── Fetch
   └── Checkout

DevOps
   │
   ├── CI Fundamentals
   ├── Source → Build Flow
   └── Build Validation
📌 Final Takeaway

This project demonstrates the fundamental CI workflow where Jenkins retrieves source code from GitHub, checks it out into a dedicated workspace, executes build commands, validates the result, and reports the build status.

🔥 Core Flow
        👩‍💻
     Developer
         │
         ▼
     🐙 GitHub
         │
         ▼
     ⚙️ Jenkins
         │
         ▼
    📂 Workspace
         │
         ▼
     🔨 Build
         │
         ▼
   📋 Console Logs
         │
         ▼
    🟢 SUCCESS



🚀 Built as a hands-on DevOps learning project

GitHub → Jenkins → Build → Validate → SUCCESS
