# Computer Basics and Developer Tools

## What Are the Basic Parts of a Computer?
A computer consists of several essential components:

1. **Central Processing Unit (CPU)** – The brain of the computer, responsible for executing instructions.
2. **Memory (RAM)** – Temporary storage for currently running programs.
3. **Storage Devices** – Hard drives (HDDs) and Solid-State Drives (SSDs) for permanent data storage.
4. **Motherboard** – The main circuit board connecting all components.
5. **Power Supply Unit (PSU)** – Converts electricity to a usable form for the computer.
6. **Input Devices** – Keyboard, mouse, touchpad, etc.
7. **Output Devices** – Monitor, speakers, printer, etc.

Example command to check system information in Linux:
```bash
lsblk   # Lists storage devices
cat /proc/cpuinfo   # Displays CPU details
```

## How Can You Effectively Work With Your Keyboard, Mouse, and Other Pointing Devices?

- **Keyboard Shortcuts**:
  - `Ctrl + C`: Copy
  - `Ctrl + V`: Paste
  - `Ctrl + Z`: Undo
  - `Alt + Tab`: Switch between windows

- **Mouse Usage**:
  - **Left-click**: Select items
  - **Right-click**: Open context menus
  - **Scroll Wheel**: Scroll through pages

- **Touchpad Gestures**:
  - Two-finger scroll
  - Three-finger swipe for switching applications

## What Are the Different Types of Internet Service Providers?

1. **Dial-Up** – Uses telephone lines; slow speeds.
2. **DSL (Digital Subscriber Line)** – Faster than dial-up, still uses phone lines.
3. **Cable** – Uses coaxial cables for high-speed internet.
4. **Fiber-Optic** – High-speed internet using fiber-optic cables.
5. **Satellite** – Internet access via satellite; useful in remote areas.
6. **Mobile Broadband** – Internet through cellular networks (3G, 4G, 5G).

Example of checking your internet connection in Linux:
```bash
ping google.com  # Checks if the internet is working
```

## What Are Safe Ways to Sign Into Your Computer?

- **Use Strong Passwords**
- **Enable Two-Factor Authentication (2FA)**
- **Use Biometric Authentication (Fingerprint/Face ID)**
- **Use a Password Manager**
- **Avoid Public Wi-Fi for Logging In**

Example of creating a strong password in Python:
```python
import secrets
import string

characters = string.ascii_letters + string.digits + string.punctuation
password = ''.join(secrets.choice(characters) for _ in range(12))
print(password)  # Secure random password
```

## What Are the Different Types of Tools Professional Developers Use?

1. **Code Editors & IDEs**
   - Visual Studio Code, JetBrains IntelliJ, Eclipse
2. **Version Control Systems**
   - Git, GitHub, GitLab
   - Example Git command:
   ```bash
   git init  # Initialize a new Git repository
   ```
3. **Debugging Tools**
   - Chrome DevTools, GDB, Postman
4. **Containerization & Virtualization**
   - Docker, Kubernetes, VirtualBox
5. **CI/CD Tools**
   - Jenkins, GitHub Actions
6. **Package Managers**
   - npm (Node.js), pip (Python), apt (Linux)
7. **Cloud Platforms**
   - AWS, Google Cloud, Azure

This document provides a foundational overview of key computer concepts and developer tools.

