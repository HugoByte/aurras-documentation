# Windows

### Prerequisites

1. Install Windows Subsystem for Linux with WSL 2 Enabled.

### Installation Guide

1. Navigate to [https://hub.docker.com/editions/community/docker-ce-desktop-windows/](https://hub.docker.com/editions/community/docker-ce-desktop-windows/)
2. Click Get Docker Button and download docker for desktop
3. When prompted, ensure the Enable Hyper-V Windows Features option is selected on the Configuration page.
4. Follow the usual installation instructions to install Docker Desktop.
5. If your admin account is different from your user account, you must add the user to the docker-users group. Run Computer Management as an administrator and navigate to  Local Users and Groups &gt; Groups &gt; docker-users. Right-click to add the user to the group. Log out and log back in for the changes to take effect.
6. Start Docker Desktop from the Windows Start menu.
7. From the Docker menu, select Settings &gt; General.
8. Enable Use WSL 2 Based Engine Option.

Reference: 

* [https://docs.microsoft.com/en-us/windows/wsl/install-win10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* [https://docs.docker.com/docker-for-windows/install/](https://docs.docker.com/docker-for-windows/install/)



