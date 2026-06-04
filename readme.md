# Bootcamp File System Setup

## Why not OneDrive?

Later in the course you'll work with Node.js and React. OneDrive's background syncing can conflict with `node_modules` (which contains thousands of files) and cause hard-to-debug errors. Keep your bootcamp folder in your **home directory** instead.

---

## Step 1 — Create your bootcamp folder

**Mac (Terminal):**
```bash
cd ~
mkdir bootcamp
```

**Windows (Command Prompt or PowerShell):**
```
cd %USERPROFILE%
mkdir bootcamp
```

This creates the folder at:
- Mac: `/Users/your-name/bootcamp`
- Windows: `C:\Users\your-name\bootcamp`

> Do **not** create this inside OneDrive, Dropbox, or any other sync folder.

---

## Step 2 — Clone the class repository

```bash
cd ~/bootcamp
git clone https://github.com/Step8Up-SBC/May-26.git
```

On Windows, replace `~/bootcamp` with `%USERPROFILE%\bootcamp` if needed.

This creates a `May-26` folder inside `bootcamp`. You have **read-only access** to this repo — do not edit files here directly. Each week you'll run:

```bash
cd ~/bootcamp/May-26
git pull
```

to pick up the latest course material.

---

## Step 3 — Create your working folders

```bash
cd ~/bootcamp
mkdir class-work
mkdir projects
```

Your folder structure should now look like this:

```
bootcamp/
├── May-26/          ← class repo (read-only, git pull each week)
├── class-work/      ← your weekly working copies
└── projects/        ← your weekly challenge repos
```

---

## Step 4 — Working with each week's material

At the start of each week:

1. Pull the latest content from the class repo:
   ```bash
   cd ~/bootcamp/May-26
   git pull
   ```

2. Copy that week's folder into `class-work`:

   **Mac:**
   ```bash
   cp -r ~/bootcamp/May-26/week-01 ~/bootcamp/class-work/week-01
   ```

   **Windows (PowerShell):**
   ```powershell
   Copy-Item -Recurse "$env:USERPROFILE\bootcamp\May-26\week-01" "$env:USERPROFILE\bootcamp\class-work\week-01"
   ```

3. Open the `class-work/week-01` folder in VS Code — **not** the `May-26` folder.

---

## Step 5 — Weekly challenge projects

Each weekly challenge should live in its own folder under `projects` and be linked to a repository on **your own GitHub account**.

```bash
cd ~/bootcamp/projects
mkdir week-01-challenge
cd week-01-challenge
git init
git remote add origin https://github.com/YOUR-USERNAME/week-01-challenge.git
```

Commit and push your work regularly throughout the week.

---

## Final folder structure

```
bootcamp/
├── May-26/                  ← class repo (git pull only)
├── class-work/
│   ├── week-01/
│   ├── week-02/
│   └── ...
└── projects/
    ├── week-01-challenge/   ← your own GitHub repo
    ├── week-02-challenge/
    └── ...
```