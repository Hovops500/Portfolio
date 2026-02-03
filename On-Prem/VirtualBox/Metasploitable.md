# Installing Metasploitable in VirtualBox

Metasploitable is an intentionally vulnerable Linux virtual machine designed for penetration testing and security training. Below are the steps to set it up in VirtualBox.

<b>Step 1:</b> Download Metasploitable

Visit the Metasploitable project page and download the latest ZIP file containing the .vmdk (virtual hard disk) file.

<b>Step 2:</b>Extract the ZIP File

Use tools like WinRAR or any unzip utility to extract the downloaded ZIP file. This will provide a .vmdk file.

<b>Step 3:</b> Create a New Virtual Machine

Open VirtualBox and click on New to create a new virtual machine.

Provide the following details: Name: Any name of your choice (e.g., Metasploitable). Type: Linux. Version: Other (64-bit).

Allocate at least 512 MB of RAM (recommended).

<b>Step 4:</b> Attach the Virtual Hard Disk

In the hard disk section, select Use an existing virtual hard disk file.

Browse to the extracted .vmdk file and select it.

Click Create to finalize the VM setup.

<b>Step 5:</b> Start the Virtual Machine

Select your newly created VM and click Start.

Once booted, log in using the default credentials: Username: msfadmin Password: msfadmin

