# Control OC Project
Main GitHub repository of the Control OC project.

Control OC is a lightweight, fast, and secure operating system built for full control over your PC. 

🔗 [Official Website](https://controloc.vercel.app/) • [Source Code Repository](https://github.com/ControlOC/ControlOC-Source-Code/)

---

## 🎯 3 Main Goals of Control OC:
*   **Lightweight:** The ISO is only **210 MB** (around 29 times smaller than the Windows 11 installer).
*   **Incredible Speed:** Boots in just **~8 seconds** (tested on an HDD inside VirtualBox).
*   **Pre-installed Utilities:** Control OC comes with a bunch of built-in system utilities that weigh less than a single `.deb` package, providing a wide range of functionality right out of the box.

## 📦 4 Types of Supported Packages
You might think there are no programs for Control OC. You would be wrong! The system supports 4 package formats:
*   **Ckrnl Utility (`.cutil`):** Native Control OC utilities with wider functionality than standard packages.
*   **Tiny Core Utilities (`.tcz`):** Native Tiny Core Linux extensions, integrating perfectly with the system.
*   **AppImage:** Portable applications that work on any Linux-based distribution.
*   **Debian Packages (`.deb`):** Since most developers create apps exclusively for Debian, Control OC supports Debian packages out of the box (via an isolated `dpkg` environment).

## 🎨 Customization: OneTheme
Control OC is all about control, and customization is a huge part of it. 
**OneTheme** ensures that all Ckrnl Utility programs and the system UI share the same color palette. 

With OneTheme, you can:
*   Color **ControlScriptGUI** applications (Ckrnl Utility packages).
*   Change the **colors and settings** of the Window Manager.
*   Change the **position and icons** of Window Manager buttons.
*   **Decorate** your applications.
*   Transform your Control OC into a unified, **one-tone color system**.

## 🛡️ Security: Not just a pretty face
You might wonder: *"With all this control, does Control OC have vulnerabilities?"* No, security was a top priority:
*   **SRP (Secure Root Permission):** Protects you from secure data leaks by controlling root actions.
*   **SRP Data:** Allows your programs to safely store and contain sensitive data, preventing unauthorized leaks.
*   **AUP System (Another-User-Processes):** A unique privilege separation system.
    *   *How it works:* The system creates a separate, restricted user account to run GUI applications. Meanwhile, the system itself uses the native administrative user.
    *   *Why this is necessary:* Tiny Core Linux relies heavily on the native `tc` user for booting and system initialization. Changing or restricting `tc` directly would permanently block the system from starting. Therefore, AUP drops privileges for apps while keeping the boot process alive.
