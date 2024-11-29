---
title: Auto Hot Key to automate Keystrokes in Windsurf IDE
published: true
description: How to automate shortcuts / keystrokes. Example is on Windsurf IDE.
tags: 'vscode, windsurf, shortcuts, breadcrumbs'
canonical_url: null
id: 2126873
date: '2024-11-29T12:40:25Z'
---

# Using Keyboard Shortcuts to Enhance Productivity in Windsurf IDE  

As a non-visual developer (screen reader user), I rely heavily on keyboard shortcuts and keybindings. This article provides a workaround for inputting keystrokes in the Windsurf IDE.

## Breadcrumbs in VSCode IDE  

I primarily use VSCode IDE because it is highly accessible for screen reader users. One of the shortcuts I use most frequently is **`Breadcrumbs Focus`**.  

**Shortcut**: `Ctrl` + `Shift` + `.`  
Action: *Focus and Select Breadcrumbs* (`breadcrumbs.focusAndSelect`)  

![VSCode Breadcrumbs](https://github.com/wiscer-org/devto-sinedied/blob/main/assets/images/vscode-breadcrumbs.png)

Breadcrumbs are located at the upper part of the text editor. I use this shortcut every 5–10 minutes because:  
- It provides a quick snapshot of the code hierarchy, whether within a class or an HTML tree.  
- It helps navigate between methods within the file efficiently.  

## Windsurf IDE  

Windsurf IDE is an accessible, AI-powered IDE built on top of VSCode, inheriting many of its shortcuts. However, the shortcut for **`breadcrumbs.focusAndSelect`** does not work in Windsurf.  

## The `breadcrumbs.focus` Shortcut  

In Windsurf, I discovered an alternative shortcut:  

**Shortcut**: `Ctrl` + `Shift` + `;`  
Action: *Focus on Breadcrumbs* (`breadcrumbs.focus`)  

However, in Windsurf, this shortcut does not automatically focus on the original breadcrumbs. Instead, it defaults to a new visual element on the right side of the breadcrumbs containing "Explain," "Refactor," and "Add Docstring" links.  

To replicate the functionality of `breadcrumbs.focusAndSelect`, I have to:  
1. Press `Ctrl + Shift + ;` to focus on the new links.  
2. Use the left arrow to move focus to the original breadcrumbs.  
3. Press the down arrow to select and display the code tree.  

<!-- ![Windsurf Breadcrumbs](https://github.com/wiscer-org/devto-sinedied/blob/main/assets/images/windsurf-breadcrumbs.png) -->

Since I frequently use this functionality, automating these steps into a single keystroke would save a lot of hassle.  

## AutoHotkey: A Solution  

To streamline the process, I use **AutoHotkey**, a free tool for customizing keyboard shortcuts.  

I mapped the sequence to `NumpadIns` followed by the right arrow, as they are conveniently close on my keyboard.  

### AutoHotkey Script  

```ahk
; Map NumpadIns + Right Arrow to simulate breadcrumbs.focusAndSelect in Windsurf
NumpadIns & Right::
Send ^+;  ; Send Ctrl+Shift+;
Sleep 100  ; Pause for 100 milliseconds
Send {Left}  
Sleep 100  
Send {Down}  
return
```

## Complete Setup
Follow these steps to set up the shortcut:

1. Download AutoHotkey: [Download AHK](https://www.autohotkey.com/).
2. Create a Script File:
    - Open a text editor, such as Notepad.
    - Paste the script above.
    - Save the file with a `.ahk` extension (e.g., `breadcrumbs.ahk`). Ensure there is no hidden `.txt` suffix.
3. Run the Script: Double-click the .ahk file to activate the script.

For a detailed guide, refer to the AutoHotkey Tutorial.

This solution significantly simplifies navigating breadcrumbs in Windsurf IDE and enhances accessibility for screen reader users.