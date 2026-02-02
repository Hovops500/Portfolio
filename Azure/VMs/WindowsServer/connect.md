# Connect to virtual machine

Create a remote desktop connection to the virtual machine. These directions tell you how to connect to your VM from a Windows computer. On a Mac, you need an RDP client such as this Remote Desktop Client from the Mac App Store.

<b>Step 1:</b> On the overview page for your virtual machine, select the Connect > RDP.

Screenshot of the virtual machine overview page showing the location of the connect button.

<b>Step 2:</b> In the Connect with RDP tab, keep the default options to connect by IP address, over port 3389, and click Download RDP file.

<b>Step 3:</b> Open the downloaded RDP file and click Connect when prompted.

<b>Step 4:</b> In the Windows Security window, select More choices and then Use a different account. Type the username as localhost\username, enter the password you created for the virtual machine, and then click OK.

<b>Step 5:</b> You may receive a certificate warning during the sign-in process. Click Yes or Continue to create the connection.

# Install web server
To see your VM in action, install the IIS web server. Open a PowerShell prompt on the VM and run the following command:

## PowerShell
Install-WindowsFeature -name Web-Server -IncludeManagementTools
When done, close the RDP connection to the VM.

# View the IIS welcome page
In the portal, select the VM and in the overview of the VM, hover over the IP address to show Copy to clipboard. Copy the IP address and paste it into a browser tab. The default IIS welcome page will open, and should look like this:

Screenshot of the IIS default site in a browser
