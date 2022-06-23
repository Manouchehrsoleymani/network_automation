# network_automation
discover network devices and get information to add in a NetBox(Source of  truth)

this is a free app and if you use it and get any issue let me know to fix it or help you to customize it for your environment.
please feel free and contact me (Manoochehr.solamani@gmail.com)

There is a pattern for Device's name like this:
DeviceRole+_+Rack+_+DCName
This pattern can be in order too.

If your Netbox is empty and you need to fill it completely, you have to add some information in both .env and inventory files. they will explain below.
- In ".env" file :
--  you must add your default environment variable like user_name, password, Netbox token, Netbox URL, etc.
--  there are some other environment variable too such as "INVENTORY_GROUP_NAME" that it tells the app to whish group of devices in "inventory" discover and add to Netbox. 
- In "inventory" file:
--  you must add your hostname and their ipaddress and groups of inventories.
--  there are some other groups in inventory file like "DC" and "Device_Role" group that if your Netbox is empty you can add this information to prepare requirement to add your network devices.

=======================================================================================================================================================
I use both SwagerAPI and pynetbox package to get information from netbox and post the device's information to it.
if you want to add duplicated device or other modules like site,Device_Role, Device_type, Interfaces, Rack and etc, application ignore them and just update device with new information. and if it doesn't found each inventory then will be added  in Netbox

This app dicover all interfaces and Ip addresses from Cisco devices and add them to  Netbox Automatically.

i'm going to added other module like vlan and interfaces's information like Dot1Q information to it too.

