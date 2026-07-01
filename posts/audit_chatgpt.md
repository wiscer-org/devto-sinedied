---
title: ChatGPT Manual Screen Reader Audit
tags: 'accessibility, a11y, nvda, pagelive'
published: true
description: ChatGPT manual screen ready audit using NVDA on Windows 11.
id: 4016730
---

## About

**Target URL:** https://chatgpt.com

This document records the findings of an ongoing manual screen reader audit
conducted on [ChatGPT](https://chatgpt.com). Issues are identified through
direct interaction using screen reader assistive technology.

<!-- and evaluated against WCAG 2.1 AA criteria. -->

---

## Test Environment

All testing sessions are conducted manually using the following environment.
Versions reflect the latest available at the time of each audit session date.

| Component            | Details                                         |
| -------------------- | ----------------------------------------------- |
| **Screen Reader**    | NVDA (latest version as of audit date)          |
| **Browser**          | Google Chrome (latest version as of audit date) |
| **Operating System** | Windows 11 (latest version as of audit date)    |

---

## Issue Classification

| Classification         | Meaning                                                                                                                                                          |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Blocker / Critical** | Task is completely impossible for screen reader users. Immediate attention required.                                                                             |
| **Barrier / High**     | Task is severely impaired. Significant effort or workaround required to proceed. Users may not perceive that something has happened or that a task is available. |
| **Barrier / Medium**   | Task is degraded but completable. Causes meaningful confusion or extra steps. Users may be uncertain about the current state or outcome of an interaction.       |
| **Friction / Low**     | Task is completable with minor inconvenience. Cosmetic or edge case impact.                                                                                      |

---

## Audit Findings

### 2026-06-29

#### Unaccessible Command Palette Options

- **Classification:** Blocker / Critical

<!-- - **WCAG Criterion:** x.x.x — Criterion Name (Level A/AA) -->

- **Description:** After typing / in the prompt input, a command palette appears
  containing a list of available commands. Users can navigate the command list
  using the Up and Down Arrow keys.
- **Issue:** When moving focus between command -options, the screen reader does
  not announce the currently focused option.
- **Recommendation:** Describe the fix or remediation approach.

#### Missing 'Current Key Sequence' Text in the Keyboard Shortcut Dialog

- **Classification:** Blocker / Critical
- **Description:** The Keyboard Shortcut dialog, opened with `Ctrl` + `/`, shows
  a table of shortcuts in three columns. The third column is intended to display
  the currently assigned key sequence for each action.
- **Issue:** When navigating to the current key sequence column, only a 'Change
  key sequence' button is exposed. There is no information about the actual key
  combination assigned to the shortcut.
- **Suggestion:** Display the active shortcut text in each row, for example
  'Open New Chat — `Ctrl + Shift + O`', so users can hear or read the current
  key sequence.

#### Missing Reading of Received New Response

- **Classification:** Barrier / High
- **Description:** After submitting a prompt, ChatGPT may take some time to
  finish generating the response. The app announces when the response is
  complete, which is helpful, but users still cannot immediately review the full
  response.
- **Issue:** Screen reader users must switch into browse or virtual cursor mode
  and use a key sequence to read the completed response, then manually return to
  the chat input before continuing.
- **Recommendation:** Expose the full response to assistive technology via a
  screen-reader-only element with `aria-live`, or ensure the response area is
  automatically announced when generation ends.

#### Missing Announcement of the Focused Chat Title in the Search Chats Dialog

- **Classification:** Friction / Low
- **Description:** The Search Chats dialog opens with `Ctrl` + `/`, and focus is
  placed in the search input at the top. Below it, a list of chats is displayed,
  showing either all chats or the results of the current search. While focus
  remains in the search field, users can move through the list with the Up and
  Down Arrow keys to select a chat without moving focus away.
- **Issue:** As the highlighted chat changes, the screen reader announces the
  contents of the search input rather than the currently highlighted chat title.
  This makes it harder for users to confirm which chat is selected before
  opening it.
- **Recommendation:** Announce the highlighted chat title when the selection
  changes, for example by temporarily exposing it in an element with an
  `aria-live` region.

#### Missing Notification When a Dialog Closes

- **Classification:** Friction / Low
- **Description:** Dialogs such as the Search Chats and Keyboard Shortcuts
  dialogs can be closed by pressing the `Escape` key.
- **Issue:** Some users may not be aware that the dialog has closed, which can
  make the interaction feel abrupt or confusing.
- **Suggestion:** Announce the dialog closing in a live region, for example with
  a screen-reader-only element using `aria-live`.

#### Missing Hint to Close Menu in Pop Up Menus

- **Classification:** Friction / Low
- **Description:** There few pop up menus that open from related button, like
  'Profile Menu', 'Organize Chats Menu', and 'Model Selector Menu'. The menus
  appears as a modal-like dialog with focus trap behavior, which is a good
  pattern for this interaction.
- **Issue:** Users may not realize how to close the menu because there is no
  spoken or visible hint that Escape will dismiss it.
- **Suggestion:** Add hidden screen-reader text or visible instructions in the
  menu that clearly states 'Press Escape to close'.

---

## Resolution via PageLive

Some of the issues identified in this audit are not straightforward to resolve
at the source — either because they require changes to the target application
itself, or because a native fix is unlikely to be prioritised. For those cases,
potential workaround approaches are explored in
[PageLive for ChatGPT](https://wiscer.org/pagelive/chatgpt/) articles, and
implementations are shipped as part of the
**[PageLive Chrome extension](https://wiscer.org/pagelive)**, which bridges
missing accessibility features for screen reader users in selected web
applications.

<!--
| Issue                   | Related Article                              | PageLive Status                     |
| ----------------------- | -------------------------------------------- | ----------------------------------- |
| Issue description or ID | [Article title](https://example.com/article) | Implemented / In Progress / Planned |

**Audit Status:** Ongoing

**Auditor:** Your Name

**Last Updated:** 2026-06-29

-->
