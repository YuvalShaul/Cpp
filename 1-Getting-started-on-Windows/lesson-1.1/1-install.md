# Step 1: Installing the Toolchain

To get started, you need to install the core compiler and tools required to build native Windows applications.

## Hands-on Setup

1. Download and launch the **Visual Studio 2022 Installer**.
2. Under the **Workloads** tab, locate the Desktop & Mobile section.
3. Check the box for **"Desktop development with C++"**. 
4. Keep the default optional components selected on the right (this ensures you get the MSVC compiler tools and the Windows SDK).
5. Click **Install** and wait for the process to complete.

> 💡 **Why this workload?** Visual Studio is modular. Checking this specific workload ensures your machine gets `cl.exe` (the C++ compiler) and the standard system headers (like `<iostream>`) without bloating your hard drive with web or mobile development tools.

Next step: [Building Your First Program](1-first-program.md)
