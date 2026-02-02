# Create a Linux virtual machine in the Azure portal

Azure virtual machines (VMs) can be created through the Azure portal. The Azure portal is a browser-based user interface to create Azure resources. This quickstart shows you how to use the Azure portal to deploy a Linux virtual machine (VM) running Ubuntu Server 22.04 LTS. To see your VM in action, you also SSH to the VM and install the NGINX web server.

Step one: Create virtual machine

Step two: Enter virtual machines in the search.

Step three: Under Services, select Virtual machines.

Step four: In the Virtual machines page, select Create and then Virtual machine. The Create a virtual machine page opens.

Step five: In the Basics tab, under Project details, make sure the correct subscription is selected and then choose to Create new resource group. Enter myResourceGroup for the name.

Screenshot of the Project details section showing where you select the Azure subscription and the resource group for the virtual machine

Step six: Under Instance details, enter myVM for the Virtual machine name. Under Availability options, select No infrastructure redundancy required. Under Security type, select Standard. Choose Ubuntu Server 22.04 LTS - Gen2 for your Image. Leave the other defaults. The default size and pricing is only shown as an example. Size availability and pricing are dependent on your region and subscription.

Step seven: Under Administrator account, for Authentication type, select SSH public key.

Step eight: In Username enter azureuser.

Step nine: For SSH public key source, leave the default of Generate new key pair, and then enter myKey for the Key pair name.

Screenshot of the Administrator account section where you select an authentication type and provide the administrator credentials

Step ten: Under Inbound port rules > Public inbound ports, choose Allow selected ports and then select SSH (22) and HTTP (80) from the drop-down.


Step eleven: Leave the remaining defaults and then select the Review + create button at the bottom of the page. A final validation runs.

Step twelve: On the Create a virtual machine page, review the details about the VM you're about to create. When you're ready, select Create.

Step thirteen: When the Generate new key pair window opens, select Download private key and create resource. Your key file will be download as myKey.pem. Make sure you know where the .pem file was downloaded; you'll need the path to it in the next step.

Step fourteen: When the deployment is finished, select Go to resource.

Step fifteen: On the page for your new VM, select the public IP address and copy it to your clipboard.
