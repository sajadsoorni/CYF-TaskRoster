# Backend Data Structure Decision – CYF-TaskRoster

This document explains the decision made regarding how rota data will be stored in the backend of the CYF-TaskRoster app. It compares two potential options — using a local JSON file or a cloud-hosted MongoDB database — and justifies the chosen approach for early development.

---

## 💡 Summary Decision

We decided to use a **JSON file** for the early stages of development to reduce complexity and allow fast testing of frontend-backend integration. This approach also makes it easier for contributors to run and contribute to the project without requiring database credentials or internet access.

Later, we may transition to **MongoDB** when we introduce user authentication, admin roles, and cloud deployment with persistent data storage.

---

## 🔍 Comparison Table

| Feature                    | JSON File                     | MongoDB (Atlas)              |
| -------------------------- | ----------------------------- | ---------------------------- |
| 🛠 Setup Effort             | Very low                      | Medium (account, connection) |
| ⚙️ Backend Integration     | Easy with `fs` in Node.js     | Easy with Mongoose/MongoDB   |
| 🔒 Authentication Needed   | ❌ Not required               | ✅ Needed for DB URI         |
| 🌍 Works Offline           | ✅ Yes                        | ❌ Requires internet         |
| 🔁 Scalable / Multi-user   | ❌ No                         | ✅ Yes                       |
| 🔎 Advanced Querying       | ❌ Manual filtering           | ✅ Powerful querying support |
| 📦 Suitable for Deployment | ❌ Not ideal (no persistence) | ✅ Great for cloud hosting   |

---

## ✅ Why We Chose JSON (for now)

- ⚡ **Speed & Simplicity**: Easy to implement and test during Sprint 3, especially for local development and prototyping.
- 🧪 **No External Setup**: Contributors don’t need MongoDB Atlas accounts or connection URIs to run the project.
- 🧑‍💻 **Beginner-Friendly**: Ideal for understanding how data flows between frontend and backend before introducing databases.

---

## 🔄 Future Plan: Move to MongoDB

Once the following features are planned, we will consider upgrading to MongoDB:

- 🔐 User authentication (e.g., admin vs. trainee roles)
- ☁️ Deployment to Render / Railway (requires persistent storage)
- 📈 Support for multiple users and real-time updates
- 🔎 Filtering, sorting, or querying rota data

---

📄 **View in Google Docs:**  
[Backend Planning Document](https://docs.google.com/document/d/1Y4dHeMSDZMd70Le-_-fvCjEz4ipjXL0ohiwW4Fv5xTQ/edit?usp=sharing)
