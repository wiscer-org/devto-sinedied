---
title: VSCode shortcuts / keybinding for Non Visual Users
tags: 'vscode, keybindings, withscreenreader'
published: true
description: List of benefial and most used VSCode standard keybindings for non visual users.
---
In this article, I’ll be sharing a selection of VSCode shortcuts and keybindings that I frequently use and find
particularly useful as a screen reader (non-visual) developer. 

While memorizing every keybinding available in VSCode can
be overwhelming, focusing on a core set of shortcuts can greatly enhance efficiency and ease of use.
To make this guide practical, I’ve highlighted keybindings that are most likely to be beneficial for screen reader
users. The list below will have marks on shortcuts which I think essential. 

The default
keybindings are sourced from the official VSCode documentation as of September 3, 2024. I hope this resource will help
you streamline your workflow by focusing on the most useful and frequently used shortcuts.

> NOTE: The essential shortcuts will started by a star symbol

<h2>General</h2>
<dl>
    <dt class="s">Ctrl+Shift+P,</dt>
    <dd>F1 Show Command Palette</dd>
    <dt class="s">Ctrl+P</dt>
    <dd>Quick Open, Go to File…</dd>
    <dt>Ctrl+Shift+N</dt>
    <dd>New window/instance</dd>
    <dt class="s">Ctrl+Shift+W</dt>
    <dd>Close window/instance</dd>
    <dt class="s">Ctrl+,</dt>
    <dd>User Settings</dd>
    <dt class="s">Ctrl+K Ctrl+S
    <dd>Keyboard Shortcuts</dd>
</dl>

<h2>Basic editing</h2>
<dl>
    <dt class="s">Ctrl+X</dt>
    <dd>Cut line (empty selection)</dd>
    <dt class="s">Ctrl+C</dt>
    <dd>Copy line (empty selection)</dd>
    <dt class="s">Alt+ ↑/↓<dt>
    <dd>Move line up/down</dd>
    <dt class="s">Shift+Alt+ ↑/↓<dt>
    <dd>Copy line up/down</dd>
    <dt class="s">Ctrl+Shift+K</dt>
    <dd>Delete line</dd>
    <dt class="s">Ctrl+Enter</dt>
    <dd>Insert line below</dd>
    <dt class="s">Ctrl+Shift+Enter</dt>
    <dd>Insert line above</dd>
    <dt class="s">Ctrl+Shift+\</dt>
    <dd>Jump to matching bracket</dd>
    <dt>Ctrl+ ]/[</dt>
    <dd>Indent/outdent line. This is useful when I want to make sure there is no whitespaces at start.</dd>
    <dt class="s">Home/End</dt>
    <dd>Go to beginning / end of line</dd>
    <dt class="s">Ctrl+Home</dt>
    <dd>Go to beginning of file</dd>
    <dt class="s">Ctrl+End</dt>
    <dd>Go to end of file</dd>
    <dt>Ctrl+ ↑/↓ </dt>
    <dd>Scroll line up/down</dd>
    <dt>Alt+ PgUp/PgDn</dt>
    <dd>Scroll page up/down</dd>
    <dt>Ctrl+Shift+[</dt>
    <dd>Fold (collapse) region</dd>
    <dt>Ctrl+Shift+]</dt>
    <dd>Unfold (uncollapse) region</dd>
    <dt>Ctrl+K</dt>
    <dd>Ctrl+[ Fold (collapse) all subregions</dd>
    <dt>Ctrl+K</dt>
    <dd>Ctrl+] Unfold (uncollapse) all subregions</dd>
    <dt>Ctrl+K Ctrl+0</dt>
<dd class="s">Fold (collapse) all regions</dd>
    <dt>Ctrl+K Ctrl+J</dt>
<dd class="s">Unfold (uncollapse) all regions</dd>
    <dt>Ctrl+K Ctrl+C</dt>
<dd>Add line comment</dd>
    <dt>Ctrl+K Ctrl+U</dt>
<dd>Remove line comment</dd>
    <dt class="s">Ctrl+/</dt>
    <dd>Toggle line comment</dd>
    <dt class="s">Shift+Alt+A</dt>
    <dd>Toggle block comment</dd>
    <dt class="s">Alt+Z</dt>
    <dd>Toggle word wrap</dd>
</dl>

<h2>Navigation</h2>
<dl>
    <dt>Ctrl+T</dt>
    <dd>Show all Symbols</dd>
    <dt class="s">Ctrl+G</dt>
    <dd>Go to Line...</dd>
    <dt class="s">Ctrl+P</dt>
    <dd>Go to File...</dd>
    <dt class="s">Ctrl+Shift+O</dt>
    <dd>Go to Symbol...</dd>
    <dt class="s">Ctrl+Shift+M</dt>
    <dd>Show Problems panel</dd>
    <dt class="s">F8</dt>
    <dd>Go to next error or warning</dd>
    <dt class="s">Shift+F8</dt>
    <dd>Go to previous error or warning</dd>
    <dt class="s">Ctrl+Shift+Tab</dt>
    <dd>Navigate editor group history</dd>
    <dt class="s">Alt+ ←/→<dt>
    <dd>Go back / forward</dd>
    <dt class="s">Ctrl+M</dt>
    <dd>Toggle Tab moves focus</dd>
</dl>

<h2>Search and replace</h2>
<dl>
    <dt class="s">Ctrl+F</dt>
    <dd>Find</dd>
    <dt class="s">Ctrl+H</dt>
    <dd>Replace</dd>
    <dt>F3 / Shift+F3<dt>
    <dd>Find next/previous</dd>
    <dt>Alt+Enter</dt>
    <dd>Select all occurences of Find match</dd>
    <dt>Ctrl+D</dt>
    <dd>Add selection to next Find match</dd>
    <dt>Ctrl+K Ctrl+D</dt>
    <dd>Move last selection to next Find match</dd>
    <dt>Alt+ C/R/W<dt>
    <dd>Toggle case-sensitive / regex / whole word</dd>
</dl>

<h2>Multi-cursor and selection</h2>
<dl>
    <dt>Alt+Click</dt>
    <dd>Insert cursor</dd>
    <dt>Ctrl+Alt+ ↑/↓</dt>
    <dd>Insert cursor above / below</dd>
    <dt>Ctrl+U</dt>
    <dd>Undo last cursor operation</dd>
    <dt class="s">Shift+Alt+I</dt>
    <dd>Insert cursor at end of each line selected</dd>
    <dt class="s">Ctrl+L</dt>
    <dd>Select current line</dd>
    <dt>Ctrl+Shift+L</dt>
    <dd>Select all occurrences of current selection</dd>
    <dt class="s">Ctrl+F2</dt>
    <dd>Select all occurrences of current word</dd>
    <dt>Shift+Alt+→</dt>
    <dd>Expand selection</dd>
    <dt>Shift+Alt+←</dt>
    <dd>Shrink selection</dd>
    <dt>Shift+Alt + (drag mouse)</dt>
    <dd>Column (box) selection</dd>
    <dt>Ctrl+Shift+Alt+ (arrow key)</dt>
    <dd>Column (box) selection</dd>
    <dt>Ctrl+Shift+Alt+ PgUp/PgDn</dt>
    <dd>Column (box) selection page up/down</dd>
</dl>

<h2>Rich languages editing</h2>
<dl>
    <dt class="s">Ctrl+Space, Ctrl+I</dt>
    <dd>Trigger suggestion</dd>
    <dt class="s">Ctrl+Shift+Space</dt>
    <dd>Trigger parameter hints</dd>
    <dt class="s">Shift+Alt+F</dt>
    <dd>Format document</dd>
    <dt class="s">Ctrl+K Ctrl+F</dt>
    <dd>Format selection</dd>
    <dt class="s">F12</dt>
    <dd>Go to Definition</dd>
    <dt class="s">Alt+F12</dt>
    <dd>Peek Definition</dd>
    <dt class="s">Ctrl+K F12</dt>
    <dd>Open Definition to the side</dd>
    <dt class="s">Ctrl+.</dt>
    <dd>Quick Fix</dd>
    <dt class="s">Shift+F12</dt>
    <dd>Show References</dd>
    <dt class="s">F2</dt>
    <dd>Rename Symbol</dd>
    <dt class="s">Ctrl+K Ctrl+X</dt>
<dd>Trim trailing whitespace</dd>
    <dt>Ctrl+K M</dt>
    <dd>Change file language</dd>
<dl>

<h2>Editor management</h2>
<dl>
    <dt class="s">Ctrl+F4, Ctrl+W</dt>
    <dd>Close editor</dd>
    <dt>Ctrl+K F</dt>
    <dd>Close folder</dd>
    <dt>Ctrl+\</dt>
    <dd>Split editor</dd>
    <dt class="s">Ctrl+ 1/2/3<dt>
    <dd>Focus into 1st, 2nd or 3rd editor group. This is most useful for me when I repeatedly jump between specific locations in file/files.</dd>
    <dt>Ctrl+K Ctrl+ ←/→<dt>
    <dd>Focus into previous/next editor group</dd>
    <dt>Ctrl+Shift+ PgUp/PgDn<dt>
    <dd>Move editor left/right</dd>
    <dt>Ctrl+K ←/→<dt>
    <dd>Move active editor group</dd>
<dl>

<h2>File management</h2>
<dl>
    <dt>Ctrl+N</dt>
    <dd>New File</dd>
    <dt>Ctrl+O</dt>
    <dd>Open File...</dd>
    <dt class="s">Ctrl+S</dt>
    <dd>Save</dd>
    <dt>Ctrl+Shift+S</dt>
    <dd>Save As...</dd>
    <dt>Ctrl+K S</dt>
    <dd>Save All</dd>
    <dt class="s">Ctrl+F4</dt>
    <dd>Close</dd>
    <dt>Ctrl+K Ctrl+W</dt>
    <dd>Close All</dd>
    <dt class="s">Ctrl+Shift+T</dt>
    <dd>Reopen closed editor</dd>
    <dt class="s">Ctrl+K</dt>
    <dd>Enter Keep preview mode editor open</dd>
    <dt class="s">Ctrl+Tab</dt>
    <dd>Open next</dd>
    <dt class="s">Ctrl+Shift+Tab</dt>
    <dd>Open previous</dd>
    <dt class="s">Ctrl+K P</dt>
    <dd>Copy path of active file</dd>
    <dt class="s">Ctrl+K R</dt> 
    <dd>Reveal active file in Explorer</dd>
    <dt>Ctrl+K O</dt>
    <dd>Show active file in new window/instance</dd>
</dl>

<h2>Display</h2>
<dl>
    <dt>F11</dt>
    <dd>Toggle full screen</dd>
    <dt>Shift+Alt+0</dt>
    <dd>Toggle editor layout (horizontal/vertical)</dd>
    <dt>Ctrl+ =/-<dt>
    <dd>Zoom in/out</dd>
    <dt>Ctrl+B</dt>
    <dd>Toggle Sidebar visibility</dd>
    <dt class="s">Ctrl+Shift+E</dt>
    <dd>Show Explorer / Toggle focus</dd>
    <dt class="s">Ctrl+Shift+F</dt>
    <dd>Show Search</dd>
    <dt class="s">Ctrl+Shift+G</dt>
    <dd>Show Source Control</dd>
    <dt class="s">Ctrl+Shift+D</dt>
    <dd>Show Debug</dd>
    <dt class="s">Ctrl+Shift+X</dt>
    <dd>Show Extensions</dd>
    <dt class="s">Ctrl+Shift+H</dt>
    <dd>Replace in files</dd>
    <dt>Ctrl+Shift+J</dt>
    <dd>Toggle Search details</dd>
    <dt>Ctrl+Shift+U</dt>
    <dd>Show Output panel</dd>
    <dt class="s">Ctrl+Shift+V</dt>
    <dd>Open Markdown preview</dd>
    <dt>Ctrl+K V<dt>
    <dd>Open Markdown preview to the side</dd>
    <dt>Ctrl+K Z<dt>
    <dd>Zen Mode (Esc Esc to exit)</dd>
</dl>

<h2>Debug</h2>
<dl>
    <dt class="s">F9</dt>
    <dd>Toggle breakpoint</dd>
    <dt class="s">F5</dt>
    <dd>Start/Continue</dd>
    <dt class="s">Shift+F5</dt>
    <dd>Stop</dd>
    <dt>F11 / Shift+F11<dt>
    <dd>Step into/out</dd>
    <dt>F10</dt>
    <dd>Step over</dd>
    <dt>Ctrl+K Ctrl+I</dt>
    <dd>Show hover</dd>
<dl>

<h2>Integrated terminal</h2>
<dl>
    <dt class="s">Ctrl+`</dt>
    <dd>Show integrated terminal</dd>
    <dt class="s">Ctrl+Shift+`</dt>
    <dd>Create new terminal</dd>
    <dt class="s">Ctrl+C</dt>
    <dd>Copy selection</dd>
    <dt class="s">Ctrl+V</dt>
    <dd>Paste into active terminal</dd>
    <dt class="s">Ctrl+ ↑/↓ </dt>
    <dd>Scroll up/down</dd>
    <dt class="s">Shift+ PgUp/PgDn</dt>
    <dd>Scroll page up/down</dd>
    <dt class="s">Ctrl+ Home/End<dt>
    <dd>Scroll to top/bottom</dd>

Other operating systems’ keyboard shortcuts and additional unassigned shortcuts available at [aka.ms/vscodekeybindings](aka.ms/vscodekeybindings)

<style>
    body {
        background: #fff;
        color: #000;
    }
    dl {
        color: #444;
    }
    dt.s{
        color: #000;
        font-weight: 700;
    }
    blockquote{
        background-color: #eee;
    }
</style>