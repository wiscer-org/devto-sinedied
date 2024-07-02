---
title : VSCode - How to Jumps between Points in a File
tags : vscode, withscreenreader
published : true
description : Tips to jump between multiple points in Visual Studio Code (VSCode).
id: 1183087
---

<p>This article contains tips to jumps between points (combination of line & column number) in a single file
in VSCode for screen reader users (blind, visually impaired, etc).
</p>

<p>This article is based on personal experience.
</p>

## Background

<p>I often face situation where I have to jumps from 1 point to another line back and forth in a single file.
It is a bit challenging for me since now I am a screen reader user. 
</p>

<p>As an example, in JSON file below
I need to look for <code>sku</code>s in <code>products</code> to replace <code>sku</code> (xxx) in the <code>cart</code> array.
Imagine scenarios with much more products and more cart items.
It will require me to traverse through the <code>products</code> for each <code>cart</code> item.
</p>

<p>For this tutorial let's just say <code>carts</code>, that we need to fill in as a <code>work point</code>.
And <code>sku</code> field , that we will look for, as a <code>lookup point</code>.
</p>

{% embed https://gist.github.com/wiscer-org/48f2077ad3c3c2310a8006e5134db578 %}

## Sighted Users

<p>This is how a sighted user typically will complete the task:
</p>

1. Get the  `name` of the first `cart` item. Cursor is at <code>work point</code>.
2. Scroll to `products`.
3. Scan through the `products` until find the matching `name` (<code>lookup point</code>).
4. Copy the `sku`.
5. Scroll back to the first item of `cart` (<code>work point</code>).
6. Replace `xxx` with the copied `sku`.
7. Repeat from the beginning for the second item in `cart`.

<p>The steps above are pretty simple because a sighted user only need to scroll down/up without having to repeatedly press keys to navigate.
</p>

## Screen Reader Users

### The Challenge

<p>SC users (Screen reader users), on the other hand, do not use scrolling devices.
They only use keyboards to give input to computer.
SC users have to press key up / down to 'scroll' the pages.
</p>

<p>During the navigation process, SC users have to press up/down key to move cursor 1 line to read each line until reaching the intended 'section'.
It will require much longer time to complete simple task such as above, compared to sighted users.
</p>

<p>Below are tips I used to  workaround the challenge.
</p>

<p>Let's consider an initial condition for each tips
where the cursor is at <code>"name" : "Milk"</code> (line 4).
</p>

### Use `PgUp` and `PgDn` Keys

<p>Users can use <code>PgUp</code>, to move up 1 page, and <code>PgDn</code> to move down 1 page.
Until  approximately near the intended lines, the <code>lookup point</code>, user can use arrow up / down to read each line to get to the <code>lookup point</point>.
</p>

<p>The challenge SC users may have with this method
is to remember how many times they have to press <code>PgUp</code> or <code>PgDn</code> keys to jump back and forth betwen <code>work point</code> to <code>lookup point</code>.
The distance between <code>work point</code> and <code>lookup point</code> may change everytime lines are inserted or deleted between those 2 points.
</p>

### Use Line Numbers

<p>Another way to jump is by remember the line number of 
the <code>work point</code> and line number near the <code>lookup point</code>.
</p>

<p>To jump to a certain line number in VSCode :
- Press `Ctrl` + ` G` to open a modal.
- Type in the destination line number, then press `Enter`.
</p>

<p>With this method SC users have to remember the line numbers and 
they will change everytime a line is inserted or deleted between <code>work point</code> and <code>lookup point</code>.
</p>

### Find 'dummy' anchors

<p>This was the method I preferred compared to the previous ones.
We can use dummy anchors to mark the <code>work point</code> and <code>lookup point</code>.
Dummy anchor, in my own term, is a sequence of characters that not existed in the file.
</p>

<p>For example we can type `aaa` 1 line above <code>work point</code> and `bbb` near the <code>lookup point</code>.
I use `aa` and `bbb` because I now there are no such substring in the related file
and it just faster to type those characters.
Then I use VSCode 'find' tool, press `Ctrl` + `F`, to jump between <code>work point</code> and <code>lookup point</code>.
</p>

<p>The downside of this method is we have to remember to remove those dummy anchors after being used,
and we have to move those dummy anchors if we want to change the jumping points.
This is still not the ideal solution to match the scrolling speed used by sighted users.
</p>

### Use multiple 'editor Group'

<p>This is the ideal method I found out a while ago.
</p>

<p>'Editor group' is group of 1 or multiple files or tabs. 
One of the benefit of usin multiple editors is to compare same file of different version (commit) side by side.
We can also view the exactly same file version in multiple editor group at the same time. 
Any changes we make to file `xxx` in any editor group will instantly reflected in the same file `xxx` in other editor group.
</p>

<p>When we start VSCode, by default, we will only have 1 editor group (Editor group 1).
Pressing `Ctrl` + `2` will open empty editor group 2, `Ctrl` + `3` will open empty editor group 3, and so on.
</p>

<p>Below are the steps to jumps between <code>work point</code> and <code>lookup point</code> back and forth :
</p>

1. Press `Ctrl` + `\` to open new editor group with the exact files currently being opened. The cursor will also at the same point (<code>work point</code>), but editor group 2 is active now.
2. Move the cursor to <code>lookup point</code>, copy the required `sku`.
3. Press `Ctrl` + `1`. This will move focus to editor group 1 with the cursor at the same position (<code>work point</code>).
4. Paste the `sku`.
5. Press `Ctrl` + `2` to focus on the editor group 2. Cursor on the editor groop 2 is still at the <code>lookup point</code>. 
6. Press `Ctrl` + `1` if we want to focus back to editor group 1.

<p>We can use this method to jump between multiple points back and forth.
</p>

<p>This method, IMHO, is faster than the 'scrolling' method commonly used by sighted users.
To close editor group2, just close all the file in the editor group 2.
Press `Ctrl` + `w` to close the currently focused file.
</p>

## Conclusion

<p>I just found out about the 'multiple editor groups' method few weeks ago.
I am still trying to make that method a habit.
By far using multiple editor groups to jump between points really increase my productivity.
</p>

<p>I had been looking for a perfect way to jump between multiple points for a long time.
By sharing my experience I hope this article could help some people, both sighted and screen reader users.
</p>

Good luck !

