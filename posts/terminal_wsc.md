---
title: Windows Terminal with Screen Reader
published: true
description: Tips on how to use  terminal application such as Powershell with NVDA screen reader.
tags: 'terminal, powershell, nvda, screenreader'
cover_image: null
canonical_url: null
---
When I first started using a screen reader, one of the biggest challenges I faced was operating terminal applications like Powershell. It took me quite some time to become comfortable navigating and using these terminal apps.

This article shares tips on operating Powershell and other terminal applications using the NVDA screen reader (Desktop keyboard layout), based on my personal experience. It is a work-in-progress article that will be updated over time.

## Reading Text in the Terminal
In the terminal, the cursor is always at the bottom. To read text, use the Navigator Object. For example, to read the previous line use `Numpad 7`for Desktop Layout. Full description about the Navigator Object navigation can be found in [NVDA Command Key Quick Reference](https://www.nvaccess.org/files/nvdaTracAttachments/455/keycommands%20with%20laptop%20keyboard%20layout.html) page.


## Copying Text
To copy a range of text in the terminal, follow these steps:
1. Mark the start of the text to be copied: 
   - Use the Navigator Object to move to the starting point of the text you want to copy. 
   - Press `Caps Lock` + `F9`.
2. Mark the end of the text:
   - Use the Navigator Object to move to the endpoint of the text selection.
   - Press `Caps Lock` + `F10` twice. (Hold the `Caps Lock` and then quickly press `F10` twice.)

After completing these steps, the selected text will be copied to the clipboard.