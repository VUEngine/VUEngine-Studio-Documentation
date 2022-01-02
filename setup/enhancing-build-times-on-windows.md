---
layout: documentation
title: Enhancing build times on Windows
---

If you're running Windows 10 or upwards, you can greatly enhance build times by using the Windows Subsystem for Linux (WSL).

1. Open PowerShell as Administrator and run the following command to Ubuntu in WSL 1. Note that WSL 1 is recommended over WSL 2 for much faster file access.

        wsl --set-default-version 1
        wsl --install --distribution=Ubuntu

2. When installation is complete, your newly installed Linux distro is being launched. Follow the on-screen instructions to create a new user.

3. Update the distro: 

        sudo apt update && sudo apt upgrade

4. Install required libraries: 

        sudo apt install make libmpfr-dev libmpc-dev

5. VUEngine Studio automatically detects WSL when it installed. You might have to restart it to pick up the change if you just installed WSL.