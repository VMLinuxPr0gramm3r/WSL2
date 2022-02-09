# Installation instructions:

    1. Enable the windows subsystem for linux featue.
    Open powershell as administrator and run the following command:
    $ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    * This can also be done by using a GUI.
    * In the search bar type turn windows features on or off and then click "run and administrator".
    * Then scroll down to where it says 'Windows Subsystem for Linux', click the check box.
    * Then in the same way enable the Virtual Machine Feature and reboot.
    
    ![image](https://user-images.githubusercontent.com/99178290/153110730-bfe4de01-2ed7-4c05-83cd-2c669ae43ea6.png)
    
     After running this command, restart your computer.

    2. Enable the Vitual Machine Feature
    Open powershell as administrator and run the following command:
    $ dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

    After running this command, restart your computer again.

    3. Download and install the Linux kernel update package.
    Go to the following link:
    https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
    
    ! If you dont find it the file is in this repository.

    It will automatically download the package.
    To install the Linux kernel update package open your downloads folder and look for the "wsl update" package. Right click on it and select run as administrator.
    It will take some time to install.

    4. Set WSL2 as your defualt version.
    To do this run the following command in powershell:
    $ wsl --set-default-version 2

    5. Open Microsoft store and search for linux, choose yourr favorite distro and install it.

    6. Confirm if the distro is running wsl2.
    Run the following command in powershell/cmd:
    $ wsl --list --verbose
