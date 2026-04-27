# Local Development & Auto-Upload to GitHub
## The Complete Beginner Guide

This guide sets up your computer so you can:
- Edit your website in VS Code (like a proper developer)
- Preview changes instantly in your browser
- Push updates to GitHub with one click — site goes live automatically

---

## What You Need to Install (One Time Only)

### 1. Install Git
Git is the tool that talks to GitHub from your computer.

1. Go to [git-scm.com/downloads](https://git-scm.com/downloads)
2. Click your operating system (Windows / Mac)
3. Download and install — keep all the default settings, just click Next/Continue
4. When done, verify it worked:
   - **Windows**: search "Command Prompt" in Start Menu, open it, type `git --version`, press Enter
   - **Mac**: open Terminal (search "Terminal" in Spotlight), type `git --version`, press Enter
   - You should see something like: `git version 2.43.0` — any version is fine

### 2. Install VS Code
VS Code is the text editor you'll use to edit your site.

1. Go to [code.visualstudio.com](https://code.visualstudio.com)
2. Click the big **Download** button
3. Install it — keep all default settings
4. Open VS Code — you'll see a welcome screen

### 3. Tell Git Who You Are (One Time Only)
Git needs your name and email so it knows who is making changes.

Open Command Prompt (Windows) or Terminal (Mac) and type these two commands,
pressing Enter after each one:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Use the same email address as your GitHub account.

---

## Connect Your GitHub Repo to Your Computer

This is called "cloning" — it downloads your website files to your computer.

### Step 1 — Get your repo URL
1. Go to your GitHub repository (`github.com/yourusername/yourusername.github.io`)
2. Click the green **< > Code** button
3. Make sure **HTTPS** is selected
4. Copy the URL — it looks like:
   `https://github.com/yourusername/yourusername.github.io.git`

### Step 2 — Choose where to save it on your computer
Decide which folder you want your website files to live in.
A good place is your Desktop or a Documents/Projects folder.

### Step 3 — Clone the repo
Open Command Prompt / Terminal and type:

```bash
cd Desktop
```
(This moves you to your Desktop. Change "Desktop" to wherever you want the folder.)

Then type:
```bash
git clone https://github.com/yourusername/yourusername.github.io.git
```

Replace `yourusername` with your actual GitHub username.

You'll see some text appear — when it finishes, a new folder appears on your
Desktop with your website files inside. Done!

---

## Open Your Site in VS Code

1. Open VS Code
2. Click **File → Open Folder**
3. Navigate to the folder that was just created on your Desktop
4. Click **Select Folder** (Windows) or **Open** (Mac)
5. You'll see your files listed on the left panel — click `index.html` to open it

---

## Preview Your Site Locally (Without Internet)

**Option A — Simple (just double-click):**
1. Open File Explorer / Finder
2. Navigate to your website folder
3. Double-click `index.html`
4. It opens in your browser — this is your website!
5. Every time you save a change in VS Code, press **F5** in the browser to refresh

**Option B — Live Preview in VS Code (auto-refreshes):**
1. In VS Code, go to **Extensions** (icon on the left sidebar that looks like 4 squares)
2. Search for **Live Server**
3. Click **Install** on the extension by Ritwick Dey
4. After installing, right-click `index.html` in the file panel
5. Click **Open with Live Server**
6. Your browser opens automatically — and now it **auto-refreshes every time you save**
   No need to press F5 at all!

---

## Edit Your Site

1. In VS Code, click `index.html` in the left panel
2. Use **Ctrl+F** (Windows) or **Cmd+F** (Mac) to search for text you want to change
3. Edit the text directly
4. Press **Ctrl+S** (Windows) or **Cmd+S** (Mac) to save
5. Your browser preview updates instantly (if using Live Server)

---

## Upload Changes to GitHub

Once you're happy with your edits, here's how to push them live.

### Option A — Using VS Code (No commands, beginner friendly) ✅ Recommended

1. In VS Code, click the **Source Control** icon in the left sidebar
   (it looks like a branching tree — 3 dots connected by lines)
2. You'll see a list of files you changed
3. Type a short message in the box at the top describing what you did
   e.g. `"Added new blog post"` or `"Updated work experience"`
4. Click the **✓ Commit** button
5. Click the **Sync Changes** button (or the cloud icon with an arrow)
6. Done! GitHub updates and your live site reflects the changes in ~1 minute

### Option B — Using the Terminal (3 commands)

Open Terminal / Command Prompt, navigate to your folder:

```bash
cd Desktop/yourusername.github.io
```

Then run these 3 commands:

```bash
git add .
git commit -m "Describe what you changed here"
git push
```

That's it. Your site is updated live within 1 minute.

---

## First Time Pushing — GitHub Login

The first time you push from your computer, GitHub will ask you to log in.

**On Windows:**
- A login window pops up automatically
- Sign in with your GitHub username and password
- Your credentials are saved — you won't need to do this again

**On Mac:**
- Terminal will ask for your GitHub username
- For the password, you **cannot use your GitHub password** — you need a token instead:
  1. Go to GitHub → click your profile photo → **Settings**
  2. Scroll to the bottom → click **Developer settings**
  3. Click **Personal access tokens → Tokens (classic)**
  4. Click **Generate new token (classic)**
  5. Give it a name, set expiry to "No expiration", tick the **repo** checkbox
  6. Click **Generate token**
  7. Copy the token (you only see it once!) and paste it as your password

---

## Your Daily Workflow (Once Everything is Set Up)

```
1. Open VS Code
2. Edit index.html
3. Preview in browser (Live Server auto-refreshes)
4. When happy → Source Control panel → write message → Commit → Sync
5. Site is live on GitHub within 1 minute ✓
```

---

## Troubleshooting

| Problem | Fix |
|---|---|
| `git: command not found` | Git wasn't installed correctly — reinstall from git-scm.com |
| `Permission denied` | You need to log in to GitHub — see "First Time Pushing" above |
| Changes pushed but site not updated | Wait 2 minutes and hard-refresh: Ctrl+Shift+R (Windows) / Cmd+Shift+R (Mac) |
| VS Code doesn't show Source Control changes | Make sure you opened the **folder**, not just the file |
| Live Server not working | Make sure the extension is installed and you right-clicked `index.html` |

---

## Summary — What Each Tool Does

| Tool | What it does |
|---|---|
| **Git** | Tracks your changes and talks to GitHub |
| **VS Code** | Text editor for editing your site |
| **Live Server** (VS Code extension) | Shows a live preview in your browser |
| **Source Control panel** (in VS Code) | Visual interface for committing and pushing — no commands needed |
| **Terminal / Command Prompt** | Alternative way to run Git commands if you prefer |

---

> Come back to this guide when you're on your new computer and ready to set up.
> Follow the steps in order and you'll be up and running in under 20 minutes.
