# Linux Production-Style Server Practice

This repository documents my hands-on practice of setting up a **production-like Linux server environment**, focusing on real-world concepts rather than just commands.

The goal of this exercise was to understand how Linux servers are actually managed in **Cloud / DevOps environments**, especially around user roles, permissions, and directory standards.

---

## 🔹 What I Implemented

- Created separate Linux users:
  - **Admin user** (with sudo access)
  - **Developer user** (limited permissions)
- Implemented **role-based access control** following the least privilege principle
- Designed proper Linux directory structure for:
  - Application code (`/opt/apps`)
  - Logs (`/var/log`)
  - Backups
  - Temporary files
- Ensured:
  - Developers can work on application code
  - Developers can read logs but **cannot modify them**
  - Only admin users can manage logs and system-level resources
- Created different file types to simulate real environments:
  - `.log` (logs)
  - `.conf` (configuration)
  - `.sh` (automation scripts)
  - `.txt` (documentation)

---

## 🔐 Key Concepts Practiced

- Linux user and group management
- sudo access control
- File ownership and permissions
- Secure directory structuring
- Real-world Linux server workflows

---

## 📸 Proof of Work

Screenshots in this repository show:
- Admin vs developer access
- Permission denied scenarios (expected behavior)
- Proper ownership of application directories

---

## 🧠 Why This Matters

In real production environments:
- Developers do not get full server access
- Logs and system files are protected
- Security and structure are as important as functionality

This practice helped me understand **why Linux permissions and roles are critical in Cloud and DevOps roles**.

---

## 🚀 Tech Stack

- Linux (Ubuntu)
- Git & GitHub
- Shell scripting basics

---

## 📌 Status

This is a learning-focused repository and will be improved further as I continue practicing Linux, Cloud, and DevOps concepts.
                  ┌─────────────────────────┐
                  │     Linux Server         │
                  │     (Ubuntu)             │
                  └──────────┬──────────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
     ┌────────▼────────┐         ┌──────────▼─────────┐
     │   Admin User     │         │   Developer User   │
     │   (adminuser)    │         │   (devuser)        │
     │   sudo access    │         │   no sudo          │
     └────────┬────────┘         └──────────┬─────────┘
              │                             │
   ┌──────────▼──────────┐       ┌──────────▼──────────┐
   │ System Resources     │       │ Application Code    │
   │                      │       │ /opt/apps/myapp     │
   │ /var/log/myapp       │       │  - src              │
   │ /backup/myapp        │       │  - build            │
   │ cron / services      │       │  - scripts          │
   └─────────────────────┘       └─────────────────────┘

              ┌─────────────────────────────┐
              │  Access Control (Linux)     │
              │  - Ownership                │
              │  - Permissions (chmod)      │
              │  - Groups                   │
              │  - sudo policy              │
              └─────────────────────────────┘
