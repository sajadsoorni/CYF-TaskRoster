# Task Permission Strategy – CYF-TaskRoster

This document outlines the permissions strategy for managing rota tasks in the CYF-TaskRoster app. It explains who can create, edit, and delete tasks, and why these decisions were made.

---

## 🎯 Overview

The CYF-TaskRoster app will have two user roles:

- **Trainees** – regular users who can sign up for food or cleaning duties.
- **Admins** – team leads or organisers who can manage all tasks, including modifying or removing entries by others.

---

## 🔐 Action Permissions by Role

| Action         | Trainee              | Admin      |
| -------------- | -------------------- | ---------- |
| Add task       | ✅ Allowed           | ✅ Allowed |
| Delete task    | ❌ Not allowed (MVP) | ✅ Allowed |
| Edit task      | ❌ Not allowed (MVP) | ✅ Allowed |
| View all tasks | ✅ Allowed           | ✅ Allowed |

---

## ✅ Current Decision (MVP)

- For the MVP, **only admins will be able to delete or edit tasks**.
- Trainees will be able to **add tasks** and **view the rota**, but **not edit or delete anything** (even their own entries).
- This avoids accidental changes, keeps the UI simple, and ensures more consistent data handling.

---

## 💡 Future Considerations

We may revisit permissions after the MVP to:

- Allow trainees to delete/edit **their own** tasks
- Introduce user authentication (logins with roles)
- Log changes for transparency
- Add confirmation prompts for destructive actions

---

📄 **View in Google Docs:**  
[Permissions Planning Doc](https://docs.google.com/document/d/1TioxMee8RErutXoWC13rs_MvAi7RG_u3Ak0aIKn4xv8/edit?usp=sharing)
