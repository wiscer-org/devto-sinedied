---
title: ChatGPT Manual Screen Reader Audit
tags: 'accessibility, a11y, nvda, pagelive'
published: false
description: ChatGPT manual screen ready audit using NVDA on Windows 11.
id: 4016730
---

## About

**Target URL:** https://chatgpt.com

This document records the findings of an ongoing manual screen reader audit
conducted on [ChatGPT](https://chatgpt.com). Issues are identified through
direct interaction using screen reader assistive technology.

<!-- and evaluated against WCAG 2.1 AA criteria. -->

## Test Environment

All testing sessions are conducted manually using the following environment.
Versions reflect the latest available at the time of each audit session date.

| Component            | Details                                         |
| -------------------- | ----------------------------------------------- |
| **Screen Reader**    | NVDA (latest version as of audit date)          |
| **Browser**          | Google Chrome (latest version as of audit date) |
| **Operating System** | Windows 11 (latest version as of audit date)    |

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
  using the Up and Down Arrow keys. Issue: When moving focus between command
  options, the screen reader does not announce the currently focused option.
- **Recommendation:** Describe the fix or remediation approach.

<!--
---

#### Issue 2

- **Classification:** Barrier / High
- **WCAG Criterion:** x.x.x — Criterion Name (Level A/AA)
- **Description:** Describe what the issue is and how it was encountered during
  screen reader testing.
- **Recommendation:** Describe the fix or remediation approach.

---

### 2026-MM-DD

#### Issue 1

- **Classification:** Friction / Low
- **WCAG Criterion:** x.x.x — Criterion Name (Level A/AA)
- **Description:** Describe what the issue is and how it was encountered during
  screen reader testing.
- **Recommendation:** Describe the fix or remediation approach.

---

 -->

## Resolution via PageLive

Some of the issues identified in this audit are not straightforward to resolve
at the source — either because they require changes to the target application
itself, or because a native fix is unlikely to be prioritised. For those cases,
potential workaround approaches are explored in separate articles, and
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
