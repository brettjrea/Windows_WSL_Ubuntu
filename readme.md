#### Title: "Node.js and Build Tools Installation Guide with Optional OS Upgrades"

  <details>
  <summary>1. Get Debian/Ubuntu:</summary>
  
  1. [Install WSL Debian on Windows](https://github.com/brettjrea/Windows_WSL_Debian)
  
  2. [Install WSL Ubuntu on Windows](https://github.com/brettjrea/Windows_WSL_Ubuntu)
  
  3. [Install VSCode with Remote Pack on Windows](https://github.com/brettjrea/Windows_VSC_Remote_Pack)
  
  </details>

  <details>
  <summary>2. Optional OS upgrades:</summary>
  
  1. [Upgrade Debian Bullseye to Buster](https://github.com/brettjrea/Debian_Bullseye_Upgrade_Script)
  
  2. [Upgrade Ubuntu Focal to Jammy](https://github.com/brettjrea/Ubuntu_Jammy_Upgrade_Script)
  
  </details>
  
  <details>
  <summary>3. Node.js tools:</summary>
  
  1. [Install NVM](https://github.com/brettjrea/Debian_Install_NVM) - Node Version Manager
  
  2. [Install NVS](https://github.com/brettjrea/Debian_Install_NVS) - Node Version Switcher (added 02/23 it is a cross-platform node based successor/replacement for NVM)
  
  </details>
  
  <details>     
  <summary>4. Build tools:</summary>       
  
  1. [Install common build tools.](https://github.com/brettjrea/Debian_Install_Common_Build_Tools)
  
  </details>
  
  <details>   
  <summary>5. Add a Backend:</summary> 
  
  1. [Install Strapi.io backend](https://github.com/brettjrea/Debian_Strapi_Backend_API)
  
  </details>
  
  <details>   
  <summary>6. Add a Frontend:</summary> 
  
  1. [Install Gatsby frontend](https://github.com/brettjrea/Debian_Gatsby_Frontend_Client)
  
  </details>
  
  <details>   
  <summary>7. Configure Process Manager:</summary> 
  
  1. [Configure PM2 Process Manager](https://github.com/brettjrea/Debian_Configure_PM2)
  
  </details>
  
  <details>   
  <summary>8. Add GitHub CLI:</summary> 
  
  1. [Install GitHub CLI](https://github.com/brettjrea/Debian_Install_GitHub_CLI)
  
  </details>
  
  
---
```
# Step 1: Open Windows Powershell from powerusers menu
Start-Process powershell -Verb runAs

# Step 2: Enable Windows Optional Feature Microsoft-Windows-Subsystem-Linux
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Write-Host "Windows Optional Feature Microsoft-Windows-Subsystem-Linux is enabled."

# Enable Hyper-V
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
wsl --set-default-version 2
Invoke-WebRequest -Uri https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi -OutFile wsl_update_x64.msi -UseBasicParsing
.\wsl_update_x64.msi

# Step 3: Download Ubuntu
Invoke-WebRequest -Uri https://aka.ms/wslubuntu -OutFile Ubuntu.appx -UseBasicParsing
Write-Host "Ubuntu is downloaded."

# Step 4: Add Ubuntu package
Add-AppxPackage .\Ubuntu.appx
Write-Host "Ubuntu package is added."

# Step 5: Update WSL
wsl --update

# Step 6: Start Debian
ubuntu
```
