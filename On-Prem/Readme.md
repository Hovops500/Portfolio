# Installing Virtualbox

Installing software in a VirtualBox virtual machine (VM) involves transferring the software to the VM and running its installer. Below are the steps to achieve this effectively.

# 1. Use ISO Files

If the software is available as an ISO file: Open VirtualBox and start your VM. Go to the Devices menu in the VM window. Select Optical Drives > Choose a disk file, then browse to the ISO file. The ISO will mount as a virtual CD/DVD drive in the guest OS. Open the drive in the guest OS and run the installer.

# 2. Shared Folders

To transfer files from your host system: Install Guest Additions in your VM by selecting Devices > Insert Guest Additions CD Image. Enable shared folders: Go to Settings > Shared Folders in VirtualBox. Add a folder from your host system and set it as "Auto-mount." Access the shared folder in your guest OS (e.g., under \\VBOXSVR for Windows).

# 3. USB Drives

If the software is on a USB drive: Plug the USB into your host machine. In VirtualBox, go to Devices > USB and select your USB device. The USB will appear in the guest OS, allowing you to access and install the software.

4. Network Downloads

If the software is downloadable: Use the browser in your guest OS to download and install it directly.

5. Drag and Drop

Enable drag-and-drop functionality: Go to Settings > General > Advanced and set Drag’n’Drop to "Bidirectional." Drag files from your host system into the VM window.
