---
title: "Deploying a Next.js Project on Vercel: My Experience"
datePublished: Mon Sep 30 2024 06:54:46 GMT+0000 (Coordinated Universal Time)
cuid: cm1onn0xv000m0al5e61e64jg
slug: deploying-a-nextjs-project-on-vercel-my-experience
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1727679143735/6d132d15-f12f-433d-aded-edf0c5e1d191.webp
tags: blog, blogging, technology, tech, hashnode, nextjs, vercel, hashnodecommunity, technical-writing-1, hashnodebootcamp, vercelhashnode, next-dev, blogswithcc, nextauthjs, nextjs-132

---

Recently, I deployed my Next.js project on Vercel, [and i](https://vercel.com)t was surprisingly easy. If you're new to deploying Next.js apps, here's how I did it:

### 1\. **Create a Next.js Project**

First, I created my N[ext.js](https://vercel.com) project using the comm[and:](https://vercel.com)

```javascript
npx create-next-app@latest
```

This sets up the basic structure of the app.

### 2\. **P**[**ush to**](https://vercel.com) **GitHub**

Once my project was ready, I pu[shed t](https://vercel.com)he code to a [GitHub](https://vercel.com) repository. If you haven't done this before, you can initialize a git repository using:

```javascript
git init
git add .
git commit -m "Initial commit"
git remote add origin <your-github-repo-url>
git push -u origin main
```

### 3\. **Connect to Vercel**

I then went to [Vercel](https://vercel.com), signe[d in,](https://vercel.com) and clicked on t[he **"Ne**](https://vercel.com)**w Project"** button. Vercel automatically detected my GitHub repositories, so I selected my Next.js project from the list.

### 4\. **Deploy**

Once selected, I simply clicked **"Deploy**[**"**, and](https://vercel.com) that[’s it!](https://vercel.com) Vercel took care of the rest. It deployed my Next.js app, and in a few minutes, my project was live with a URL.

### 5\. **Live Link**

After deployment, I got a live link [where](https://vercel.com) my Next.[js pro](https://vercel.com)ject was hosted. Now, I can easily share it with anyone.

That's how I deployed my Next.js project using Vercel. The whole process was smooth, and it hardly took any time!