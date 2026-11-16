# Interactive Network Troubleshooting Workspace

A local-first, CompTIA-inspired troubleshooting workspace for GitHub Pages and Jekyll.

## Features
- Multi-select incidents: no internet, email server connectivity, slow file transfers
- Expandable six-step checklist with task completion tracking
- Issue-specific branching diagnostics with pros, limitations and next steps
- Multiple named incident sessions, automatically saved in the browser using `localStorage`
- JSON export/import for portable backups
- Blank and completed print views (browser Print → Save as PDF also works)
- No external libraries, account, analytics, server or API calls

## Deploy to GitHub Pages

1. Copy the **contents** of this folder into a directory such as `network-troubleshooting/` in your Jekyll GitHub Pages repository.
2. Commit `index.md` and the `assets/` directory.
3. Visit `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/network-troubleshooting/` (or `/network-troubleshooting/` for a user site).
4. The `layout: null` front matter prevents a Jekyll theme from wrapping the full HTML page.

You can also preview the page locally by serving the folder using `python -m http.server 8000`, then opening `http://localhost:8000/`. The browser may restrict storage when opened directly from `file://`.

## Privacy and data retention

Data is stored only in the current browser's local storage. It is **not synchronized across devices**, and clearing browser storage or using private browsing may erase it. Export JSON regularly and avoid entering passwords, private employee data, credentials or sensitive packet captures. JSON exports contain the entered notes in plaintext; handle them securely.

Import replaces the locally saved session collection after confirmation. The tool does not automatically execute commands or determine confirmed root causes. Always follow local security and change-management procedures.

## Files
- `index.md`: Jekyll-compatible interactive page
- `assets/troubleshooting.css`: styling and print views
- `assets/troubleshooting.js`: session management, branching, exports and UI

## Learning disclaimer
This is a training and operational aid, not a replacement for organizational incident response procedures. Device command availability varies by platform and software version.
