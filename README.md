## INSTALL THE SNORT PACKAGE
+ Go to "System/Package Manager" (screenshot 1.1)
+ Click on the "Available Packages" tab
+ In the search box, type "snort"
+ Click the install button
+ Click "Confirm"
+ You will see "Success" upon Snort install (screenshot 1.2)

## ASSIGN AN INTERFACE TO SNORT
+ Click on "Services/Snort" (screenshot 2.1)
+ Click "Add"
+ You should be in to "Services/Snort/WAN - Interface Settings" (
+ You can leave all of the settings as is and click "Save"

## CREATE THE CUSTOM DETECT PING RULE
+ Click on the "WAN Rules" tab (screenshot 3.1)
+ In the "Defined Custom Rules" box, enter the following
+ (bold)alert icmp $EXTERNAL_NET any -> any any (msg:"Ping Detected";sid 999000;) (screenshot 3.2)
+ Click "Save"

## START THE SNORT SERVICE
+ Click on the "Snort Interfaces" tab (screenshot 4.1) 
+ Click on the "play" button under the "Snort Status" label (screenshot 4.2)

Once you ping the public IP address of your firewall, you can click on "Services/Snort/Alerts", and see the pings showing up in the logs (screenshot 5.1)
