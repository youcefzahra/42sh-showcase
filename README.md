# 🐚 42sh - Custom POSIX Shell in C

> **Showcase Repository:** To adhere to EPITA's anti-plagiarism guidelines, the source code remains private. This repository documents the technical architecture. A compiled version is available in the Releases section for testing.

## 📖 Project Overview

The **42sh** is a major EPITA project requiring the development of a complete UNIX command-line interpreter from scratch, strictly following the POSIX standard. This involves advanced system programming, abstract syntax tree (AST) generation, and process management.

## 💡 My Core Contributions

[⚠️ YOUCEF, DIS-MOI CE QUE TU AS CODÉ EXACTEMENT POUR QUE JE RÉDIGE CETTE PARTIE DE FAÇON TECHNIQUE : Lexer ? Execution ? Redirections ? Built-ins ?]

## ✨ Technical Features

* **Process Execution:** Binary resolution via `$PATH`, child process creation using `fork`, and execution via `execvp`.
* **Built-in Commands:** Custom implementation of fundamental commands (`cd`, `echo`, `exit`, `export`, `unset`, `set`, `.`).
* **Control Structures:** Full support for conditional branching (`if/elif/else/fi`) and loops (`while`, `until`, `for` with `break`/`continue`).
* **Logical Operations:** Command chaining with AND (`&&`), OR (`||`), and negation (`!`).
* **Pipelines & Redirections:** Process communication using pipes (`|`) and comprehensive file descriptor management for redirections (`>`, `<`, `>>`, `>&`, `<&`, `<>`).
* **Variable Expansion:** Environment variable resolution and special parameters support (e.g., `$?` for exit statuses).
* **Execution Contexts:** Support for command blocks `{ ... }` and subshells `( ... )`.
* **Quoting Mechanisms:** Handled single (`'`) and double (`"`) quotes for escaping characters and preventing expansion.

## 🏗️ Architecture Pipeline

1. **Lexical Analysis (Lexer):** Tokenization of the standard input or script files.
2. **Syntax Analysis (Parser):** Construction of the Abstract Syntax Tree (AST) based on strict shell grammar rules.
3. **Execution Engine:** Recursive traversal of the AST, applying redirections, creating pipelines, and executing the corresponding nodes.

## 🎯 Testing the Shell

A pre-compiled binary is available.

1. Navigate to the **[Releases](../../releases)** tab.
2. Download the release archive.
3. Open a Linux terminal (or WSL) and execute:

```bash
tar -xvf 42sh_release.tar.gz
chmod +x 42sh
./42sh
```

## 👥 The Team
* **[Wael Akhdar](https://github.com/Wael-Akhdar)** : Project Manager & AST/Parser
* **[Youcef Zahra](https://github.com/youcefzahra)** : [Ton rôle précis ici]
* **[Jessim Ziani](https://github.com/jessim-ziani)** : [Son rôle]
* **[Louis-Maximilien Chappuit]()** : [Son rôle]
