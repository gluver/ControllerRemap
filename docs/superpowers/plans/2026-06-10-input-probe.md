# Controller Input Probe Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a local diagnostic page that shows raw Xbox/gamepad input and keyboard events from a Bluetooth controller.

**Architecture:** A single static HTML file contains the UI, Gamepad API polling, keyboard event logging, and export/clear controls. A short README explains how to test the controller in Xbox mode first, then keyboard mode.

**Tech Stack:** HTML, CSS, browser JavaScript, Gamepad API, KeyboardEvent.

---

### Task 1: Static Input Probe

**Files:**
- Create: `index.html`
- Create: `README.md`

- [ ] **Step 1: Create the diagnostic page**

Create `index.html` with:
- A gamepad status section that lists connected pads, buttons, axes, and recent changed controls.
- A keyboard event section that logs `keydown` and `keyup` with `key`, `code`, modifiers, repeat state, and timestamp.
- Clear and copy buttons for the keyboard log.
- No external dependencies, so it works from `file://`.

- [ ] **Step 2: Create usage instructions**

Create `README.md` with:
- Xbox mode test steps.
- Keyboard mode test steps.
- Notes on likely remapping choices after raw input is known.

- [ ] **Step 3: Verify static files are present**

Run: `Get-ChildItem -Force`

Expected: `index.html` and `README.md` are listed.

- [ ] **Step 4: Open in browser and verify visible state**

Open `index.html` in the in-app browser.

Expected: The page shows sections for Xbox/Gamepad mode and Keyboard mode, with no script errors visible in the UI.
