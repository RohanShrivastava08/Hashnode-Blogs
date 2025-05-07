---
title: "Getting Started with Tailwind CSS (Latest Version) in a React + Vite Project — The Easy Way!🌟"
datePublished: Tue May 06 2025 12:46:54 GMT+0000 (Coordinated Universal Time)
cuid: cmaci7ks3000h09ld8tegbftg
slug: getting-started-with-tailwind-css-latest-version-in-a-react-vite-project-the-easy-way
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1746535526920/92590972-9311-4564-a558-b68caee15366.png
tags: blogging, trends, software-development, technology, web-development, webdev, learning, reactjs, tech, hashnode, software-engineering, tailwind-css, vite, blogswithcc, explore

---

Hey folks 👋

I recently explored the latest version of **Tailwind CSS**, and I’ve got to say — it’s one of the best CSS frameworks out there. It’s fast, flexible, and makes styling modern UIs a breeze. In this blog, I’ll walk you through how I installed Tailwind CSS in a React project using **Vite**. So, if you're starting fresh or just want a quick and clean setup, this guide is for you!

---

## 🚀 What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework that lets you build modern websites without writing custom CSS. You just use predefined class names right in your HTML or JSX. No more switching between HTML and CSS files constantly!

And the best part? Tailwind scans all your files and only includes the styles you actually use. That means smaller file sizes and faster performance.

---

## ⚡ Why Vite?

Vite is a modern build tool that’s super fast and developer-friendly. It works great with React, and integrating Tailwind into it is smooth and straightforward.

---

## 🛠️ Step-by-Step: Installing Tailwind CSS with Vite (React Project)

Here’s how I did it in just a few minutes.

---

### 1️⃣ Create a Vite + React project

```javascript
npm create vite@latest my-tailwind-app -- --template react
cd my-tailwind-app
npm install
```

---

### 2️⃣ Install Tailwind CSS and its Vite plugin

```javascript
npm install tailwindcss @tailwindcss/vite
```

This installs both Tailwind and its official Vite plugin for smooth integration.

---

### 3️⃣ Configure the Vite plugin

Open `vite.config.js` or `vite.config.ts` and update it like this:

```javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [react(), tailwindcss()],
});
```

---

### 4️⃣ Create your Tailwind CSS file

Inside `src/`, create a file called `styles.css` (or any name you like), and add:

```javascript
@import "tailwindcss";
```

Now Tailwind will inject all its utility classes here!

---

### 5️⃣ Link the CSS in your project

Import the `styles.css` in your `main.jsx` file:

```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App.jsx';
import './styles.css'; // <-- Tailwind styles

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

---

### 6️⃣ Start the dev server

Now just run:

```javascript
npm run dev
```

That’s it! Your app is now using Tailwind CSS! 🎉

---

## 💡 Let’s Test It

Open your `App.jsx` and add a simple heading:

```javascript
function App() {
  return (
    <div className="text-3xl font-bold underline text-blue-600 p-4">
      Hello Tailwind + Vite! 👋
    </div>
  );
}

export default App;
```

You’ll instantly see your styles applied. Super cool, right?

---

## ✨ Final Thoughts

Tailwind CSS has seriously boosted my productivity in frontend development. With Vite’s blazing-fast setup and Tailwind’s utility classes, I can now prototype and build clean UIs faster than ever before.

If you're someone who loves writing minimal CSS and focusing on functionality and speed — **Tailwind is a game changer**.

---

## 📝 Useful Resources

* [Tailwind CSS Docs](https://tailwindcss.com/docs/installation/using-vite)
    
* [Vite Official Site](https://vitejs.dev/)
    

---

Thanks for reading 🙌  
If you found this helpful, feel free to share or drop a comment on my Hashnode!  
Let’s build something awesome. 💻✨