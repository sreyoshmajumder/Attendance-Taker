<!-- HEADER BANNER -->
<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:001a0a,40:003320,70:004d2e,100:0a0a0f&height=240&section=header&text=📋%20Attendance%20Taker%20System&fontSize=40&fontColor=00ff88&fontAlignY=40&desc=Smart%20Attendance%20Management%20for%20Teachers%20%26%20Admins%20%7C%20Pure%20HTML%20%7C%20Zero%20Dependencies&descAlignY=62&descColor=4ade80&animation=fadeIn)

<br/>

[![HTML5](https://img.shields.io/badge/HTML5-0a0a0f?style=for-the-badge&logo=html5&logoColor=ff6347)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-0a0a0f?style=for-the-badge&logo=css3&logoColor=00ff88)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/Vanilla%20JS-0a0a0f?style=for-the-badge&logo=javascript&logoColor=ffd700)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Single File](https://img.shields.io/badge/Single%20File%20App-171%20lines-0a0a0f?style=for-the-badge&logoColor=00ff88)](https://github.com/sreyoshmajumder/Attendance-Taker)
[![No Backend](https://img.shields.io/badge/No%20Backend-100%25%20Frontend-0a0a0f?style=for-the-badge&logoColor=39ff14)](https://github.com/sreyoshmajumder/Attendance-Taker)
[![License](https://img.shields.io/badge/License-MIT-0a0a0f?style=for-the-badge&logoColor=00ff88)](LICENSE)

<br/>

> **📋 A complete, zero-dependency attendance management system for teachers and admins — built in a single HTML file. Add students, mark them present or absent day by day, and instantly see days present, days absent, and live attendance percentage. No server, no database, no install — just open and use.**

<br/>

![Students](https://img.shields.io/badge/Tracks-Unlimited%20Students-00ff88?style=flat-square&labelColor=0a0a0f)
![Metrics](https://img.shields.io/badge/Shows-Days%20Present%20%7C%20Absent%20%7C%20Percentage-ffd700?style=flat-square&labelColor=0a0a0f)
![Deploy](https://img.shields.io/badge/Deploy-Any%20Browser-4ade80?style=flat-square&labelColor=0a0a0f)
![Size](https://img.shields.io/badge/Size-5.32%20KB-ff2d78?style=flat-square&labelColor=0a0a0f)

</div>

---

## 📋 Table of Contents

| | Section |
|---|---|
| 🎯 | [Problem Statement](#-problem-statement) |
| ✨ | [Features](#-features) |
| 🏗️ | [System Architecture](#-system-architecture) |
| 🔄 | [User Workflow](#-user-workflow) |
| ⚙️ | [JavaScript Functions](#-javascript-functions) |
| 📐 | [State Management](#-state-management) |
| 🧮 | [Attendance Formula](#-attendance-calculation-formula) |
| 🎨 | [UI Component Map](#-ui-component-map) |
| 🗂️ | [Project Structure](#-project-structure) |
| 🚀 | [Quick Start](#-quick-start) |
| 💡 | [Usage Guide](#-usage-guide) |
| 🔭 | [Roadmap](#-future-roadmap) |

---

## 🎯 Problem Statement

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   Tracking student attendance manually is tedious, error-prone,          ║
║   and time-consuming for teachers managing large classrooms.             ║
║                                                                          ║
║   Traditional methods fail because:                                      ║
║   ❌  Paper registers get lost or damaged                                ║
║   ❌  Calculating percentages by hand takes time and causes errors       ║
║   ❌  No instant visibility into who is below attendance threshold       ║
║   ❌  Expensive dedicated software requires installation & accounts      ║
║                                                                          ║
║   ► Attendance Taker solves this instantly:                              ║
║                                                                          ║
║   ✅  Type student name  ──▶  Click "Add Student"                       ║
║   ✅  Click "Mark Present" or "Mark Absent" for each student             ║
║   ✅  Days present, days absent & percentage update instantly            ║
║   ✅  Works in any browser — no install, no login, no cost              ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

</div>

---

## ✨ Features

| ⚡ Feature | 📋 Description |
|---|---|
| ➕ **Add Students** | Type any student name and add them instantly to the attendance table |
| ✅ **Mark Present** | One-click green button increments days present for that student |
| ❌ **Mark Absent** | One-click red button increments days absent for that student |
| 📊 **Auto Percentage** | Attendance % = `(present / total) × 100` — updates live on every click |
| 🔢 **Working Days** | Editable total working days input — auto-recalculates percentage on change |
| 📋 **Tabular View** | Clean table with Name · Total Days · Days Present · Days Absent · % · Actions |
| 🔁 **Unlimited Students** | Add as many students as needed — no cap, no pagination |
| 🚫 **Empty Name Guard** | Alerts teacher if they try to add a student with a blank name |
| ⚡ **Instant Load** | 5.32 KB single file — opens in milliseconds, zero network calls |
| 📱 **Responsive** | `width: 80%; margin: auto` — works cleanly on any screen size |

---

## 🏗️ System Architecture

```
╔═══════════════════════════════════════════════════════════════════════════════╗
║              ATTENDANCE TAKER SYSTEM — COMPLETE ARCHITECTURE                  ║
╚═══════════════════════════════════════════════════════════════════════════════╝

  ┌────────────────────────────────────────────────────────────────────────┐
  │                     SINGLE FILE APPLICATION                            │
  │              "attendance taker system.html"  (171 lines · 5.32 KB)     │
  │                                                                        │
  │  ┌──────────────────┐  ┌───────────────────┐  ┌──────────────────┐   │
  │  │     <head>       │  │     <body>         │  │    <script>      │   │
  │  │                  │  │                    │  │                  │   │
  │  │  • UTF-8 charset │  │  • <h1> App Title  │  │  studentId = 0   │   │
  │  │  • Viewport meta │  │  • .add-student    │  │                  │   │
  │  │  • <title>       │  │    Input + Button  │  │  addStudent()    │   │
  │  │  • Inline <style>│  │  • #attendanceTable│  │  markAttendance()│   │
  │  │    (67 lines CSS)│  │    thead + tbody   │  │  updatePercentage│   │
  │  └──────────────────┘  └───────────────────┘  └──────────────────┘   │
  └────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
  ┌────────────────────────────────────────────────────────────────────────┐
  │                         IN-MEMORY STATE                                │
  │                    (lives in DOM — no JS objects)                      │
  │                                                                        │
  │   studentId counter  ──▶  auto-increments on each addStudent() call   │
  │                                                                        │
  │   Per student row (in DOM):                                            │
  │   ┌──────────────────────────────────────────────────────────────┐    │
  │   │  <input id="total-N">     ← editable total working days      │    │
  │   │  <td    id="present-N">   ← days present counter (innerText) │    │
  │   │  <td    id="absent-N">    ← days absent counter (innerText)  │    │
  │   │  <td    id="percentage-N">← live % display (innerText)       │    │
  │   └──────────────────────────────────────────────────────────────┘    │
  │                                                                        │
  │   State is read/written directly from the DOM via getElementById()     │
  └────────────────────────────────────────────────────────────────────────┘
                                      │
                     ┌────────────────┼─────────────────┐
                     ▼                ▼                  ▼
          ┌──────────────┐  ┌──────────────────┐  ┌─────────────────┐
          │ addStudent() │  │ markAttendance() │  │updatePercentage │
          │              │  │                  │  │                 │
          │ Reads:       │  │ Reads:           │  │ Reads:          │
          │ #studentName │  │ total-N          │  │ total-N (input) │
          │              │  │ present-N        │  │ present-N       │
          │ Creates:     │  │ absent-N         │  │                 │
          │ New <tr> row │  │                  │  │ Writes:         │
          │ with inputs  │  │ Writes:          │  │ percentage-N    │
          │ and buttons  │  │ present-N        │  │                 │
          │              │  │ absent-N         │  │ Formula:        │
          │ Appends to:  │  │ total-N (input)  │  │ (P/T)×100      │
          │ tbody        │  │ percentage-N     │  │ .toFixed(2)     │
          └──────────────┘  └──────────────────┘  └─────────────────┘
```

---

## 🔄 User Workflow

```
╔═══════════════════════════════════════════════════════════════════════════════╗
║                    COMPLETE USER WORKFLOW — STEP BY STEP                      ║
╠═══════════════════════════════════════════════════════════════════════════════╣
║                                                                               ║
║  PHASE 1 ── SETUP                                                             ║
║  ─────────────────────────────────────────────────────────────────────────   ║
║  Teacher opens "attendance taker system.html" in any browser                 ║
║  └──▶  Page renders instantly with:                                          ║
║         • Title: "Attendance Taker System"                                   ║
║         • Input box: "Enter Student Name"                                    ║
║         • Button: "Add Student"                                              ║
║         • Empty table with 6 column headers                                  ║
║                                                                               ║
║  PHASE 2 ── ADD STUDENTS                                                      ║
║  ─────────────────────────────────────────────────────────────────────────   ║
║  For each student in the class:                                               ║
║    1. Type student name in the input box                                      ║
║    2. Click "Add Student"  ──▶  addStudent() fires                          ║
║    3. Validation: blank name?  ──▶  alert("Please enter a student name.")   ║
║    4. studentId++ (1, 2, 3, ...)                                             ║
║    5. New row appended to table:                                              ║
║       ┌─────────────┬──────────┬─────────┬────────┬──────┬──────────────┐   ║
║       │ Student Name│ Total: 0 │ Pres: 0 │ Abs: 0 │  0%  │ ✅ ❌ Btns  │   ║
║       └─────────────┴──────────┴─────────┴────────┴──────┴──────────────┘   ║
║    6. Input box clears automatically                                          ║
║                                                                               ║
║  PHASE 3 ── MARK DAILY ATTENDANCE                                             ║
║  ─────────────────────────────────────────────────────────────────────────   ║
║  Each day (or each session), for every student:                               ║
║                                                                               ║
║    Click ✅ "Mark Present":                                                   ║
║    ├── present += 1                                                           ║
║    ├── total = present + absent  (auto-updated)                              ║
║    └── percentage = (present / total) × 100  (live)                         ║
║                                                                               ║
║    Click ❌ "Mark Absent":                                                    ║
║    ├── absent += 1                                                            ║
║    ├── total = present + absent  (auto-updated)                              ║
║    └── percentage = (present / total) × 100  (live)                         ║
║                                                                               ║
║  PHASE 4 ── MANUAL TOTAL ADJUSTMENT                                           ║
║  ─────────────────────────────────────────────────────────────────────────   ║
║  Teacher can directly edit "Total Working Days":                              ║
║    ├── Type a custom number (e.g. 30 for a full month)                       ║
║    ├── onchange event fires  ──▶  updatePercentage() called                 ║
║    └── percentage = (present / newTotal) × 100  (recalculated)              ║
║                                                                               ║
║  PHASE 5 ── READ RESULTS                                                      ║
║  ─────────────────────────────────────────────────────────────────────────   ║
║  Final table shows per student:                                               ║
║    ✅  Total Working Days  (editable)                                        ║
║    ✅  Days Present        (click-counted)                                   ║
║    ✅  Days Absent         (click-counted)                                   ║
║    ✅  Attendance %        (auto-calculated, 2 decimal places)               ║
║                                                                               ║
╚═══════════════════════════════════════════════════════════════════════════════╝
```

---

## ⚙️ JavaScript Functions

### `addStudent()` — Add a New Student Row

```javascript
function addStudent() {
    // 1. Read input value and trim whitespace
    const studentNameInput = document.getElementById('studentName');
    const studentName = studentNameInput.value.trim();

    // 2. Guard: block empty name submissions
    if (studentName === '') {
        alert('Please enter a student name.');
        return;
    }

    // 3. Increment global student ID counter
    studentId++;  // studentId starts at 0, becomes 1, 2, 3...

    // 4. Build new table row with dynamic IDs per student
    const tableBody = document.querySelector('#attendanceTable tbody');
    const row = document.createElement('tr');
    row.innerHTML = `
        <td>${studentName}</td>
        <td><input type="number" id="total-${studentId}"
                   class="editable" value="0" min="0"
                   onchange="updatePercentage(${studentId})"></td>
        <td id="present-${studentId}">0</td>
        <td id="absent-${studentId}">0</td>
        <td id="percentage-${studentId}">0%</td>
        <td>
            <button class="present"
                    onclick="markAttendance(${studentId}, true)">Mark Present</button>
            <button class="absent"
                    onclick="markAttendance(${studentId}, false)">Mark Absent</button>
        </td>
    `;

    // 5. Append row to table body
    tableBody.appendChild(row);

    // 6. Clear input for next student
    studentNameInput.value = '';
}
```

### `markAttendance(id, isPresent)` — Record Present / Absent

```javascript
function markAttendance(id, isPresent) {
    // 1. Get all 4 live DOM cells for this student
    const totalCell      = document.getElementById(`total-${id}`);      // <input>
    const presentCell    = document.getElementById(`present-${id}`);    // <td>
    const absentCell     = document.getElementById(`absent-${id}`);     // <td>
    const percentageCell = document.getElementById(`percentage-${id}`); // <td>

    // 2. Parse current values from DOM
    let present = parseInt(presentCell.innerText);
    let absent  = parseInt(absentCell.innerText);

    // 3. Increment the correct counter
    if (isPresent) {
        present += 1;   // ✅ Mark Present button
    } else {
        absent  += 1;   // ❌ Mark Absent button
    }

    // 4. Auto-update total = present + absent (cumulative)
    const total = present + absent;
    totalCell.value = total;

    // 5. Calculate percentage to 2 decimal places
    const percentage = ((present / total) * 100).toFixed(2);

    // 6. Write all values back to DOM
    presentCell.innerText    = present;
    absentCell.innerText     = absent;
    percentageCell.innerText = `${percentage}%`;
}
```

### `updatePercentage(id)` — Recalculate on Manual Total Edit

```javascript
function updatePercentage(id) {
    // 1. Read current total from input (teacher manually edited it)
    const totalCell      = document.getElementById(`total-${id}`);
    const presentCell    = document.getElementById(`present-${id}`);
    const percentageCell = document.getElementById(`percentage-${id}`);

    let total   = parseInt(totalCell.value);
    let present = parseInt(presentCell.innerText);

    // 2. Guard against division by zero
    const percentage = total > 0 ? ((present / total) * 100).toFixed(2) : 0;

    // 3. Update percentage display
    percentageCell.innerText = `${percentage}%`;
}
```

---

## 📐 State Management

```
  HOW STATE IS STORED — DOM AS DATABASE
  ════════════════════════════════════════════════════════════════════

  There is NO JavaScript object / array holding student data.
  All state lives directly in the DOM using dynamic element IDs.

  Global state:
  ┌─────────────────────────────────────────────────────────────┐
  │  let studentId = 0;   ← monotonically increasing counter    │
  └─────────────────────────────────────────────────────────────┘

  Per-student state (stored in DOM nodes, read via getElementById):
  ┌──────────────────────────┬──────────┬──────────────────────┐
  │  DOM Element             │  Tag     │  Value               │
  ├──────────────────────────┼──────────┼──────────────────────┤
  │  #total-{studentId}      │ <input>  │ .value  (number)     │
  │  #present-{studentId}    │ <td>     │ .innerText (number)  │
  │  #absent-{studentId}     │ <td>     │ .innerText (number)  │
  │  #percentage-{studentId} │ <td>     │ .innerText (string%) │
  └──────────────────────────┴──────────┴──────────────────────┘

  Example with 3 students added:

  studentId = 3

  DOM elements in memory:
  #total-1      value="22"   ← Student 1: 22 working days
  #present-1    innerText=18 ← Student 1: 18 present
  #absent-1     innerText=4  ← Student 1: 4 absent
  #percentage-1 innerText="81.82%"

  #total-2      value="22"
  #present-2    innerText=20
  #absent-2     innerText=2
  #percentage-2 innerText="90.91%"

  #total-3      value="5"    ← Student 3: only 5 days tracked
  #present-3    innerText=3
  #absent-3     innerText=2
  #percentage-3 innerText="60.00%"
```

---

## 🧮 Attendance Calculation Formula

```
  FORMULA ENGINE
  ════════════════════════════════════════════════════════════════════

  ► On markAttendance() click:
  ─────────────────────────────────────────────────────────────────
  total      = present + absent          (cumulative, auto-set)
  percentage = (present / total) × 100   (to 2 decimal places)

  ► On updatePercentage() — manual total edit:
  ─────────────────────────────────────────────────────────────────
  percentage = total > 0 ? (present / total) × 100 : 0
               └── Division-by-zero guard when total = 0

  ► .toFixed(2) — always 2 decimal places:
  ─────────────────────────────────────────────────────────────────
  18 present / 22 total  =  81.818181...%  →  "81.82%"
  20 present / 22 total  =  90.909090...%  →  "90.91%"
   3 present /  5 total  =  60.000000...%  →  "60.00%"

  ATTENDANCE STATUS REFERENCE:
  ─────────────────────────────────────────────────────────────────
  ≥ 75%   ██████████████████████░░  ✅  SAFE     — full attendance
  60–74%  ████████████████░░░░░░░░  ⚠️  WARNING  — at risk
  < 60%   ██████████░░░░░░░░░░░░░░  ❌  CRITICAL — may be detained
```

---

## 🎨 UI Component Map

```
  FULL PAGE LAYOUT  (171 lines · 5.32 KB)
  ════════════════════════════════════════════════════════════════════

  ┌─────────────────────────────────────────────────────────────────┐
  │                  Attendance Taker System  (h1)                  │
  │          color: #333 · text-align: center · margin: 20px        │
  └─────────────────────────────────────────────────────────────────┘

  ┌─────────────────────────────────────────────────────────────────┐
  │                  .add-student  (input row)                      │
  │                                                                 │
  │  ┌─────────────────────────────────┐  ┌─────────────────────┐  │
  │  │  <input id="studentName"        │  │    Add Student      │  │
  │  │   placeholder="Enter Student..  │  │    <button>         │  │
  │  │   padding: 5px                  │  │    onclick=         │  │
  │  │   margin-right: 10px            │  │    addStudent()     │  │
  │  └─────────────────────────────────┘  └─────────────────────┘  │
  └─────────────────────────────────────────────────────────────────┘

  ┌─────────────────────────────────────────────────────────────────┐
  │             #attendanceTable  (width: 100%)                     │
  │                                                                 │
  │  ┌──────────────┬────────────┬──────────┬────────┬──────┬────┐  │
  │  │ Student Name │ Total Days │  Present │ Absent │   %  │ Act│  │
  │  │   (th)       │   (th)     │   (th)   │  (th)  │ (th) │(th)│  │
  │  │  bg: #333    │            │          │        │      │    │  │
  │  │  color: white│            │          │        │      │    │  │
  │  ├──────────────┼────────────┼──────────┼────────┼──────┼────┤  │
  │  │  Alice       │  [  22  ] │    18    │   4    │81.82%│✅❌│  │
  │  │  Bob         │  [  22  ] │    20    │   2    │90.91%│✅❌│  │
  │  │  Charlie     │  [   5  ] │     3    │   2    │60.00%│✅❌│  │
  │  └──────────────┴────────────┴──────────┴────────┴──────┴────┘  │
  │                                                                 │
  │  ✅ .present button:  bg: #4CAF50 (green) · color: white        │
  │  ❌ .absent  button:  bg: #f44336 (red)   · color: white        │
  │  📝 .editable input:  bg: #eef · border: 1px #ccc              │
  └─────────────────────────────────────────────────────────────────┘

  CSS CLASS REFERENCE:
  ──────────────────────────────────────────────────────────────────
  body          bg: #f4f4f9 · font: Arial
  .container    width: 80% · margin: auto
  h1            text-align: center · color: #333
  table         width: 100% · border-collapse: collapse
  th            bg: #333 · color: white · padding: 10px
  td            border: 1px #ccc · padding: 10px · centered
  .present      bg: #4CAF50 · color: white · border-radius: 5px ✅
  .absent       bg: #f44336 · color: white · border-radius: 5px ❌
  .editable     bg: #eef · border: 1px #ccc · width: 100%
```

---

## 🗂️ Project Structure

```
Attendance-Taker/
│
├── 📄 attendance taker system.html    # The complete app — 171 lines · 5.32 KB
│   │
│   ├── <head>
│   │   ├── charset UTF-8 + viewport meta
│   │   ├── <title>Attendance Taker System</title>
│   │   └── <style>  ← 67 lines of inline CSS
│   │       ├── body, .container, h1
│   │       ├── table, th, td
│   │       ├── .present (green #4CAF50), .absent (red #f44336)
│   │       ├── .add-student, .editable
│   │       └── .actions
│   │
│   ├── <body>
│   │   ├── <h1>Attendance Taker System</h1>
│   │   ├── .add-student div
│   │   │   ├── <input id="studentName">
│   │   │   └── <button onclick="addStudent()">Add Student</button>
│   │   └── #attendanceTable
│   │       ├── <thead> — 6 column headers
│   │       └── <tbody> — dynamically populated by addStudent()
│   │
│   └── <script>  ← 50 lines of vanilla JS
│       ├── let studentId = 0           (global counter)
│       ├── addStudent()                (add row + clear input)
│       ├── markAttendance(id, bool)    (increment + recalculate)
│       └── updatePercentage(id)        (manual total → recalculate)
│
└── 📖 README.md                        # This file
```

---

## 🚀 Quick Start

### Open Directly (Zero Setup)

```bash
# Clone the repo
git clone https://github.com/sreyoshmajumder/Attendance-Taker.git
cd Attendance-Taker

# Just double-click or open in browser:
open "attendance taker system.html"         # macOS
start "attendance taker system.html"        # Windows
xdg-open "attendance taker system.html"     # Linux
```

> ✅ That's it. No npm install. No pip. No server. No account. Just open and use.

### Host on GitHub Pages (Free)

```bash
# Already pushed to GitHub ✅
# Go to: Settings → Pages → Source: main branch → / (root)
# Live at: https://sreyoshmajumder.github.io/Attendance-Taker/attendance%20taker%20system.html
```

### Host with Live Server (VS Code)

```
1. Install "Live Server" extension in VS Code
2. Right-click "attendance taker system.html"
3. Click "Open with Live Server"
4. Auto-opens at http://localhost:5500
```

---

## 💡 Usage Guide

### Step 1 — Add All Students

```
Type "Alice"   → Click "Add Student"  → Row appears ✅
Type "Bob"     → Click "Add Student"  → Row appears ✅
Type "Charlie" → Click "Add Student"  → Row appears ✅
```

### Step 2 — Mark Daily Attendance

```
Day 1:
  Alice   → Click ✅ Mark Present  (Present: 1, Absent: 0, Total: 1, %: 100.00%)
  Bob     → Click ✅ Mark Present  (Present: 1, Absent: 0, Total: 1, %: 100.00%)
  Charlie → Click ❌ Mark Absent   (Present: 0, Absent: 1, Total: 1, %: 0.00%)

Day 2:
  Alice   → Click ✅ Mark Present  (Present: 2, Absent: 0, Total: 2, %: 100.00%)
  Bob     → Click ❌ Mark Absent   (Present: 1, Absent: 1, Total: 2, %: 50.00%)
  Charlie → Click ✅ Mark Present  (Present: 1, Absent: 1, Total: 2, %: 50.00%)
```

### Step 3 — Manual Total Override

```
If you have 30 working days in the month but only marked 10 so far:
  → Edit the "Total Working Days" cell directly (type 30)
  → Percentage instantly recalculates based on new total
```

### Step 4 — Read Results

```
┌──────────┬───────────┬─────────┬────────┬──────────┐
│ Student  │ Total Days│ Present │ Absent │    %     │
├──────────┼───────────┼─────────┼────────┼──────────┤
│ Alice    │    22     │   18    │   4    │  81.82%  │  ✅ SAFE
│ Bob      │    22     │   16    │   6    │  72.73%  │  ⚠️  WARNING
│ Charlie  │    22     │   12    │  10    │  54.55%  │  ❌ CRITICAL
└──────────┴───────────┴─────────┴────────┴──────────┘
```

---

## 🔭 Future Roadmap

```
v1.0 ── CURRENT ────────────────────────────────────────────────────────
  ✅  Add unlimited students by name
  ✅  Mark present / absent with one click per student
  ✅  Auto-calculate days present, days absent, total, percentage
  ✅  Editable total working days with live recalculation
  ✅  Empty name validation alert
  ✅  Single HTML file — zero dependencies

v2.0 ── UX ENHANCEMENTS ────────────────────────────────────────────────
  🔲  Colour-coded percentage rows (green ≥75% / yellow 60–74% / red <60%)
  🔲  Delete student row button
  🔲  Reset attendance for individual or all students
  🔲  Sort table by name / attendance % / days absent
  🔲  Print / Export to PDF button

v3.0 ── PERSISTENCE ────────────────────────────────────────────────────
  🔲  Save attendance to localStorage (survives page refresh)
  🔲  Load saved session on next open
  🔲  Export to CSV / Excel for submission to admins
  🔲  Date-wise attendance log (track which specific days)

v4.0 ── ADVANCED FEATURES ──────────────────────────────────────────────
  🔲  Multiple class / section support
  🔲  Attendance threshold alert (flag students below 75%)
  🔲  Monthly / weekly attendance report summary
  🔲  Bulk import students from CSV / text list
  🔲  QR code attendance via mobile scan
```

---

## 🛠️ Tech Stack

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-0a0a0f?style=for-the-badge&logo=html5&logoColor=ff6347)
![CSS3](https://img.shields.io/badge/CSS3%20Inline-0a0a0f?style=for-the-badge&logo=css3&logoColor=00ff88)
![JavaScript](https://img.shields.io/badge/Vanilla%20JavaScript-0a0a0f?style=for-the-badge&logo=javascript&logoColor=ffd700)
![DOM API](https://img.shields.io/badge/DOM%20API-0a0a0f?style=for-the-badge&logo=html5&logoColor=4ade80)
![No Framework](https://img.shields.io/badge/No%20Framework-0a0a0f?style=for-the-badge&logoColor=ff2d78)
![No Backend](https://img.shields.io/badge/No%20Backend-0a0a0f?style=for-the-badge&logoColor=39ff14)

</div>

---

## 👨‍💻 Author

<div align="center">

**Built with 📋 + ❤️ by [Sreyosh Majumder](https://github.com/sreyoshmajumder)**

[![GitHub](https://img.shields.io/badge/GitHub-sreyoshmajumder-0a0a0f?style=for-the-badge&logo=github&logoColor=00ff88)](https://github.com/sreyoshmajumder)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a0a0f?style=for-the-badge&logo=linkedin&logoColor=0077b5)](https://linkedin.com/in/YOUR_LINKEDIN)

> *"The simplest tools are often the most powerful — a single HTML file that every teacher can use."*

</div>

---

## ⭐ Show Some Love

```
★  Star this repository
🍴  Fork it and add localStorage persistence
🐛  Open issues for bugs or feature requests
📢  Share with teachers, schools, and admins who need it
```

---

<div align="center">

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:004d2e,50:003320,100:001a0a&height=120&section=footer&text=Every%20Student%20Counted.%20Every%20Day%20Tracked.&fontSize=16&fontColor=00ff88&fontAlignY=65)

</div>
