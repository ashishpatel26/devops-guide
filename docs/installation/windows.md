# Windows 11 DevOps Setup

This guide will help you set up a robust DevOps environment on Windows 11 using WSL2 (Windows Subsystem for Linux). This allows you to run Linux tools natively on Windows.

## 1. Install WSL2

Open PowerShell as Administrator and run:

```powershell
wsl --install
```

Restart your computer when prompted. By default, this installs Ubuntu.

## 2. Install Windows Terminal

Download **Windows Terminal** from the Microsoft Store. It provides a better experience for managing multiple shells (PowerShell, WSL, Command Prompt).

## 3. Install VS Code

Download and install [Visual Studio Code](https://code.visualstudio.com/).

**Extensions to install:**
*   **WSL**: To edit files inside your Linux distro.
*   **Docker**: For managing containers.
*   **HashiCorp Terraform**: For Infrastructure as Code.
*   **YAML**: For editing configuration files.

## 4. Install Docker Desktop

1.  Download [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop).
2.  Run the installer and ensure "Use WSL 2 based engine" is checked.
3.  Start Docker Desktop.
4.  Go to **Settings > Resources > WSL Integration** and enable integration with your Ubuntu distro.

## 5. Verify Installation

Open your Ubuntu terminal (via Windows Terminal) and run:

```bash
# Check Git (usually pre-installed in Ubuntu)
git --version

# Check Docker
docker --version
```