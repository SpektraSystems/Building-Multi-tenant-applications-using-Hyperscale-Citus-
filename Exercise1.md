# Getting started with Hyperscale (Citus)

In order to use the Azure Portal Cloud Shell we will need to create a storage account. The storage account allows you to save files associated with the Cloud Shell so you may use them in various Azure portal activities like running scripts to manage Azure resources.

## Lab 1: Create a Cloud Shell
1.	 
On the portal banner click on the Cloud Shell icon 
2.	 
On the Welcome to Azure Cloud Shell click Bash
3.	 
On the You have no storage mounted screen click Show advanced settings
4.	 
Use the default values for subscription and region
5.	 
Resource Group should be set to Use existing rg564758
6.	 
For Storage account, select Create new and paste 
sg564758shell 
•  in the field
•   
For File share, select Create new and enter 
sg564758shell 
•  •   
Click Create Storage
Note: This may take up to a minute to create and start the Cloud Shell
•   
We will need the client IP address of Cloud Shell to configure the firewall in the next step. At the command prompt enter the following command and press return then copy or note the IP address of your cloud shell curl -s https://ifconfig.co 
•  Note: To paste in the bash console right click and choose paste.
•   
Click Next on the bottom right of this page
