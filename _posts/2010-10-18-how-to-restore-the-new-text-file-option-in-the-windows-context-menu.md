---
title: How to restore the new text file option in the windows context menu
date: 2010-10-18 00:00:00 Z
permalink: "/misc/how-to-restore-the-new-text-file-option-in-the-windows-context-menu/"
tags:
- misc
Published: 2010-10-18 00:00:00 Z
author: Chris S
layout: post
dsq_thread_id:
- 1084990532
---

This small registry snippet can be used if you've lost the Windows context menu's (right click menu inside explorer and your desktop) New->Text Document option.

Save the snippet below as &#8220;install.reg&#8221; (including the quotes) in Notepad, and then run it.

<!--more-->

<pre>Windows Registry Editor Version 5.00
[HKEY_CLASSES_ROOT\.txt]
"Content Type"="text/plain"
"PerceivedType"="text"
@="txtfile"
[HKEY_CLASSES_ROOT\.txt\OpenWithList]
[HKEY_CLASSES_ROOT\.txt\PersistentHandler]
@="{5e941d80-bf96-11cd-b579-08002b30bfeb}"
[HKEY_CLASSES_ROOT\.txt\ShellNew]
"ItemName"=hex(2):40,00,25,00,53,00,79,00,73,00,74,00,65,00,6d,00,52,00,6f,00,\
6f,00,74,00,25,00,5c,00,73,00,79,00,73,00,74,00,65,00,6d,00,33,00,32,00,5c,\
00,6e,00,6f,00,74,00,65,00,70,00,61,00,64,00,2e,00,65,00,78,00,65,00,2c,00,\
2d,00,34,00,37,00,30,00,00,00
"NullFile"=""
</pre>