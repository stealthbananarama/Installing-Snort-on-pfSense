## INSTALL THE SNORT PACKAGE
+ Go to "System/Package Manager" ![file](assets/1.1.png) 
+ Click on the "Available Packages" tab
+ In the search box, type "snort"
+ Click the install button
+ Click "Confirm"
+ You will see "Success" upon Snort install ![file](assets/1.2.png) 

## ASSIGN AN INTERFACE TO SNORT
+ Click on "Services/Snort" ![file](assets/2.1.png) 
+ Click "Add"
+ You should be in to "Services/Snort/WAN - Interface Settings" 
+ You can leave all of the settings as is and click "Save"

## CREATE THE CUSTOM DETECT PING RULE
+ Click on the "WAN Rules" tab ![file](assets/3.1.png)
+ In the "Defined Custom Rules" box, enter the following
+ **alert icmp $EXTERNAL_NET any -> any any (msg:"Ping Detected";sid 999000;) ** ![file](assets/3.2.png)
+ Click "Save"

## START THE SNORT SERVICE
+ Click on the "Snort Interfaces" tab ![file](assets/4.1.png)
+ Click on the "play" button under the "Snort Status" label ![file](assets/4.2.png) 

Once you ping the public IP address of your firewall, you can click on "Services/Snort/Alerts", and see the pings showing up in the logs ![file](assets/5.1.png) 
