# Terminal-Style Developer Portfolio

> A geeky, interactive Command Line Interface (CLI) style portfolio designed for Backend Developers and Software Architects.

**🌐 Live Website:** [https://iots1.github.io/me/](https://iots1.github.io/me/)

A portfolio that runs in the web browser, simulating a Linux/Mac terminal environment — built as a **single static HTML file**. Present your work history, skills, and projects with style. Perfect for Geeks, DevOps engineers, and Backend Developers.

---

## ✨ Features

| Feature                            | Description                                                                                                                     |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Interactive CLI**                | A real input field where you can type and execute commands, just like a terminal                                                |
| **Command History**                | Press ⬆️ / ⬇️ arrow keys to cycle through previously entered commands                                                           |
| **Draggable Window**               | Click and drag the header bar (near the red/yellow/green dots) to reposition the terminal window                                |
| **Boot Sequence Effect**           | Simulates a startup script with loading animations and ASCII Art logo on first load — press `Space` to pause or `Enter` to skip |
| **Built-in Presentation (Iframe)** | Opens a Resume or Portfolio (Canva) in a full-screen overlay directly on the page — press `Ctrl+X` or `Esc` to close            |
| **Easter Eggs 🥚**                 | Hidden hacker-style surprises — try typing secret commands to discover them!                                                    |

---

## 🛠️ Tech Stack

- **HTML5** — entire structure lives in a single `index.html` file
- **Tailwind CSS (CDN)** — layout and styling with a GitHub Dark Dimmed theme
- **Vanilla JavaScript** — all logic for typing, window dragging, terminal functions, and Canvas animations — no external libraries required

---

## ⌨️ Available Commands

Type any of these commands in the terminal input:

| Command                      | Description                                                       |
| ---------------------------- | ----------------------------------------------------------------- |
| `help`                       | List all available commands                                       |
| `whoami`                     | Display a brief introduction and current role                     |
| `cat contact.txt`            | Show contact information (Email, LinkedIn, GitHub)                |
| `cat skills.json`            | Display tech stack and skills in JSON format                      |
| `./show_experience.sh`       | Show work history, sorted by most recent                          |
| `tail -n 5 education.log`    | Display education history                                         |
| `ls -la ./academic_archive/` | List academic projects with links to source files                 |
| `./deploy_profile.sh`        | Display full profile information in one go                        |
| `clear`                      | Clear the terminal screen                                         |
| `exit`                       | Simulate logout and reload the page                               |
| `matrix`                     | 🥚 _[Secret]_ Transform the page into a Matrix-style digital rain |
| `sudo rm -rf /`              | 🥚 _[Secret]_ Try it and find out...                              |

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
