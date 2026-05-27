## Lesson 1.2: Types and Variables


Welcome to this foundational C++ learning module! This guide is carefully structured to take you from a complete beginner to writing your first interactive console program. The core theme of this module is mastering **Variables, Basic Data Types, and Console I/O**, which form the bedrock of all computer software.

Follow the suggested reading path below to maximize your understanding, then put your skills to the test with the practical hands-on exercise.

---

## 🗺️ Suggested Reading Path & Learning Strategy

To get the most out of these materials, read them in the following specific order. Each file builds directly upon the concepts introduced in the previous one.

### 1. 📂 `cpp_preprocessor.md` (The Doorway to C++)

* **Why start here?** Before you can write or understand any C++ program, you need to understand how files talk to each other. When you see `#include <iostream>` at the top of a file, you are using the preprocessor.
* **Key Focus:** Learn the meaning behind `#include` and how the preprocessor prepares your code for compilation. This file de-mystifies that magical line of code you see at the top of every C++ file.

### 2. 📂 `cpp_types.md` (The Master Reference)

* **Why read this next?** This is your comprehensive, complete reference table of all core C++ data types.
* **Key Focus:** Study how C++ categorizes data (integers, floating-point numbers, characters, and booleans) and pay attention to how much memory (bytes) each type occupies. *Don't try to memorize the whole table right now!* Treat this as a dictionary that you will keep open and refer back to constantly.

### 3. 📂 `using_basic_types.md` (The Tutorial)

* **Why read this next?** Now that you know what types exist in theory, this tutorial shows you how to actually use them in practice.
* **Key Focus:** Learn how to *declare* and *initialize* variables. Pay attention to syntax rules, naming conventions, and how choosing a variable's data type alters how the computer handles its numerical or logical value.

### 4. 📂 `input_and_output.md` (Making it Interactive)

* **Why read this last?** Variables are only useful if you can feed data into them and see what happens inside.
* **Key Focus:** Master `std::cout` (Console Output) to display messages to the user, and `std::cin` (Console Input) to read keyboard strokes directly into your variables. This file bridges the gap between static variables and a dynamic user experience.

---

## 🎯 Practical Learning Exercise

Once you have completed the readings, you are ready to build the core deliverable for this module. This exercise requires you to synthesize concepts from all four documents into a single, cohesive program.

### 📋 Deliverable: Console-Based System Configuration Logger

**Objective:** Write a complete C++ console application that prompts a user for server/system technical metrics, performs calculations on those numeric values, and outputs a neatly formatted specification report.

#### 🔧 Functional Requirements

1. **Preprocessor Setup:**
* Correctly use `#include <iostream>` at the very top to unlock console read/write operations (`cin` and `cout`). No other libraries are required.


2. **User Data Input (`std::cin`):**
Your program must prompt the user and safely capture the following system specifications using primitive types:
* **Processor Core Count:** (Integer type - e.g., `8`, `16`)
* **Total Installed RAM (in GB):** (Floating-point decimal type - e.g., `32.0`, `16.5`)
* **Assigned System Security Tier:** (A single character type - e.g., `'A'`, `'B'`, `'C'`)
* **Is System Remotely Accessible?** (Boolean type representation - `1` for true, `0` for false)


3. **Data Transformation & Calculations:**
* Compute the **Total Available Memory in Megabytes (MB)** assuming that $1 \text{ GB} = 1024 \text{ MB}$. Store this result in a separate descriptive variable.
* Perform an arithmetic operation to simulate resource allocation: calculate how much RAM would be allocated per CPU core if divided evenly ($\text{RAM per Core} = \text{Total RAM} / \text{Core Count}$).


4. **Formatted Data Output (`std::cout`):**
Print a clean, visually structured summary block to the terminal displaying the collected metrics alongside your newly calculated data. Use newlines (`\n` or `std::endl`) to create a readable report layout.

---

## 💡 Quick Tips for Success

* **Variable Initialization:** Remember from `using_basic_types.md` that uninitialized variables in C++ contain garbage data. Always initialize your numerical and character values upon declaration (e.g., `int cores = 0;`, `char tier = 'U';`).
* **Formatting Booleans:** By default, printing a `bool` variable via `std::cout` displays a simple `1` or `0`. That is perfectly acceptable for this console log. No complex logic is required.

