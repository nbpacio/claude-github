# Claude and GitHub Integration Guide

This guide walks you through integrating Claude with GitHub on both Windows and Linux systems.

## Prerequisites

- Claude account
- GitHub account
- Visual Studio Code (VSCode) installed
- Administrator access to your system

---

## Windows Setup

### Step 1: Add Claude Code for VSCode

1. Open Visual Studio Code
2. Go to the Extensions marketplace (Ctrl + Shift + X)
3. Search for "Claude Code"
4. Click on the official Claude Code extension by Anthropic
5. Click "Install" and wait for the installation to complete
6. Once installed, you should see the Claude Code icon in the activity sidebar

### Step 2: Install Claude CLI

1. Open PowerShell as Administrator
2. Run the following command to install Claude CLI via npm:
   ```powershell
   npm install -g @anthropic-ai/claude-cli
   ```
   If you don't have npm installed, first install Node.js from [nodejs.org](https://nodejs.org)

3. Verify the installation by running:
   ```powershell
   claude --version
   ```

### Step 3: Install GitHub CLI

1. Download the GitHub CLI installer from [cli.github.com](https://cli.github.com)
2. Run the installer and follow the on-screen prompts
3. Alternatively, if you have Chocolatey installed, run:
   ```powershell
   choco install gh
   ```

4. Verify the installation:
   ```powershell
   gh --version
   ```

### Step 4: Login to GitHub via CLI

1. Open PowerShell
2. Run the authentication command:
   ```powershell
   gh auth login
   ```
3. Follow the prompts:
   - Choose **GitHub.com** when asked which Git service
   - Choose **HTTPS** for the protocol
   - Authenticate with your browser when prompted
   - Authorize the GitHub CLI to access your account

4. Verify authentication was successful:
   ```powershell
   gh auth status
   ```

### Step 5: Open Claude and Install GitHub App

1. Open Claude in your browser or Claude desktop application
2. Navigate to the integrations or settings section
3. Look for the GitHub integration option
4. Click "Install GitHub App" or "Connect to GitHub"
5. You'll be redirected to GitHub to authorize the Claude app
6. Review the permissions and click "Authorize"
7. Return to Claude and confirm the connection is successful

---

## Linux Setup

### Step 1: Add Claude Code for VSCode

1. Open Visual Studio Code
2. Go to the Extensions marketplace (Ctrl + Shift + X)
3. Search for "Claude Code"
4. Click on the official Claude Code extension by Anthropic
5. Click "Install" and wait for the installation to complete
6. Once installed, you should see the Claude Code icon in the activity sidebar

### Step 2: Install Claude CLI

1. Open Terminal
2. Ensure npm is installed. If not, install Node.js:
   ```bash
   sudo apt update
   sudo apt install nodejs npm
   ```
   Or for other distributions, use your package manager (yum, pacman, etc.)

3. Install Claude CLI globally:
   ```bash
   sudo npm install -g @anthropic-ai/claude-cli
   ```

4. Verify the installation:
   ```bash
   claude --version
   ```

### Step 3: Install GitHub CLI

1. Add the GitHub CLI repository to your system:
   ```bash
   # For Ubuntu/Debian
   sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
   sudo apt-add-repository https://cli.github.com/packages
   sudo apt update
   sudo apt install gh
   ```

   Or for other distributions:
   ```bash
   # For Fedora/RHEL
   sudo dnf install gh
   
   # For Arch
   sudo pacman -S github-cli
   ```

2. Verify the installation:
   ```bash
   gh --version
   ```

### Step 4: Login to GitHub via CLI

1. Open Terminal
2. Run the authentication command:
   ```bash
   gh auth login
   ```

3. Follow the prompts:
   - Choose **GitHub.com** when asked which Git service
   - Choose **HTTPS** for the protocol (or SSH if preferred)
   - Select "Login with a web browser" when prompted
   - Your browser will open for authorization
   - Authorize the GitHub CLI to access your account

4. Verify authentication was successful:
   ```bash
   gh auth status
   ```

### Step 5: Open Claude and Install GitHub App

1. Open Claude in your browser or Claude desktop application
2. Navigate to the integrations or settings section
3. Look for the GitHub integration option
4. Click "Install GitHub App" or "Connect to GitHub"
5. You'll be redirected to GitHub to authorize the Claude app
6. Review the permissions and click "Authorize"
7. Return to Claude and confirm the connection is successful

---

## Troubleshooting

**Claude CLI not found after installation:**
- Ensure your terminal has been restarted after installation
- Check that npm is in your PATH
- Try reinstalling: `npm install -g @anthropic-ai/claude-cli`

**GitHub CLI authentication fails:**
- Verify your GitHub credentials are correct
- Check your internet connection
- Ensure pop-ups are not blocked in your browser
- Try again with: `gh auth logout` followed by `gh auth login`

**GitHub App won't connect in Claude:**
- Clear your browser cache and cookies
- Try using a different browser
- Ensure you're using an updated version of Claude
- Check that you have proper permissions on your GitHub account

---

## Next Steps

Once integration is complete, you can:
- Use Claude to help analyze and work with your GitHub repositories
- Leverage Claude Code in VSCode for AI-assisted development
- Use Claude CLI for command-line interactions
- Automate workflows between Claude and GitHub

