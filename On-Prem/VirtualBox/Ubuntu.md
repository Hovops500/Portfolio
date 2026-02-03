# Installing Ubuntu in VirtualBox

Running Ubuntu inside VirtualBox allows you to explore Linux without altering your main operating system. This setup is ideal for testing, development, or learning in a safe environment.

Download Required Software

<b>VirtualBox:</b> Get the latest version from the official VirtualBox website and install it on your host OS (Windows, macOS, or Linux) .

<b>Ubuntu ISO:</b> Download the latest LTS version from the Ubuntu website for stability .

Create a New Virtual Machine

Launch VirtualBox and click New.

<b>Name & Type:</b> Enter a name (e.g., "Ubuntu VM"), select Linux as type, and Ubuntu (64-bit) as version.

<b>Allocate RAM:</b> Minimum 2 GB (2048 MB), preferably 4 GB for smoother performance.

<b>Create Virtual Hard Disk:</b> Type: VDI (VirtualBox Disk Image) Storage: Dynamically allocated Size: At least 25 GB ^2^.

## Configure VM Settings

<b>System:</b> Uncheck Floppy in boot order, allocate 2 CPUs if possible.

<b>Display:</b> Set Video Memory to 128 MB.

<b>Storage:</b> Attach the downloaded Ubuntu ISO to the optical drive .


## Start the VM and choose Install Ubuntu.

Select language, keyboard layout, and installation type (Normal Installation recommended).

Proceed with default partitioning (safe inside VM).

Set username and password, then wait for installation to complete.

Reboot when prompted.

Post-Installation Enhancements

## Install Guest Additions for better resolution and shared clipboard:

sudo apt update && sudo apt upgrade

sudo apt install build-essential dkms linux-headers-$(uname -r)

sudo ./VBoxLinuxAdditions.run

sudo reboot

### Enable shared folders via VirtualBox settings for file exchange between host and VM.
