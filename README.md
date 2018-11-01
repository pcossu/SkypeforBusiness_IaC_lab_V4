# Azure SkypeforBusiness IaC Lab V4

This Lab refers to an automated installation of Skyper for Business Server 2015 with the paradigm of the IAC - Infrastructure as Code.

I did not do anything, all the thanks are for Imad Benbouzid who has made this lab available to everyone.

I just tried to deploy it but I got the error "Can not install KB2982006 - This update is not applicable to your computer."

I therefore modified a couple of lines of code by applying the workaround described in this link https://blogs.technet.microsoft.com/uclobby/2017/09/05/sfb-server-cannot-install-kb2982006-this-update-is-not-applicable-to-your-computer

These are the logs before fixing with some errors. https://github.com/pcossu/SkypeforBusiness_IaC_lab_V4/blob/master/issuelogs/Logs-Deploy-failed.zip
----------------------------------------------------------------------
SqlConnectionFailure: Failed to connect to SQL Server
SqlConnectionFailure: Failed to connect to the SQL server VM-SFB-FE01.skypefb.com\lynclocal. 	 
SqlConnectionFailureResolution: Make sure that SQL Server is running and you have enough rights to connect to the server.
----------------------------------------------------------------------

These are the logs after fixing, deploy was succesfull. https://github.com/pcossu/SkypeforBusiness_IaC_lab_V4/blob/master/issuelogs/Logs-Deploy-successful.zip

The tests seem to have been successful and so I have made available to those who need it.

You can find the original version in this link
https://github.com/ibenbouzid/SkypeforBusiness_lab_V3

=========================================================================


Azure template for Skype for Business lab deployment with Edge server, ADFS and Freeswitch PSTN Gateway. It creates an On-prem Skype for Business 2015 deployment ready to integrate with Cloud PBX

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpcossu%2FSkypeforBusiness_IaC_lab_V4%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> </a>

## Virtual Lab Topology

The intent of version V3 is to enable deployment of Office 365 CloudPBX with On-premise PSTN Connectivity Via On-Prem Skype for Business deployment. It includes folowing components:
