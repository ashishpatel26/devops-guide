# macOS DevOps Setup

This guide covers setting up a DevOps environment on macOS using Homebrew.

## 1. Install Homebrew

Homebrew is the package manager for macOS. Open Terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Follow the on-screen instructions to add Homebrew to your PATH.

## 2. Install iTerm2 (Optional but Recommended)

iTerm2 is a replacement for the default Terminal app.

```bash
brew install --cask iterm2
```

## 3. Install Core Tools

Install Git and other essentials:

```bash
brew install git wget curl tree
```

## 4. Install VS Code

```bash
brew install --cask visual-studio-code
```

**Recommended Extensions:**
*   Docker
*   HashiCorp Terraform
*   YAML
*   Kubernetes

## 5. Install Docker

We recommend using Docker Desktop for Mac.

```bash
brew install --cask docker
```

Start Docker from your Applications folder.

## 6. Verify Installation

Open a new terminal window and run:

```bash
git --version
docker --version
```