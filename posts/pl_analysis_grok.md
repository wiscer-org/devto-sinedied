---
title: Screen Reader Experience Analysis on Grok
published: true
description: Screen reader experience manual analysis on Grok
tags: 'PageLive, a11y, grok, screenreader, accessibility'
canonical_url: null
id: 3322522
date: '2026-03-07T12:36:49Z'
---

*7 March 2026* — **PageLive Project**

---

## Summary

This report documents the difficulties a screen reader user encounters when using Grok. Testing was conducted using NVDA on Chrome on a Windows desktop. While the findings are based on NVDA, the barriers described are expected to affect users of other screen readers, including JAWS, in similar ways. While Grok is usable with a screen reader, several interactions require significant extra effort or guesswork that sighted users do not face.

## 1. Scope and Testing Environment

This analysis evaluates the screen reader experience on Grok as encountered during manual testing. The scope is limited to interactions that are part of routine use: composing and reading conversations, navigating between chats, and accessing application controls.

Findings are not evaluated against WCAG criteria. The focus is on the practical experience of a screen reader user during everyday tasks.

| | |
|---|---|
| **Screen Reader** | NVDA 2025.3.3.54605 |
| **Browser** | Chrome 145.0.7632.117 |
| **Platform** | Windows Desktop |
| **Interface Tested** | grok.com web application |

Findings are classified by their impact on task completion:

- **Blocker** — The task cannot be completed.
- **Barrier** — The task can be completed, but requires significant additional effort, guesswork, or repeated keystrokes that are not required of sighted users.
- **Friction** — The task works as expected, but the experience is degraded in a way that compounds over extended use.

## 2. Findings

### 2.1 Response Completion Is Not Announced
**Severity: Barrier**

When Grok finishes generating a response, no announcement is made to the screen reader. The response content is not placed in a live region, so the screen reader does not notify the user that new content is available or that generation has completed.

As a result, the user has no reliable way to know when it is appropriate to begin reading. The user must manually navigate to the chat area, attempt to locate the new response, and determine through repeated keystrokes whether generation has finished or is still in progress. This interaction occurs on every single exchange, making it the most consequential barrier in routine use.

### 2.2 The "Show All" Button in the All Chats Dialog Is Not Accessible
**Severity: Blocker**

The All Chats dialog in Grok contains a "Show All" button that reveals additional application actions beyond the default view. By default, only the "Create New Chat" action is visible. Activating "Show All" exposes further actions including Switch Theme, Change Language, and others.

The "Show All" button is neither perceivable nor operable by a screen reader. The button is not exposed in the accessibility tree, meaning the screen reader does not announce its presence and the user has no means of activating it through keyboard navigation.

As a result, the actions revealed by this button — Switch Theme, Change Language, and any others — are permanently inaccessible to screen reader users. The task of discovering and using these actions cannot be completed.

### 2.3 Missing Keyboard Shortcuts for Frequently Used Actions
**Severity: Friction**

The following actions do not have keyboard shortcuts in Grok:

- Delete the current chat
- Toggle the sidebar
- Open the chat list to allow chat switching
- Start a new chat
- Announce the last response
- Jump to the chat input field

Each of these actions is available through the interface but requires the user to locate the relevant control through navigation. For a sighted user, these controls are immediately visible. For a screen reader user, the location of a button is not always remembered between sessions, and finding it requires traversal through surrounding content.

The absence of shortcuts does not prevent these actions. However, the cumulative effect of repeated traversal meaningfully degrades the experience of extended use, particularly given the number of actions affected.

## 3. Summary of Findings

| # | Finding | Severity |
|---|---|---|
| 2.1 | Response completion not announced | Barrier |
| 2.2 | "Show All" button in All Chats dialog not accessible | Blocker |
| 2.3 | Missing keyboard shortcuts for common actions | Friction |

## 4. Further Reading

This article is part of the PageLive project's documentation for Grok. A companion article, [Screen Reader Experience Mitigation on Grok](https://dev.to/wiscer/screen-reader-experience-mitigation-on-grok-35j4), describes how PageLive addresses the barriers identified above. For a full list of keyboard shortcuts and features PageLive provides for Grok, see the [PageLive for Grok documentation](https://wiscer.org/pagelive/grok).

---

*— End of Article —*

## Disclaimers

*This analysis was conducted as part of the PageLive project, which develops keyboard shortcut and screen reader support for AI chat interfaces. The author develops PageLive, a Chrome extension that addresses several of the barriers described in this report. A companion Screen Reader Experience Mitigation documents the approaches PageLive applies to each finding.*

*PageLive can be installed for free on the [PageLive chrome webstore page](https://chromewebstore.google.com/detail/pagelive/kachdjbdcmofjmaoklcfofbcnlakfnbb).*

*The findings, severity classifications, and testing observations in this report are the author's own, based on manual testing with NVDA on Chrome. AI assistance was used solely to shape the writing style of this document.*
