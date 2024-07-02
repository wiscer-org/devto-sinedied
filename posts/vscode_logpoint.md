---
title: How to Use VSCode Logpoint with Keyboard Shortcuts
published: true
description: How to use VSCode logpoint feature with only using keyboard.
tags: 'vscode, logpoint, javascript'
canonical_url: null
id: 1908312
date: '2024-07-02T01:47:50Z'
---

# How to Use VSCode Logpoint with Keyboard Shortcuts

## Introduction
This article demonstrates how to efficiently utilize VSCode Logpoints using only keyboard shortcuts. This method is particularly beneficial for users who rely on screen readers or prefer keyboard-centric workflows.

## Understanding VSCode Logpoint
VSCode Logpoints allow developers to dynamically insert logging messages into their code without modifying the source code itself. This feature is invaluable for debugging and understanding code execution flow.

## Setting Up Custom Shortcut for Logpoints
Since there is no default shortcut or menu item for adding Logpoints, follow these steps to define a custom shortcut:
- Open the keybinding editor with `Ctrl + K Ctrl + S`.
- Type `Logpoint` into the search box and press `Tab` to navigate to the `Debug:Add Logpoint` result. Press `Enter` to activate.
- Enter your desired keyboard shortcut, for example, `Ctrl + L Ctrl + P`, and confirm by pressing `Enter`.

## Example File
To illustrate the usage of Logpoints, consider the following JavaScript file:

```javascript
let a = 1;
let b = plus_4(a);
plus_9(b);
console.log("End of file");

function plus_4(x) {
    console.log("plus 4");
    return x + 4;                               
}

function plus_9(x) {
    console.log("Plus 9");
    return x + 9;
}
```

## Adding Logpoints to Replace `console.log`
Replacing repetitive `console.log` statements with Logpoints enhances debugging efficiency:
- Navigate to the line containing `console.log`.
- Use the custom shortcut (`Ctrl + L Ctrl + P`) to add a Logpoint. Enter a descriptive message when prompted, e.g., "Reached end of file", and press `Enter`.

Repeat these steps for each `console.log` statement in your code.

## Running in Debug Environment
To execute the JavaScript file with Logpoints:
- Open the debug panel with `Ctrl + Shift + D`.
- Navigate to `Javascript Debug Terminal` using `Tab` and activate it.
- Run the script using:
  ```bash
  node index.js
  ```
  Logpoint messages will be displayed in the terminal.

**Note for screen reader users:** Switch to screen reader compatibility mode with `F2` to read the terminal output. Use arrow keys to navigate through lines and press `F1` to return to normal mode.

Using Logpoints eliminates the need for repetitive `console.log` cleanup during debugging sessions, streamlining your workflow.

## Removing Logpoints
To remove a Logpoint, position the cursor on the relevant line and press `F9`, similar to removing breakpoints.

## Conclusion
Using VSCode Logpoints significantly improves debugging efficiency compared to traditional `console.log` methods. It saves time by reducing code clutter and repetitive cleanup tasks, making debugging more focused and productive.

We hope this article helps streamline your development process with VSCode Logpoints. Happy coding!

Thanks for reading.

