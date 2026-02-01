Below is a **fully updated beginner-optimized version** of that page. You can copy-paste it as documentation or learning notes.

---

```md
---
layout: page
title: Installing Express.js (Beginner Friendly)
description: A step-by-step beginner guide to installing Express.js, setting up a Node.js project, and understanding what each command does.
menu: starter
order: 1
redirect_from: "/starter/installing.html"
---
```

# Installing Express.js (For Complete Beginners)

This guide assumes **no prior backend experience**.
If you can open a terminal and type commands, you’re good to go 👍

---

## 1️⃣ What is Express.js?

**Express.js** is a lightweight web framework for **Node.js** that helps you:

* Create web servers
* Build APIs
* Handle requests and responses
* Connect frontend apps (React, Next.js, etc.) to a backend

Think of it as:

> “A tool that makes Node.js easier and faster for web development.”

---

## 2️⃣ Prerequisite: Install Node.js

Before installing Express, you **must** have Node.js installed.

### Check if Node.js is installed

Open your terminal (Command Prompt / PowerShell / Terminal) and run:

```bash
node -v
```

If you see a version number like `v18.x.x` or higher, you’re good.

If not:
👉 Download and install Node.js from
**[https://nodejs.org](https://nodejs.org)**
(Choose the **LTS version**, recommended for beginners)

---

### Node.js version requirements

* **Express 4.x** → Node.js **10 or higher**
* **Express 5.x** → Node.js **18 or higher** (recommended)

If you’re learning today, **Node 18+ + Express 5** is the best combo.

---

## 3️⃣ Create a Project Folder

Now let’s create a folder for your Express app.

```bash
mkdir myapp
cd myapp
```

📌 This folder will contain:

* Your backend code
* Installed packages
* Configuration files

---

## 4️⃣ Initialize a Node.js Project (`package.json`)

Run the following command:

```bash
npm init
```

You’ll be asked several questions like:

```
package name:
version:
description:
entry point:
```

### What should beginners do?

👉 **Just press ENTER for everything**, except:

```
entry point: (index.js)
```

You can:

* Press ENTER to keep `index.js`, **or**
* Type `app.js` (very common for Express apps)

Both are correct.

---

### What is `package.json`?

This file:

* Describes your project
* Lists installed dependencies (like Express)
* Stores scripts (start, dev, etc.)

Think of it as:

> “The brain of your Node.js project.”

---

## 5️⃣ Install Express.js

Now install Express inside your project folder:

```bash
npm install express
```

This will:

* Download Express
* Create a `node_modules` folder
* Add Express to `dependencies` in `package.json`

---

### After installation, your folder looks like this:

```
myapp/
├── node_modules/
├── package.json
├── package-lock.json
```

📌 **Do not delete `node_modules` or `package-lock.json`**

---

## 6️⃣ (Optional) Install Express without saving

If you just want to **experiment** and not save Express permanently:

```bash
npm install express --no-save
```

⚠️ Beginners usually **do NOT need this**.
Use normal `npm install express` instead.

---

## 7️⃣ Important npm behavior (Beginner Note)

* **npm 5+ (modern npm)** automatically saves packages to `dependencies`
* Older npm versions needed `--save` manually

Today, you **do not need `--save`**.

---

## 8️⃣ What’s Next?

Now that Express is installed, the next steps are:

1. Create your main file (`app.js` or `index.js`)
2. Import Express
3. Create a server
4. Listen on a port

Example (just for understanding, not yet required):

```js
const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(3000, () => {
  console.log("Server running on port 3000");
});
```

You’ll learn this step-by-step next.

---

## 🧠 Beginner Mental Model (Very Important)

* **Node.js** → JavaScript runtime
* **npm** → package manager
* **Express.js** → backend framework
* **package.json** → project configuration
* **node_modules** → installed libraries

Once this clicks, backend becomes much easier.
