# D2L Brightspace APIs 🛠️

**Free, ready-to-use tools for D2L Brightspace — just download, upload, and go.**

[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-ea4aaa?logo=github)](https://github.com/sponsors/jonsorr)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Brightspace](https://img.shields.io/badge/Platform-D2L%20Brightspace-orange)

Every tool in this repository is a **single, self-contained HTML file** that runs inside your Brightspace site using the **Brightspace (Valence) API**. Upload the file, open it, and it works with your existing Brightspace login. You don't need a server, an install, an API key, or a developer.

---

## 📑 Table of Contents

- [Why These Tools?](#-why-these-tools)
- [Available Tools](#-available-tools)
- [Quick Start](#-quick-start)
- [Configuration](#-configuration)
- [Permissions](#-permissions)
- [Security & Privacy](#-security--privacy)
- [Troubleshooting](#-troubleshooting)
- [Support This Project](#-support-this-project)
- [Contributing](#-contributing)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 💡 Why These Tools?

Brightspace is powerful, but many everyday admin and course tasks still mean clicking through hundreds of screens, waiting on support tickets, or paying for vendor add-ons and custom development. That can cost a school **thousands of dollars a year** in licenses and staff time.

These tools handle many of those jobs for free:

- ✅ **No cost.** Free for every institution, forever.
- ✅ **No setup.** One HTML file per tool, with no servers or installs.
- ✅ **No API keys.** Each tool uses your existing Brightspace session.
- ✅ **No coding required.** Most tools work as-is or need a one-line change.
- ✅ **Transparent.** All code is open, readable, and yours to review.

---

## 🧰 Available Tools

> **Status key:** ✅ Available · 🚧 In progress · 📅 Planned

### Administration

| Tool | What it does | Status |
|------|--------------|--------|
| **Notification Settings Updater** | Bulk-update users' Summary Notification settings | 📅 |
| **Correct User Emails** | Fix or clear external email addresses by org role to stop bounce-backs | 📅 |
| **Create Org Units** | Create Departments, Course Templates, and Course Offerings in bulk | 📅 |
| **Set Active Status** | Set many org units to Active or Inactive at once | 📅 |
| **Delete Groups** | Bulk-delete groups and group categories across courses | 📅 |
| **Adjusted Grade Config** | Bulk-set the `ReleaseAdjustedGrade` config variable across courses | 📅 |

### Course Batch Tools

| Tool | What it does | Status |
|------|--------------|--------|
| **Copy Course Batch** | Copy a master shell into many course offerings in one run | 📅 |
| **Enrollment Batch CSV** | Build an enrollment CSV by picking courses, users, and a role | 📅 |
| **Post News Batch** | Post one announcement into many courses at once | 📅 |

### Reports

| Tool | What it does | Status |
|------|--------------|--------|
| **Instructor Last Accessed** | Show each course's instructors and when they last accessed it | 📅 |
| **Attendance Check** | Check whether courses have attendance registers and whether attendance is being taken | 📅 |
| **Empty Course Check** | Find active courses with nothing in Content | 📅 |
| **Template Audit** | Check courses for required Content modules and flag outdated ones | 📅 |
| **Department Tools Dashboard** | Run several reports from one page after a single course scan | 📅 |

### Widgets & Course Pages

| Tool | What it does | Status |
|------|--------------|--------|
| **My Courses Widget** | Homepage widget with semester tabs and role-based course cards | 📅 |
| **Welcome Window** | Course homepage pop-up that shows unread announcements | 📅 |
| **Visual Table of Contents** | Visual, card-style navigation for course content | 📅 |
| **Assignment Schedule** | Course page that lists every dated activity, grouped by due date | 📅 |

---

## 🚀 Quick Start

### 1. Download a tool
Open the tool's folder in this repository and download the `.html` file (click the file, then **Download raw file**).

### 2. Upload it to Brightspace
Pick the option that fits the tool:

**Option A: Admin and report tools (recommended)**
1. Go to an admin or sandbox course you control.
2. Open **Course Admin → Manage Files** and upload the `.html` file.
3. In **Content**, add the file as a topic (**Upload / Create → Add from Manage Files**).
4. Restrict the topic so only admins can see it.

**Option B: Homepage and course widgets**
1. Upload the `.html` file to **Manage Files** in the course or org unit.
2. Create a custom widget (**Course Admin → Widgets → Create Widget**).
3. Embed the file in the widget with an `<iframe>` pointing to its file path.
4. Add the widget to your homepage layout.

### 3. Open it and go
Open the topic or page. The tool runs as **you**, using your current Brightspace login and permissions.

> 💡 **Tip:** Always test a new tool in a **sandbox course or test environment** first, especially tools that change data in bulk.

---

## ⚙️ Configuration

Most tools work without any changes. If a tool needs settings, they are grouped together at the **top of the file** in a clearly marked block:

```javascript
// ===== CONFIGURATION — edit these values for your institution =====
const CONFIG = {
  ORG_UNIT_ID: 6606,          // Your org's root org unit ID
  LP_VERSION: "1.46",         // Learning Platform API version
  LE_VERSION: "1.82",         // Learning Environment API version
};
// ===================================================================
```

Open the file in any text editor (Notepad, TextEdit, VS Code), change the values, save, and re-upload.

**Finding your values:**
- **Org Unit ID:** Shown in the URL when you view an org unit or course (for example, `/d2l/home/6606`).
- **API versions:** Visit `https://YOUR-SCHOOL.brightspace.com/d2l/api/versions/` while logged in.

Each tool's own README lists any settings specific to that tool.

---

## 🔐 Permissions

Each tool can do only what **your Brightspace role** is allowed to do. If your role can't perform an action in the normal Brightspace interface, the tool can't perform it either.

- **Report tools** usually need permission to view classlists, content, and org units.
- **Admin tools** usually need administrator-level permissions for the area they change, such as users, org units, or groups.
- **Widgets** usually need only normal student or instructor access.

Each tool's own README lists the permissions it needs.

---

## 🛡️ Security & Privacy

- **Runs in your browser.** No data is sent to any outside server. Everything stays between your browser and your Brightspace site.
- **Uses your session.** Tools authenticate with your existing Brightspace login and the built-in security token. No passwords or API keys are stored in the files.
- **Open source.** You or your IT team can read every line of code before using it.
- **Bulk changes ask first.** Tools that change data show a preview and ask you to confirm before making changes.

> ⚠️ Review your institution's policies before deploying custom tools, and check with your IT or LMS team if you're unsure.

---

## 🧯 Troubleshooting

| Problem | Likely cause | Fix |
|---------|--------------|-----|
| `403 Forbidden` errors | Your role lacks permission | Ask your Brightspace admin to check your role's permissions |
| `404 Not Found` errors | Wrong org unit ID or API version | Double-check the values in the configuration block |
| Blank page or nothing loads | The file was opened from your computer instead of Brightspace | Open the tool from inside Brightspace, not from your Downloads folder |
| Tool worked before but stopped | A Brightspace update changed the API | Check this repo for an updated version, or [open an issue](../../issues) |

Still stuck? [Open an issue](../../issues) and include the tool name, the error message, and the steps you took.

---

## 💙 Support This Project

These tools are free and always will be. Building and testing them still costs money for AI development tools, testing environments, hosting, and API access.

**If a tool saved your team time or money, please consider sponsoring.** Every sponsorship helps pay for more tools, faster updates, and better documentation for the whole Brightspace community.

[![Sponsor on GitHub](https://img.shields.io/badge/Sponsor%20on%20GitHub-%E2%9D%A4-ea4aaa?style=for-the-badge&logo=github)](https://github.com/sponsors/jonsorr)

### 🌟 Sponsors

Thank you to everyone who supports this work!

<!-- SPONSORS-START -->
*Be the first sponsor!*
<!-- SPONSORS-END -->

### 🏫 Institutional Partners

<!-- PARTNERS-START -->
*Your institution could be listed here.*
<!-- PARTNERS-END -->

---

## 🤝 Contributing

Contributions are welcome! Ways to help:

- 🐛 **Report bugs** by [opening an issue](../../issues)
- 💡 **Suggest a tool** by opening an issue with the `tool request` label
- 📝 **Improve documentation** by fixing typos, adding screenshots, or clarifying steps
- 🔧 **Submit code** by forking the repo, making your changes, and opening a pull request

When you submit a tool, please keep it to **one self-contained HTML file** with any settings in a configuration block at the top.

---

## 📄 License

This project is licensed under the **MIT License**. You're free to use, modify, and share these tools, including at your institution. See [LICENSE](LICENSE) for details.

---

## ⚖️ Disclaimer

This is an independent community project. It is **not affiliated with, endorsed by, or supported by D2L Corporation**. D2L and Brightspace are trademarks of D2L Corporation.

These tools are provided **as-is, without warranty**. Always test in a non-production environment first, and use them at your own risk.

---

<p align="center">
  Made with 💙 for the Brightspace community<br>
  <a href="https://github.com/sponsors/jonsorr">Sponsor</a> ·
  <a href="../../issues">Report an Issue</a> ·
  <a href="../../issues/new">Request a Tool</a>
</p>
