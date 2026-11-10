# Workshop installation steps

Use supported stable releases. Follow the instructions for your OS.

Complete these installation steps before the workshop. GitHub Copilot for Azure,
Azure MCP Server, Azure Resource Manager MCP Server, and the Azure Agent plugin
will be explained and installed during the workshop. No advance installation of
these components is required.

## Required accounts

- [GitHub account](https://github.com/signup).
- [GitHub Copilot](https://github.com/features/copilot/plans). The Free plan should
  work for this workshop, subject to its usage limits.
- [Azure subscription](https://azure.microsoft.com/en-us/free/). Use your own
  subscription or one you have permission to access.

## 1. Install VS Code

[Download and installation instructions](https://code.visualstudio.com/docs/setup/setup-overview)

Windows (WinGet):

```powershell
winget install --exact --id Microsoft.VisualStudioCode
```

macOS (with Homebrew):

```sh
brew install --cask visual-studio-code
```

Linux: follow the [distribution-specific instructions](https://code.visualstudio.com/docs/setup/linux).

## 2. Install Git

[Download and installation instructions](https://git-scm.com/downloads)

Windows:

```powershell
winget install --exact --id Git.Git
```

macOS (with Homebrew):

```sh
brew install git
```

Linux: use the [Linux installation instructions](https://git-scm.com/download/linux).

## 3. Install PowerShell 7

Installation instructions: [Windows](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows),
[macOS](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-macos),
[Linux](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-linux).

Windows:

```powershell
winget install --exact --id Microsoft.PowerShell
```

macOS (with Homebrew):

```sh
brew install --cask powershell
```

## 4. Install Azure CLI

Installation instructions: [Windows](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows),
[macOS](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-macos),
[Linux](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux).

Windows:

```powershell
winget install --exact --id Microsoft.AzureCLI
```

macOS (with Homebrew):

```sh
brew install azure-cli
```

Restart your terminal after installation. Run the remaining commands in PowerShell 7 (`pwsh`).

## 5. Install the Azure PowerShell module

[Installation instructions](https://learn.microsoft.com/en-us/powershell/azure/install-azure-powershell)

```powershell
Install-Module -Name Az -Repository PSGallery -Scope CurrentUser -ErrorAction Stop
```

Review the PSGallery trust prompt before accepting.

## 6. Install the VS Code extensions

Run these commands, or install through VS Code's Extensions view using the links:

```powershell
code --install-extension ms-vscode.PowerShell
code --install-extension ms-azuretools.vscode-bicep
```

- [PowerShell](https://marketplace.visualstudio.com/items?itemName=ms-vscode.PowerShell)
- [Bicep](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-bicep)

If `code` is unavailable, use the Extensions view. On macOS, you can also run
**Shell Command: Install 'code' command in PATH** from the Command Palette.

## 7. Sign in to GitHub and enable Copilot

Copilot is built into recent VS Code versions. No separate Copilot extension is required.

1. In VS Code, open **Accounts** and select **Sign in with GitHub**.
2. Complete sign-in in your browser using the account with Copilot enabled.
3. Open **Chat** and send a simple `Who are you?` prompt to confirm access.

[VS Code's Copilot setup](https://code.visualstudio.com/docs/setup/copilot)

## 8. Install the Azure CLI-managed Bicep CLI

[Installation instructions](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/install)

```powershell
az bicep install
```
