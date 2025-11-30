# Linux DevOps Setup

This guide assumes you are using a Debian-based distribution (like Ubuntu).

## 1. Update System

Always start by updating your package list.

```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install Git

```bash
sudo apt install git -y
git --version
```

## 3. Install VS Code

1.  Download the `.deb` package from the [VS Code website](https://code.visualstudio.com/).
2.  Install it using apt:

```bash
sudo apt install ./<file-name>.deb
```

Alternatively, use Snap:

```bash
sudo snap install code --classic
```

## 4. Install Docker

Install Docker Engine using the convenience script (for development environments):

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

Add your user to the docker group to run without sudo:

```bash
sudo usermod -aG docker $USER
# Log out and log back in for changes to take effect
```

## 5. Install Additional Tools

```bash
# Install curl and wget if missing
sudo apt install curl wget -y
```