+++
title = "Installing NS2 on Linux / WSL2"
date = 2024-02-22T18:08:23+05:30
draft = false
tags = ['Linux' ]
+++

# Installing NS2 on Linux / WSL2

Network Simulator 2 (NS2) is a popular tool used for simulating network protocols and scenarios. In this guide, we'll walk through the process of installing NS2 on Ubuntu Linux or Windows Subsystem for Linux 2 (WSL2), along with necessary dependencies and configurations.

## Installing NS2 Dependencies

Before installing NS2, we need to ensure that all necessary dependencies are met.

### Install `nam`

First, let's install `nam`, the Network Animator tool:
 - Download the suitable nam installer from [this link](https://github.com/MJKSabit/ns2-installation). After downloading, run the following command::

```bash
sudo dpkg -i FILE_NAME
```

Replace `FILE_NAME` with the actual name of the downloaded `nam` installer. 
- For example:
If you have downloaded `nam_1.15-10-ubuntu14_amd64.deb`, then the command will be:

```bash
sudo dpkg -i nam_1.15-10-ubuntu14_amd64.deb
```

Navigate to the directory where the installer is located before executing the above command.

### Install `ns2-allinone-2.35`

#### Install `g++-4.8`
```bash
sudo apt-get install g++-4.8
```

If you encounter issues installing `g++-4.8`, you may need to add an older repository and then install it manually:

```bash
echo "deb [trusted=yes] http://th.archive.ubuntu.com/ubuntu bionic main universe" | sudo tee -a /etc/apt/sources.list
sudo apt update
sudo apt install g++-4.8
```

- If there are errors, try:
```bash 
sudo apt --fix-broken install 
```
 and then proceed

#### Install Additional Dependencies

You might encounter errors related to missing dependencies. Install them using:

```bash
sudo apt install libx11-dev xorg-dev
```

### Install NS2

Download the NS2 installer and unzip it:
-  Download the installer from [this link](https://github.com/MJKSabit/ns2-installation).
```bash
tar xvf ns-allinone-2.35_gcc5.tar.gz
cd ns-allinone-2.35/
export CC=gcc-4.8 CXX=g++-4.8 && ./install
cd ns-2.35/
sudo make install
```

After successful installation, you should be able to execute `ns` in the terminal.

### Optional: Install Build Tools

If you're using Ubuntu, it's recommended to install essential build tools( if make files are missing ):

```bash
sudo apt update
sudo apt install build-essential
```

## Post-Installation Configuration

### Cleanup (Optional)

To remove the older repository link from your system:

```bash
sudo sed -i '$ d' /etc/apt/sources.list
```

## Setting up GUI Support in WSL2 (Optional)

If you're using WSL2 and need GUI support, follow these steps:

### GWSL Setup

1. Download GWSL from [this link](https://github.com/MJKSabit/ns2-installation) from their official github repository.
2. Install GWSL and run it.
3. Allow GWSL through the Windows Firewall.
4. Enable Display / Audio Auto Exporting.

## Conclusion

You've successfully installed NS2 on your Linux system or WSL2. With NS2, you can simulate various network scenarios and protocols for research or educational purposes. If you encounter any issues during the installation process, feel free to ask for further assistance.

Happy networking! 🌐