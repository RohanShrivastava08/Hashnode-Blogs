---
title: "Oops, I Pushed firebase.js to GitHub: Here’s How I Recovered Like a Pro"
datePublished: Sat Apr 19 2025 17:11:59 GMT+0000 (Coordinated Universal Time)
cuid: cm9oh707s000a09l28shvcdxm
slug: oops-i-pushed-firebasejs-to-github-heres-how-i-recovered-like-a-pro
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1745082497371/c00d071c-c544-42f0-a86d-031b3845706b.png
tags: blogging, trends, github, technology, git, learning, coding, tech, hashnode, github-actions, githubpages, technical-writing-1, github-actions-1, blogswithcc, gitcommands

---

So, something happened recently that made my stomach drop.

I was working on my project like usual, pushing updates, tweaking components, polishing my Firebase setup the usual grind. Everything was going smooth until I pushed my code to GitHub… and realized something horrifying.

**I had pushed** `firebase.js` to a public repo.  
With **API keys.**  
Exposed. To the world.

### That oh-no moment...

If you've ever had that feeling where your soul just *leaves your body*, you know what I mean.

At first, I didn’t think it was a big deal. “No worries,” I told myself. “I’ll just delete the file, add it to `.gitignore`, commit, and push again.”

But guess what? Git doesn’t forget. Even if the file is gone from your latest commit, it’s still there in your **commit history**.

So technically, **the damage was already done**.

### Panic mode: ON 🔥

I searched everything “How to remove sensitive files from GitHub,” “firebase.js exposed GitHub fix,” “how to delete commit history file,” and more.

Eventually, I found the solution. An old-school command, powerful and effective:

`git filter-branch`.

Yes, I know there are newer tools like `git filter-repo`, but in that moment, I just needed to **wipe the file** from every single commit like it never existed.

---

## Here’s How I Fixed It (Like a Boss 😎)

### Step 1: Run the history-rewriting command

Inside the root of my project folder, I ran this:

```javascript
bashCopyEditgit filter-branch --force --index-filter \
"git rm --cached --ignore-unmatch src/firebase.js" \
--prune-empty --tag-name-filter cat -- --all
```

What this command does:

* It goes through all the commits in the repo.
    
* Removes the file `src/firebase.js` from every commit.
    
* Cleans up empty commits after removing the file.
    

You’ll get a warning that `git filter-branch` has some risks that’s true, especially if you're working with a team or shared repo. But in my case, I was flying solo, so I hit enter and hoped for the best.

### Step 2: Force push the cleaned history

After the above process finished, I pushed everything back to GitHub like this:

```javascript
bashCopyEditgit push origin --force --all
git push origin --force --tags
```

Boom. GitHub now had a clean history. The file was **gone** not just from the latest commit, but from **everywhere**.

### Step 3: Double-check using `git log`

I wanted to be 100% sure that the file was no longer present, so I ran:

```javascript
bashCopyEditgit log --all --grep="firebase.js"
```

Nothing came up. ✅

I even checked GitHub manually. It was clean. No trace of the file. Success.

---

## What I Learned (The Hard Way)

This was a solid slap of a lesson. But I learned a lot and if you’re reading this, maybe you can avoid the same mistake.

### 1\. Never push secrets to GitHub. Not even by mistake.

Always double-check what’s being committed. Run `git status`. Add critical files to `.gitignore` from the start.

### 2\. Rotate your Firebase API keys immediately.

Even if you delete them later, **once they’re public, they’re compromised**. I went into my Firebase console and regenerated new keys.

### 3\. Use environment variables for secrets.

Store your keys in a `.env` file and reference them safely in your code. Never hardcode them into your files.

### 4\. Set up GitHub secret scanning and tools like GitGuardian.

GitHub has built-in alerts now. You can also use third-party tools to scan for exposed secrets. Better safe than sorry.

---

## Mistakes Happen: That’s How We Grow 💡

Look, we’re all human. We’re devs juggling 100 things, switching between files, trying to ship features and squash bugs at the same time.

Sometimes, mistakes happen.

What matters is that we learn, fix, and share so the next person can avoid the same pitfall.

I’m sharing this not because I’m proud of what happened… but because I’m proud I fixed it, learned from it, and came out a better developer.

If you’ve ever messed up and felt like it was the end of the world trust me, it’s not. You got this.

---

## Was this helpful?

If this saved you hours of panic, please leave a like, comment, or share it with a fellow dev.  
Because chances are, someone else is out there googling in full panic mode right now — just like I was.

Let’s help each other out.

Stay safe, stay smart, and protect your API keys ✌️