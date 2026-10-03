# Oopsie

## 🧩 Challenge Overview

**Category:** Pwn / Binary Exploitation
**Difficulty:** Beginner
**Target:** `oopsie`

Welcome to **Oopsie** — your first step into binary exploitation.

In this challenge, you'll encounter a classic **stack-based buffer overflow** caused by unsafe input handling.

Your goal is to understand what happens when a program writes more data into a buffer than it was designed to hold, and use that knowledge to trigger the intended behavior of the challenge.

---

## 📁 Files

The challenge directory contains:

```text
.
├── oopsie
├── main.c
└── challenge.txt
```

### `main.c`

The source code of the vulnerable program.

Take your time to read through it and understand:

* Where user input is stored
* How large the buffer is
* How the input is read
* What happens after the input is received

### `oopsie`

The compiled binary.

This is the program you will ultimately be interacting with.

### `challenge.txt`

Contains the challenge description and objective.

---

## 🎯 Objective

Your objective is to exploit the vulnerability in `oopsie` and trigger the behavior required by the challenge.

The challenge is **not** about guessing the flag.

Instead, investigate the program and figure out:

1. Where the vulnerability is.
2. Why the vulnerability exists.
3. What happens when the buffer is overwritten.
4. How the program behaves when you provide more input than expected.

---

## 🔍 Where Should I Start?

Start with the source code:

```bash
cat main.c
```

Look carefully at how the program handles input.

You should then run the program normally:

```bash
./oopsie
```

Try different inputs and observe how its behavior changes.

For example:

```bash
./oopsie
```

Then provide a normal string and see what happens.

---

## 🧠 Things to Think About

While investigating, ask yourself:

* How big is the buffer?
* How much data does the program allow you to write?
* Is there any protection against writing past the end?
* What is located around the buffer in memory?
* What happens when you provide significantly more input?
* Can you reproduce the crash consistently?

You may find it useful to inspect the program with debugging tools such as **GDB**.

---

## 🛠️ Useful Tools

You can use standard Linux tools while investigating the binary:

```bash
gdb ./oopsie
```

Some useful GDB commands to explore are:

```text
run
break
info registers
x
disassemble
```

You don't necessarily need to understand all of them immediately. Use them to gradually build a picture of what the program is doing.

---

## 💡 Hint

A buffer has a fixed size.

What do you think happens when the program receives **more data than the buffer can hold**?

Start there.

---

## 🚩 Flag Format

If you successfully complete the challenge, the flag will follow this format:

```text
0XATTACK{...}
```

---

## 📚 What You'll Learn

By completing this challenge, you should gain an introduction to:

* Stack memory
* Local variables
* Buffer overflows
* Stack corruption
* Program crashes
* x86-64 registers
* Basic GDB usage
* Understanding vulnerable C programs

This challenge is intended as a foundation for the more advanced pwn challenges that follow.

---

## ⚠️ Important

This is a controlled educational environment.

Only experiment against the provided challenge binary or the challenge server. Do not apply these techniques to systems you do not own or have permission to test.

Good luck, and happy pwning! 🐧

