# Kali Linux VM Installtion

Installing Kali Linux on VirtualBox is a straightforward process that allows you to run Kali in a virtualized environment. Follow these steps to set it up:

<b> Step 1:</b> Download Required Files

Download and install the latest version of VirtualBox from the official website.

Download the Kali Linux ISO file from the Kali Linux website.

<b> Step 2:</b> Create a New Virtual Machine

Open VirtualBox and click New.

Enter a name (e.g., "Kali Linux 2025"), set the type to Linux, and version to Debian (64-bit).

Allocate at least 2GB of RAM (2048 MB) or more for better performance.

Select Create a virtual hard disk now and choose VDI (VirtualBox Disk Image).

Set the storage type to Dynamically allocated and allocate at least 80GB of disk space.

<b> Step 3:</b> Configure the Virtual Machine

Go to Settings for the newly created VM: In General > Advanced, enable Shared Clipboard and Drag’n’Drop as bidirectional. In System > Motherboard, set the boot order to prioritize Hard Disk over Optical Disk. In System > Processor, allocate at least 2 processors and enable PAE/NX. In Display > Screen, set video memory to 128 MB and disable 3D acceleration.

Under Storage, attach the downloaded Kali ISO as a virtual optical disk.

<b> Step 4:</b> Install Kali Linux

Start the VM and select the attached ISO as the startup disk.

Follow the on-screen installation wizard: Choose graphical installation. Configure language, keyboard, and network settings. Partition the virtual disk (use guided partitioning for simplicity).

Complete the installation, reboot, and remove the ISO when prompted.

<b> Step 5:</b> Post-Installation Setup

During installation, VirtualBox Guest Additions may be automatically installed for better performance. If not, install them manually using:

sudo apt update
sudo apt install virtualbox-guest-x11
Copy
Your Kali Linux VM is now ready to use!
