# Create a Windows virtual machine in the Azure portal


Azure virtual machines (VMs) can be created through the Azure portal. This method provides a browser-based user interface to create VMs and their associated resources. This quickstart shows you how to use the Azure portal to deploy a virtual machine (VM) in Azure that runs Windows Server 2022 Datacenter. To see your VM in action, you then RDP to the VM and install the IIS web server.

Step one: Sign in to Azure

Step two: Sign in to the Azure portal.

Step three: Create virtual machine

Step four: Enter virtual machines in the search.

Step five: Under Services, select Virtual machines.

Step six: In the Virtual machines page, select Create and then Azure virtual machine. The Create a virtual machine page opens.

Step seven: Under Instance details, enter myVM for the Virtual machine name and choose Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 for the Image. Leave the other defaults.


 

Note: Some users will now see the option to create VMs in multiple zones. To learn more about this new capability, see Create virtual machines in an availability zone. Screenshot showing that you have the option to create virtual machines in multiple availability zones.

Step eight: Under Administrator account, provide a username, such as azureuser and a password. The password must be at least 12 characters long and meet the defined complexity requirements.

Step nine: Under Inbound port rules, choose Allow selected ports and then select RDP (3389) and HTTP (80) from the drop-down.



Step ten: Leave the remaining defaults and then select the Review + create button at the bottom of the page.



Step eleven: After validation runs, select the Create button at the bottom of the page. Screenshot showing that validation has passed. Select the Create button to create the VM.

Step twelve: After deployment is complete, select Go to resource.
