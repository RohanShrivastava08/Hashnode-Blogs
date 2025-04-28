---
title: "🧠 How I Seamlessly Synced My Obsidian Notes to GitHub 🚀"
datePublished: Mon Apr 28 2025 09:42:42 GMT+0000 (Coordinated Universal Time)
cuid: cma0w3w1m000108l5h60zciqh
slug: how-i-seamlessly-synced-my-obsidian-notes-to-github
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1745833281309/c7532399-3dba-4afd-8b4e-f187a1dda23f.png
tags: blogging, github, technology, learning, tech, hashnode, linkedin, github-actions, hashnodecommunity, technical-writing-1, github-actions-1, blogswithcc, github-copilot, obsidian, exploring

---

In today’s digital world, backing up your personal notes is just as important as writing them. I’ve been using **Obsidian** as my second brain, and recently, I took it a step further by integrating it with **GitHub** for automated backup and version control.

Here’s my simple, organized journey — and how you can do it too!

---

## 🛠️ Why I Synced Obsidian with GitHub

* **Auto Backup:** Never worry about losing important notes again.
    
* **Version History:** Easily roll back to previous versions if needed.
    
* **Access Anywhere:** Pull notes on any device via GitHub clone.
    
* **Productivity:** Smooth workflow with minimal manual effort.
    

---

## 📋 Step-by-Step Guide to Connect Obsidian to GitHub

Here’s the detailed workflow I followed:

---

### 1\. Installing the Obsidian Git Plugin

First, I opened my Obsidian app and did the following:

* Went to **Settings → Community Plugins**
    
* Turned off "Safe Mode"
    
* Browsed and installed the **Obsidian Git** plugin
    

This plugin is the bridge between Obsidian and GitHub!

---

### 2\. Creating a New GitHub Repository

Next, I headed over to [GitHub](https://github.com/) and created a **new repository**.

* I named it something simple like **Obsidian-Notes**.
    
* I kept it **private** for security.
    
* I didn’t initialize it with a README (important when cloning!).
    

---

### 3\. Generating a GitHub Personal Access Token

To allow Obsidian Git to authenticate securely, I created a **Personal Access Token**:

* Opened **GitHub → Settings → Developer Settings → Personal Access Tokens (classic)**
    
* Generated a new token with scopes: `repo`, `workflow`
    
* Copied and saved the token securely (cannot view it again later!).
    

---

### 4\. Cloning the Repository Inside Obsidian

Inside Obsidian, I:

* Opened the **Command Palette (Ctrl + P)**
    
* Searched for "**Git: Clone**"
    
* Pasted my GitHub repo URL
    
* Entered my GitHub username and pasted the generated token as the password
    

Boom — my repository was now cloned inside Obsidian Vault!

---

### 5\. Setting the Local Folder

I selected a local folder inside my Obsidian Vault where all the synced notes would reside.  
Now, everything I write inside this folder is version-controlled.

---

### 6\. Making and Editing Notes

As usual, I created and edited my notes freely — journals, ideas, code snippets, everything! 📝  
Nothing changed about my writing process — only now it’s way more secure!

---

### 7\. Committing and Pushing Changes

After making changes, here’s what I did:

* Opened the Command Palette again
    
* Selected "**Git: Commit and Push**"
    

This would instantly upload the updated notes to GitHub.  
It literally takes 5 seconds!

---

### 8\. Setting Auto Push and Auto Pull

Inside the Obsidian Git plugin settings, I tweaked these options:

* **Auto Commit:** Enabled
    
* **Auto Push:** Enabled
    
* **Auto Pull on Startup:** Enabled
    

This means even if I forget, my notes are always safely backed up!

---

## ✨ Key Takeaways

🔹 GitHub + Obsidian is a **powerful combo** for version control.  
🔹 The setup process takes **less than 20 minutes**.  
🔹 Your notes become **future-proof**, **accessible**, and **organized**.

---

## 🎯 Final Thoughts

Ever since I connected Obsidian with GitHub, my peace of mind has skyrocketed!  
I can now brainstorm, plan, and learn freely — knowing every insight is safely stored and ready whenever I need it.

If you’re serious about your knowledge management, this is a game-changer.  
Set it up once, and your future self will thank you! 🙌