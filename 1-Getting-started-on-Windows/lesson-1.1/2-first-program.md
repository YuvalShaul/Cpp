# Step 2: Code Anatomy & Compiling

Before we write code, you need to understand how Windows structures C++ developments.

## Understanding Windows Project Anatomy

When working inside the Visual Studio ecosystem, you will encounter two primary file types that manage your application:

*   **Solutions (`.sln`):** The high-level container. A solution wraps one or more projects together, managing global build configurations and relationships between them.
*   **Projects (`.vcxproj`):** The actual build target. This MSBuild XML file contains the explicit list of source files, compiler switches, optimization flags, and linker settings for a specific executable or library.

---

## Hands-on Exercise: "Hello Windows"

Create a file named `main.cpp` on your computer and paste the following code into it:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello Windows!" << std::endl;
    return 0;
}



Track A: The IDE Workflow (The Abstraction)
Open Visual Studio 2022 and create a new Empty C++ Project.

Right-click the project in the Solution Explorer, select Add > Existing Item, and choose your main.cpp.

Press Ctrl + F5 (or navigate to Debug > Start Without Debugging).

The IDE will automatically generate the backend files, compile the code, and launch a console window showing your output.

Track B: The CLI Workflow (Under the Hood)
Now let's bypass the IDE entirely and compile this manually using the Microsoft Visual C++ (MSVC) compiler directly.

Click the Windows Start Menu, search for Developer PowerShell for VS 2022, and open it.

⚠️ Note: Standard PowerShell or CMD will not work out of the box because the path to the compiler is kept isolated. The Developer PowerShell automatically loads the environment variables needed to access the compiler.

Use the cd command to navigate to the folder where you saved your main.cpp.

Run the compiler manually by executing the following command:

PowerShell
   cl /EHsc /std:c++17 main.cpp
Deconstructing the Command:
cl: Invokes the MSVC Compiler (cl.exe).

/EHsc: Enables standard synchronous C++ exception handling (ensures objects are properly destroyed if an error is thrown).

/std:c++17: Instructs the compiler to use the ISO C++17 language standard.

main.cpp: Specifies the target source file to compile.

Type .\main.exe in your terminal to run your manually compiled binary!

Verification Checklist
You are officially finished with Lesson 1.1 when:

[ ] You can explain the difference between a .sln and a .vcxproj file.

[ ] Your program runs seamlessly using Ctrl + F5 in Visual Studio.

[ ] You see a fresh main.obj and main.exe generated in your directory after running the manual cl command.