# Oversimplified

> **"A programming language, but humanized."**

**Oversimplified** is a minimal procedural programming language designed to strip away complex syntax and rely on plain English vocabulary. It runs on the **JFLAP** simulator and serves as an educational model for demonstrating the "Front-End" phases of compiler design (Lexical and Syntax Analysis).

## 📂 Project Overview

This project simulates a compiler's initial processing steps using Automata Theory. Instead of compiling to machine code, the language is parsed and validated using JFLAP's finite state machines.

### Core Components
| Component | JFLAP Model | Function |
|-----------|-------------|----------|
| **Lexer** | **DFA** (Deterministic Finite Automaton) | Scans input text and identifies valid tokens (keywords, literals). |
| **Grammar** | **CFG** (Context-Free Grammar) | Defines the hierarchical rules and structure of the language. |
| **Parser** | **PDA** (Pushdown Automaton) | Validates that the sequence of tokens follows the grammatical rules. |

---

## ⚡ Features

* **Human-Readable Keywords:** Replaces abstract symbols with words (e.g., `plus` instead of `+`, `set` instead of `=`).
* **Prefix Notation:** Arithmetic operations precede their operands (e.g., `plus 5 5`).
* **Strict Typing:** Supports 5 basic types: `number`, `text`, `fact` (boolean), `symbol`.
* **Control Flow:** Includes `test` (conditionals) and `repeat`/`whenever` (loops).

---

## 🚀 Getting Started

### Prerequisites
* [**JFLAP 7.1**](http://www.jflap.org/) (Java Formal Languages and Automata Package)
* **Java Runtime Environment (JRE)**

### How to Run
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/sgmad/oversimplified.git](https://github.com/sgmad/oversimplified.git)
    ```
2.  **Open JFLAP:** Run the `.jar` file.
3.  **Test the Logic:**
    * **To check Vocabulary:** Open `oversimplified_DFA.jff` and use the "Input" menu to test words like `set` or `number`.
    * **To check Syntax:** Open `oversimplified_PDAv2.jff`, select "Input" > "Step with Closure", and enter a full command string (e.g., `set number x = 10`).

---

## 📖 Language Syntax Guide

### 1. Variables
Variables must be declared with a type.
```text
set number age = 20
set text name = "Alice"
set fact isReady = true
````

### 2\. Arithmetic (Prefix Notation)

Operators come *before* the values.

```text
say plus 10 5      (Calculates 10 + 5)
say multiply 2 x   (Calculates 2 * x)
```

### 3\. Conditionals

Uses `test` (if) and `fail` (else).

```text
test isReady {
    say "Go"
} fail {
    say "Stop"
}
```

### 4\. Loops

Uses `repeat` (for) or `whenever` (while).

```text
set number count = 3
repeat count {
    say "Running..."
}
```

-----

## 📄 File Manifest

  * `oversimplified_DFA.jff` - Token Recognizer.
  * `oversimplified_PDAv2.jff` - Structure Validator.
  * `oversimplified_CFGv2.jff` - Context-Free Grammar.

-----

## 📚 References

  * Rodger, S.H. & Finley, T.W. (2006). *JFLAP: An Interactive Formal Languages and Automata Package*.
  * Aho, A.V., et al. (2006). *Compilers: Principles, Techniques, and Tools*.
  * C. Hamblin (1962). *Translation to and from Polish notation*.

-----
