# Create a Linux virtual machine in the Azure portal

Azure virtual machines (VMs) can be created through the Azure portal. The Azure portal is a browser-based user interface to create Azure resources. This quickstart shows you how to use the Azure portal to deploy a Linux virtual machine (VM) running Ubuntu Server 22.04 LTS. To see your VM in action, you also SSH to the VM and install the NGINX web server.

## Create virtual machine

<b>Step 1:</b> Enter virtual machines in the search.

<b>Step 2:</b> Under Services, select Virtual machines.

<b>Step 3:</b> In the Virtual machines page, select Create and then Virtual machine. The Create a virtual machine page opens.

<img src ="images/project-details.png">

<b>Step 4:</b> In the Basics tab, under Project details, make sure the correct subscription is selected and then choose to Create new resource group. Enter myResourceGroup for the name.

<img src ="images/instance-details.png">



<b>Step 5:</b> Under Instance details, enter myVM for the Virtual machine name. Under Availability options, select No infrastructure redundancy required. Under Security type, select Standard. Choose Ubuntu Server 22.04 LTS - Gen2 for your Image. Leave the other defaults. The default size and pricing is only shown as an example. Size availability and pricing are dependent on your region and subscription.

<b>Step 6:</b> Under Administrator account, for Authentication type, select SSH public key.

<b>Step 7:</b> In Username enter azureuser.

<img src ="images/administrator-account.png">

<b>Step 8:</b> For SSH public key source, leave the default of Generate new key pair, and then enter myKey for the Key pair name.

<img src ="images/inbound-port-rules.png">

<b>Step 9:</b> Under Inbound port rules > Public inbound ports, choose Allow selected ports and then select SSH (22) and HTTP (80) from the drop-down.


<b>Step 10:</b> Leave the remaining defaults and then select the Review + create button at the bottom of the page. A final validation runs.

<b>Step 11:</b> On the Create a virtual machine page, review the details about the VM you're about to create. When you're ready, select Create.

<b>Step 12:</b> When the Generate new key pair window opens, select Download private key and create resource. Your key file will be download as myKey.pem. Make sure you know where the .pem file was downloaded; you'll need the path to it in the next step.

<b>Step 13:</b> When the deployment is finished, select Go to resource.

<img src ="images/ip-address.png">

<b>Step 14:</b> On the page for your new VM, select the public IP address and copy it to your clipboard.
