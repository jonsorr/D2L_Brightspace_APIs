# D2L Brightspace APIs 🛠️

**Free, ready-to-use tools for D2L Brightspace — just download, upload, and go.**

[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-ea4aaa?logo=github)](https://github.com/sponsors/jonsorr)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Brightspace](https://img.shields.io/badge/Platform-D2L%20Brightspace-orange)

Every tool in this repository is a **single, self-contained HTML file** that runs inside your Brightspace site using the **Brightspace (Valence) API**. Upload the file, open it, and it works with your existing Brightspace login. You don't need a server, an install, an API key, or a developer.

---

## 📑 Table of Contents

- [Why These Tools?](#-why-these-tools)
- [Proven in Production](#-proven-in-production)
- [Available Tools](#-available-tools)
- [Quick Start](#-quick-start)
- [Configuration](#-configuration)
- [Permissions](#-permissions)
- [Security & Privacy](#-security--privacy)
- [Troubleshooting](#-troubleshooting)
- [Roadmap](#-roadmap)
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

## 🏭 Proven in Production

These aren't experiments or demos. **Every tool listed below is running live in a production Brightspace environment at a college**, doing real work for staff, faculty, and students every day.

| | |
|---|---|
| 🧰 **Tools running live in production** | 21 |
| ⚡ **Largest bulk run designed for** | 50,000+ course offerings in a single pass |
| 📚 **Largest course list handled** | 100,000+ courses loaded and paged in the browser |
| 🔑 **API keys required** | 0 |

---

## 🧰 Available Tools

> **Status key:** ✅ Published in this repo · 📦 Live in production, being prepared for release
>
> Every tool is already running in production. Tools move from 📦 to ✅ as each one is cleaned up, made configurable for any institution, and documented.

### 🔧 Admin Tools
*Bulk tools for LMS administrators: change thousands of records in minutes instead of days.*

| Tool | File | What it does | Status |
|------|------|--------------|--------|
| **Summary Notification Settings Updater** | `d2l_notification_updater.html` | Paste a list of usernames and bulk-update their Summary Notification settings, with parallel workers for very large lists | 📦 |
| **Correct User Emails** | `d2l_correct_user_emails.html` | Stop bounce-backs by correcting user email addresses in bulk based on each user's role | 📦 |
| **Adjusted Grade Config Updater** | `adjusted-grade-config-update.html` | Bulk-set the Release Adjusted Final Grade setting across 50,000+ courses, with preview mode and a one-course test run | 📦 |
| **Create Org Units** | `d2l_create_org_units.html` | Create Departments, Course Templates, and Course Offerings in bulk | 📦 |
| **Set Active Status** | `d2l_set_active_status.html` | Set Divisions, Departments, Templates, Semesters, and Courses Active or Inactive, built to handle 100,000+ courses | 📦 |
| **Delete Groups** | `d2l_delete_groups.html` | Clean up thousands of groups and group categories, deleting a group only after checking that no Content, Quiz, Discussion, or Assignment uses it | 📦 |

### 🏫 Department Tools
*Reports and batch tools for deans, department chairs, and program coordinators.*

| Tool | File | What it does | Status |
|------|------|--------------|--------|
| ⭐ **Department Tools Dashboard** | `department-dashboard.html` | All 8 department tools on one page, sharing **one** course and term scan instead of eight | 📦 |
| **Department Grades** | `d2l_dean_grade_widget.html` | Every active course in a department, with counts of at-risk and not-passing students, matched to Brightspace's own grade math | 📦 |
| **Course Readiness Audit** | `course-content-check.html` | Find course sections with nothing in Content before students arrive | 📦 |
| **Course Template Audit** | `course-template-audit.html` | Check courses for the Content modules your template requires and flag outdated ones | 📦 |
| **Attendance Check** | `course-attendance-check.html` | Report attendance registers, session counts, and whether attendance is being marked | 📦 |
| **Last Date Instructor Accessed** | `course-instructor-access.html` | Show when each faculty member last opened each course, in color-coded groups you can click to filter | 📦 |
| **Copy Course Batch** | `course-copy-batch.html` | Copy one model course into many course offerings in a single run, with an option to target only empty courses | 📦 |
| **Enrollment Batch CSV Builder** | `course-enrollment-batch.html` | Build a ready-to-upload enrollment CSV: pick courses, enter people, choose roles | 📦 |
| **Post News Batch** | `course-news-batch.html` | Write an announcement once and post it into many courses, with a rich-text editor and protection against duplicate posts | 📦 |

### 🏠 Homepage Widgets
*Student- and instructor-facing widgets that live on Brightspace homepages.*

| Tool | File | What it does | Status |
|------|------|--------------|--------|
| **Student Grade Widget** | `d2l_grade_widget.html` | Current grade with a ring chart, a category breakdown, the lowest and highest possible final grade, and a privacy screen | 📦 |
| **Instructor Grade Widget** | `d2l_instructor_grade_widget.html` | The whole class at a glance in five performance groups, with one-click email links; matches Brightspace's Class Progress exactly | 📦 |
| **My Courses Widget** | `d2l_my_courses_widget.html` | Past / Last / This / Next Semester tabs with course cards based on your role | 📦 |
| **Welcome Window** | `mtc-welcome-window-widget.html` | Course homepage pop-up that shows unread Announcements pages, with no instructor setup | 📦 |
| **Visual Table of Contents** | `visual-toc-widget.html` | Course modules shown as visual tiles with progress tracking; ADA / WCAG 2.1 AA reviewed | 📦 |

### 📄 Content Page Templates
*Ready-made pages that instructors drop into a course's Content area.*

| Tool | File | What it does | Status |
|------|------|--------------|--------|
| **Automated Assignment Schedule** | `90_Automated_Assignment_Builder.html` | A schedule that builds itself: every dated activity from Content, Assignments, Quizzes, and Discussions, grouped by due date, with the next group due highlighted | 📦 |

---

## 🚀 Quick Start

### 1. Download a tool
Open the tool's folder in this repository and download the `.html` file (click the file, then **Download raw file**).

### 2. Upload it to D2L Brightspace

#### Part 1: Store the HTML files in the D2L Public Files area

1. Sign in to D2L as an **Admin** or **SuperAdmin**.
2. Click the **Admin Tools** (gear) icon.
3. Open the **Public Files** tool.
4. Create a folder for each category of HTML files. For example:
   - `Admin_Pages`
   - `Department_Tools`
   - `Homepage_Widgets`
   - `Content_Templates`
5. Upload each HTML file from this repository into the matching folder.

Files in Public Files are served from `/shared/`. For example, a file uploaded to the `Admin_Pages` folder is at:

```
https://YOUR-BRIGHTSPACE-URL/shared/Admin_Pages/adjusted-grade-config-update.html
```

#### Part 2: Use the HTML files

<details open>
<summary><strong>A: Admin Tools and Department Tools</strong></summary>

**To show the tools on a navbar, create a custom link:**

1. Sign in to D2L as an **Admin** or **SuperAdmin**.
2. Click the **Admin Tools** (gear) icon.
3. Open the **Navigation & Themes** tool.
4. Choose the **Custom Links** tab.
5. Click **Create Link**.
6. Enter a **name** and the **URL**, then click **Save**. For example:
   `https://YOUR-BRIGHTSPACE-URL/shared/Admin_Pages/adjusted-grade-config-update.html`
7. Add the new link to your navbar.

**To show the tools on a homepage, create a custom widget:**

1. Sign in to D2L as an **Admin** or **SuperAdmin**.
2. Click the **Admin Tools** (gear) icon.
3. Open the **Homepage Management** tool.
4. Choose the **Widgets** tab.
5. Click **Create Widget**.
6. Enter a **name**, then open the **Content** tab.
7. Use the HTML Editor to build a list of links to the tools, using the same URL structure as the example above. Set each link to **open in a new window**.
8. Click **Save and Close**, then add the widget to your homepage.

> 🔒 **Note:** Use **release conditions** on the links or widgets to control which roles can see them.

</details>

<details open>
<summary><strong>B: Homepage Widgets</strong></summary>

1. Sign in to D2L as an **Admin** or **SuperAdmin**.
2. Click the **Admin Tools** (gear) icon.
3. Open the **Homepage Management** tool.
4. Choose the **Widgets** tab.
5. Click **Create Widget**.
6. Enter a **name**, then open the **Content** tab.
7. Click the **Source Code** option on the toolbar.
8. Add an `<iframe>` that points to the HTML file. For example:
   ```html
   <iframe src="/shared/Homepage_Widgets/d2l_instructor_grade_widget.html" style="width: 100%;" height="437" scrolling="no"></iframe>
   ```
9. Click **Save**, then **Save and Close**.
10. Add the widget to your homepage.

Adjust the `height` value to fit each widget.

> 🔒 **Note:** Use **release conditions** to control which roles can see each widget.

</details>

<details open>
<summary><strong>C: Content Page Templates</strong></summary>

Content page templates must be uploaded to the **same folder as your other Content templates**.

To find that folder, check this setting in the **Config Variable Browser**:

```
d2l.Tools.Content.TemplatePath   (Org Unit)
```

For example, if it's set to `/shared/Content_Templates/`, upload the template into the `Content_Templates` folder in **Public Files**. Instructors can then add it to a course from the Content tool's document templates.

</details>

### 3. Open it and go
Open the link, widget, or page. Each tool runs as **the signed-in user**, using that person's Brightspace login and permissions.

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
- **Privacy screens on grade widgets.** Grade widgets keep grade data hidden until the user chooses to show it, so grades aren't shown on a projector or shared screen by accident.
- **Accessible by design.** Student-facing widgets are built to ADA and WCAG 2.1 AA standards.

### Built to be reliable
- **Automatic API version detection.** Tools ask your Brightspace site which API versions it supports, so they keep working after Brightspace updates.
- **Built-in rate limiting.** Tools slow down automatically when Brightspace asks them to, retry safely, and never post the same item twice.
- **Built for scale.** Bulk tools use parallel workers with live progress, speed, and time-remaining estimates.

> ⚠️ Review your institution's policies before deploying custom tools, and check with your IT or LMS team if you're unsure.

---

## 🧯 Troubleshooting

| Problem | Likely cause | Fix |
|---------|--------------|-----|
| `403 Forbidden` errors | Your role lacks permission | Ask your Brightspace admin to check your role's permissions |
| `404 Not Found` errors | Wrong org unit ID or API version | Double-check the values in the configuration block |
| Blank page or nothing loads | The file was opened from your computer instead of Brightspace | Open the tool from its `/shared/` URL inside Brightspace, not from your Downloads folder |
| Tool worked before but stopped | A Brightspace update changed the API | Check this repo for an updated version, or [open an issue](../../issues) |

Still stuck? [Open an issue](../../issues) and include the tool name, the error message, and the steps you took.

---

## 🗺️ Roadmap

1. **Publish every production tool here.** Each one is being cleaned up, with institution-specific values moved into a simple settings block at the top of the file.
2. **Documentation for every tool.** A setup guide, a permissions list, and screenshots.
3. **New tools.** Sponsors at the $10/month tier and above vote on what gets built next. Anyone can [suggest a tool](../../issues/new).

---

## 💙 Support This Project

These tools are free and always will be. Building and testing them still costs money for AI development tools, testing environments, hosting, and API access.

**🎯 Current goal: $150/month**, enough to cover the core development tools behind every release.

**If a tool saved your team time or money, please consider sponsoring.** Every sponsorship helps pay for more tools, faster updates, and better documentation for the whole Brightspace community.

[![Sponsor on GitHub](https://img.shields.io/badge/Sponsor%20on%20GitHub-%E2%9D%A4-ea4aaa?style=for-the-badge&logo=github)](https://github.com/sponsors/jonsorr)
[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypal)](https://paypal.me/jonsorr)

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
