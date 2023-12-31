
---

layout: single

title: "HackTheBox"

permalink: /ctfs/hackthebox

toc: true

toc_label: "Table of Contents"

toc_icon: stream # tasks #"torii-gate"

toc_sticky: true

---

  

> HackTheBox Writeups

  

# Introduction

  

This is writeup for Hack The Box challenges

  

# RE

  

### Behind The Scenes

  

***Solution:***

  

Looking at the main function, we can see invalidInstructionException function,

by inspecting it, it points to memory addres 001012e6 with the instruction 'UD2' and there Ghidra has not assembled the instructions below UD2.. Assemble the code by highlighting all unassembled code and press 'D', and replace all UD2 instruction with 'NOP', the source code will now show nested if statements that reveal the flag.

  

https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html

  

UD2 “generates an invalid opcode exception"This instruction is provided for software testing to explicitly generate an invalid opcode exception. The opcodes for this instruction are reserved for this purpose.”

  

Ghidra stops disassembling the file after the first occurrence of UD2

  

**Notice:** This is an important info notice.

{: .notice}

{: .notice--primary}

{: .notice--info}

{: .notice--warning}

{: .notice--danger}

{: .notice--success}

  

```

iVar1 = strncmp(*(char **)(in_RSI + 8),"Itz",3)

if (iVar1 == 0)

iVar1 = strncmp((char *)(*(long *)(in_RSI + 8) + 3),"_0n",3)

if (iVar1 == 0)

iVar1 = strncmp((char *)(*(long *)(in_RSI + 8) + 6),"Ly_",3)

if (iVar1 == 0)

iVar1 = strncmp((char *)(*(long *)(in_RSI + 8) + 9),"UD2",3)

if (iVar1 == 0)

printf("> HTB{s}\n",*(undefined8 *)(in_RSI + 8))

uVar2 = 0

```

  

Alternatively, we can run hexeditor on linux and type 'ctrl+w' to search for the flag. The keyword being 'HTB'

  

flag: HTB{Itz_0nLy_UD2}

  

## racecar

  

```┌──(root㉿kali)-[/home/kali/Downloads/HackTheBox/racecar]

└─# file racecar

racecar: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=c5631a370f7704c44312f6692e1da56c25c1863c, not stripped

```

  

not-stripped means that debugging info is still present.

  

readelf -s racecar

  

## SimpleEncryptor

  

hexdump -C flag.enc

  

xxd flag.enc

  

solution: write a reverse code

  

gcc scriptReverseEncryption.c -o test

  

flag: HTB{vRy_s1MplE_F1LE3nCryp0r}