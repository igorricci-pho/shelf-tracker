# Deployment Guide: Reparatur Regal Tracker

This guide details how to publish your Reparatur Regal Tracker website online so anyone with the link can access it.

## 🛠️ How it works now
- We have configured a shared database backend using **ExtendsClass JSON storage**.
- Every user loading the website will now read from and write to the same shared online state.
- A **Refresh** button has been added to the header so you can pull the latest changes from other users without reloading the page.
- We copied `shelf-tracker.html` to [index.html](file:///home/backup20straiv/projects/shelf_tracker/index.html) so it serves automatically as the home page when hosted.
- We initialized a local Git repository with your initial files.

---

## Option 1: Netlify Drag-and-Drop (Fastest, no setup)
This is the absolute fastest way to host your site without using Git or the command line.

1. Open your browser and go to [Netlify Drop](https://app.netlify.com/drop).
2. Open your local file explorer and navigate to your project directory: `/home/backup20straiv/projects/shelf_tracker`.
3. Drag the entire `shelf_tracker` folder and drop it into the Netlify browser window.
4. Netlify will instantly upload the files and generate a live, public URL (e.g., `https://random-name-12345.netlify.app`).

---

## Option 2: GitHub Pages (Recommended)
This is the best long-term option as it hosts your site for free and updates automatically when you make changes.

### Step 1: Create a new repository on GitHub
1. Go to [GitHub](https://github.com/) and log in.
2. Click the **New** button to create a new repository.
3. Name it `shelf-tracker` (or any name you prefer).
4. Leave it public, do **not** check "Add a README file", and click **Create repository**.

### Step 2: Push your local code to GitHub
Run the following commands in your terminal (or we can run them for you once you have your repository URL):

```bash
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/shelf-tracker.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. On your GitHub repository page, go to **Settings** (gear icon at the top).
2. On the left sidebar, click **Pages**.
3. Under "Build and deployment", set the Source to **Deploy from a branch**.
4. Choose the **main** branch and `/ (root)` folder, then click **Save**.
5. Wait a minute, and GitHub will provide your live URL (e.g., `https://<YOUR_GITHUB_USERNAME>.github.io/shelf-tracker/`).

---

## Option 3: Vercel (Git-based Deployment)
If you prefer Vercel:
1. Push your code to GitHub (using the steps in Option 2).
2. Go to [Vercel](https://vercel.com/) and sign in with GitHub.
3. Click **Add New** -> **Project**.
4. Import your `shelf-tracker` repository.
5. Click **Deploy**. Vercel will build and host your site instantly.
