# Windows IT User Prompt Toolkit

A collection of PowerShell utilities designed to bridge the gap between high-privilege system environments (like RMM tools running as SYSTEM) and active user desktop sessions.

## Features
* **Session Bridging:** Successfully bypasses session isolation by deploying an interactive scheduled task configured with highest privileges and interactive logon type.
* **Concurrency Control:** Implements a system Mutex lock to prevent duplicate script instances or overlapping prompt windows from firing simultaneously.
* **Native GUI Integration:** Utilizes the Windows Presentation Framework (WPF) to present clean, native message boxes rather than legacy VBScript popups.
* **Flexible Deployment Options:** Includes scripts for both a one-time single-shot prompt and a customizable program update prompt template.

## Prerequisites
Make sure you have administrative privileges on the machine and a management tool capable of running scripts in the SYSTEM context.
* Clone or download this repository to your local machine.
* Review and configure the script parameters (such as replacing generic template variables like `(program)` if using the update prompt).
* Run the script via PowerShell or your preferred RMM platform:
```powershell
powershell.exe -ExecutionPolicy Bypass -File .\YourScript.ps1
