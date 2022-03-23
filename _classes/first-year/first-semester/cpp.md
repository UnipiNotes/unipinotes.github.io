---
layout: class
title: Αρχές προγραμματισμού [C/C++] | Class Notes
slug: cpp
categories: first-year first-semester
---

# Αρχές προγραμματισμού [C/C++]

## Class Notes

<br />

## Installing C++

<br />

### Windows

[How To Easily Install The C++ Programming Language On Windows](https://randerson112358.medium.com/how-to-install-the-c-programming-language-on-windows-c9813f1c5abb)

<br />

### MacOS

* Installing using Homebrew:

	```bash
	brew install --with-toolchain llvm
	brew update
	brew upgrade
	```
	Τώρα το προσθέτουμε στο PATH μας:
	
	```bash
	echo 'export PATH="/usr/local/opt/llvm/bin:$PATH"' >> ~/.bash_profile
	export CC := /usr/local/opt/llvm/bin/clang
  export CXX := $(CC)++
	```

<br />

### Linux

Τα περισσότερα Linux συστήματα έρχονται με προεγκατεστημένο compiler οπότε δεν χρειάζεται να κάνουμε τίποτα.

<br />

## Choosing an IDE or a Text Editor

Ως επιλογές έχουμε τις εξής:

### IDE

1. [Eclipse](https://www.eclipse.org/downloads/packages/release/2021-03/r/eclipse-ide-cc-developers) [Windows/Linux/MacOs]
2. [Code::Blocks](https://www.codeblocks.org/) [Windows/Linux/MacOs]
3. [Visual Studio](https://visualstudio.microsoft.com/vs/) [Windows]
4. [CLion](https://www.jetbrains.com/clion/) [Windows/Linux/MacOs]

**Σημείωση**: Το **Visual Studio** και το **CLion** είναι επί πληρωμή αλλά τα παρέχει το πανεπιστήμιο δωρεάν. Οπότε μην τα αγοράσετε.

### Text Editors

1. [Visual Studio Code](https://code.visualstudio.com/#alt-downloads) [Windows/Linux/MacOS]
2. [Atom](https://atom.io/) [Windows/Linux/MacOs]
3. [Emacs](https://www.gnu.org/software/emacs/) [Windows/Linux/MacOs]
4. [Notepad++](https://notepad-plus-plus.org/) [Windows]
5. [Visual Studio Codium](https://vscodium.com/) [Windows/Linux/MacOs]

**Σημείωση**: Όλα τα Text Editors που αναφέρθηκαν είναι δωρεάν. Υπάρχουν προφανώς πολλά περισσότερα, αλλά νομίζω ένα από αυτά τα πέντε αρκούν. Επίσης θα ήταν καλό να δείτε πως να σετάρετε τον Text Editor της επιλογής σας για **C**. Πχ για το **Visual Studio Code** η διαδικασία είναι [αυτή](https://code.visualstudio.com/docs/languages/cpp).

## Websites

* [Οι δικές μου σημειώσεις για C](https://github.com/unipi-projects/extras/blob/main/Languages/C/README.md)
* [TutorialsPoint Learn C++](https://www.tutorialspoint.com/cplusplus/index.htm)

## Videos

Δεν χρειάζεται κάποιο βίντεο tutorial για τις απαιτήσεις του μαθήματος.
