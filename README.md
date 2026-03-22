# Terminal-Style Developer Portfolio

> A geeky, interactive Command Line Interface (CLI) style portfolio designed for Backend Developers and Software Architects.

**🌐 Live Website:** [https://iots1.github.io/me/](https://iots1.github.io/me/)

A portfolio that runs in the web browser, simulating a Linux/Mac terminal environment — built as a **single static HTML file**. Present your work history, skills, and projects with style. Perfect for Geeks, DevOps engineers, and Backend Developers.

---

## ⚙️ Configuration (Open Source Ready)

All personal data is centralized in a single `const CONFIG` object at the top of the `<script>` block in `index.html`. **No need to search and replace scattered values** — just edit this block:

```js
const CONFIG = {
  // 1. General Profile
  userName: "Jirayu Mool-ang",
  userTitle: "Senior Backend Developer",
  whoamiTitle: "Senior Backend Developer & Software Architect",
  whoamiDescription: "...",

  // 2. Terminal & OS Identity
  osName: "Jirayu-OS",        // Shown in boot screen & neofetch
  terminalUser: "jirayu",     // Header: [terminalUser]@[terminalHost]
  terminalHost: "backend-node",
  promptUser: "guest",        // CLI prompt: [promptUser]@[promptMachine]
  promptMachine: "system",

  // 3. GitHub Info
  githubUsername: "iots1",
  githubRepo: "me",           // Used for the ⭐ Star button in the header
  avatarUrl: "https://github.com/iots1.png",

  // 4. Contact & Links
  email: "...",
  location: "...",
  linkedinUrl: "...",
  blueprintUrl: "...",
  resumeUrl: "...",           // Canva embed link for Resume overlay
  portfolioUrl: "...",        // Canva embed link for Portfolio overlay
};
```

After editing `CONFIG`, the values are automatically applied to:
- `document.title` and the terminal header text
- GitHub profile link and ⭐ Star button iframe (`src`)
- All `guest@system` CLI prompt labels throughout the page

### Open Graph / Social Media Meta Tags

Update the `<meta>` tags in `<head>` to control how the link appears when shared on LINE, Twitter, Facebook, etc.:

```html
<meta property="og:title"       content="Jirayu Mool-ang | Senior Backend Developer" />
<meta property="og:description" content="Interactive Terminal-Style Developer Portfolio" />
<meta property="og:image"       content="https://iots1.github.io/me/thumbnail.png" />
<meta property="og:url"         content="https://iots1.github.io/me/" />
<meta property="og:type"        content="website" />
```

> **Tip:** Replace `thumbnail.png` with your own image (recommended size: **1200×630 px**). The thumbnail generator script (`generate_thumbnail.js`) can be used to automate this.

---

## ✨ Features

| Feature                            | Description                                                                                                                     |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Interactive CLI**                | A real input field where you can type and execute commands, just like a terminal                                                |
| **Command History**                | Press ⬆️ / ⬇️ arrow keys to cycle through previously entered commands                                                           |
| **Draggable Window**               | Click and drag the header bar (near the red/yellow/green dots) to reposition the terminal window                                |
| **Boot Sequence Effect**           | Simulates a startup script with loading animations and ASCII Art logo on first load — press `Space` to pause or `Enter` to skip |
| **Built-in Presentation (Iframe)** | Opens a Resume or Portfolio (Canva) in a full-screen overlay directly on the page — press `Ctrl+X` or `Esc` to close            |
| **GitHub Star Button**             | Live ⭐ Star button and profile link shown in the terminal header — driven by `CONFIG.githubUsername` and `CONFIG.githubRepo`    |
| **Open Graph Thumbnail**           | Proper `og:image` meta tag so the site previews correctly when shared on LINE, Twitter, Facebook, etc.                          |
| **Easter Eggs 🥚**                 | Hidden hacker-style surprises — try typing secret commands to discover them!                                                    |

---

## 🛠️ Tech Stack

- **HTML5** — entire structure lives in a single `index.html` file
- **Tailwind CSS (CDN)** — layout and styling with a GitHub Dark Dimmed theme
- **Vanilla JavaScript** — all logic for typing, window dragging, terminal functions, and Canvas animations — no external libraries required

---

## ⌨️ Available Commands

Type any of these commands in the terminal input:

### Core Commands

| Command                               | Shorthand     | Description                                              |
| ------------------------------------- | ------------- | -------------------------------------------------------- |
| `help`                                | —             | List all available commands                              |
| `whoami`                              | —             | Display a brief introduction and current role            |
| `ls`                                  | —             | List files in the current portfolio directory            |
| `cat contact.txt`                     | `contact`     | Show contact information (Email, LinkedIn, GitHub)       |
| `cat skills.json`                     | `skills`      | Display tech stack and skills in JSON format             |
| `./show_experience.sh`                | `experience`  | Show work history, sorted by most recent                 |
| `./show_experience.sh --latest-first` | —             | Same as above (explicit flag)                            |
| `tail -n 5 education.log`             | `education`   | Display education history                                |
| `ls -la ./academic_archive/`          | `archive`     | List academic projects with links to source files        |
| `./deploy_profile.sh`                 | —             | Display full profile (prompts `y/n` confirmation first)  |
| `clear`                               | —             | Clear the terminal screen                                |
| `history`                             | —             | Show previously entered commands with index numbers      |
| `pwd`                                 | —             | Print current working directory path                     |
| `date`                                | —             | Print current date and time                              |
| `neofetch`                            | `fastfetch`   | Show system/OS info in neofetch style                    |
| `cowsay [text]`                       | —             | Have an ASCII cow say something (default: welcome msg)   |
| `reboot`                              | `shutdown`    | Trigger a simulated shutdown and reload the page         |
| `exit`                                | —             | Simulate logout and reload the page                      |

### Easter Eggs 🥚

| Command         | What happens                                                              |
| --------------- | ------------------------------------------------------------------------- |
| `matrix`        | Transforms the page into a Matrix-style digital rain (click/key to stop)  |
| `bongo`         | Summons the Bongo Cat 🐱                                                  |
| `cat .env`      | Gets denied — secrets are in CI/CD, not plaintext 😎🔒                   |
| `sudo rm -rf /` | Triggers the Jurassic Park trap 🦕 (also: `sudo rm -rf *`, `rm -rf /`)   |
| `sudo [any]`    | "You are not in the sudoers file. This incident will be reported. 🚨"     |
| `cd [any]`      | "Permission denied. You are trapped in my portfolio! 🚪🔒"               |

---

## 🚀 Deploy to GitHub Pages

This project is a static file — deploying to GitHub Pages is straightforward.

### Option A: GitHub Actions (Recommended)

A workflow is already included at `.github/workflows/deploy.yml`. Just push to `main` and GitHub will deploy automatically.

1. Go to your repository → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Push to `main` — the site will be live at `https://<username>.github.io/<repo-name>/`

### Option B: Deploy from Branch

1. Go to **Settings** → **Pages**
2. Under **Build and deployment**, set **Source** to `Deploy from a branch`
3. Select branch `main` (or `master`) and folder `/ (root)`, then click **Save**
4. Wait 1–2 minutes — GitHub will provide your live site URL

---

## Author

**Jirayu Mool-ang** — Senior Backend Developer
