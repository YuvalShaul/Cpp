# C++ Program Creation and File Types (Windows)

## 1. The Build Pipeline

### Preprocessing
```text
[ file.cpp / file.h ]   --- Preprocessor --->>   [ file.i ]

```

### Compilation

```text
[ file.i ]              --- Compiler ---------->>   [ file.obj ]

```

### Static Linking

```text
[ file.obj ]            --- Static Linker ---->>   [ file.exe ]
  + [ file.lib ]

```

### Dynamic Linking

```text
[ file.obj ]            --- Dynamic Linker --->>   [ file.exe ] ---> (Requires [ file.dll ] at runtime)

```

---

## 2. Associated File Types

### `.cpp` (Source File)

* Contains the primary implementation of functions and logic written in C++.
* Acts as the initial input for the preprocessing and compilation pipeline.

### `.h` / `.hpp` (Header File)

* Stores function declarations, class definitions, and macros shared across multiple source files.
* Allows different compilation units to recognize external interfaces before linking.

### `.i` (Preprocessed Source File)

* The text output generated after expanding macros and resolving all header inclusions.
* Used to inspect code exactly as it appears before translation into machine code.

### `.obj` (Object File)

* An unlinked binary file containing machine code instructions and a symbol table.
* Represents a single compiled module that still requires addresses to be resolved by a linker.

### `.lib` (Static Library / Import Library)

* An archive of multiple object files bundled together for reusability, or a collection of references for dynamic links.
* Its machine code is copied and permanently embedded directly into the final executable during static linking.

### `.dll` (Dynamic Link Library)

* A compiled binary library that is loaded and linked into memory at runtime rather than build time.
* Allows multiple running programs to share a single copy of the library, saving system memory.

### `.exe` (Executable Binary)

* The final, fully linked machine-code program that can be natively run by the Windows operating system.
* Contains the complete program entry point, execution layout, and final memory addresses.

```

```