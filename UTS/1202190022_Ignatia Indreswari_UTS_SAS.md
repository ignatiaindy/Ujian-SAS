# UTS SAS

**Teknologi Informasi [ IT 02-02 ]**

**Ignatia Indreswari  1202190022**

------

## Step by Step

------

First we need to download windows server iso

```
https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022
```

After downloading it, we need to create Windows Server virtual Machine

![01_1](D:\ITTelkom IT\SAS\UTS\assets\01_1.PNG)

![01_2_Windows_Server_VM](D:\ITTelkom IT\SAS\UTS\assets\01_2_Windows_Server_VM.PNG)

After Windows Server VM have been created, then we need to go to storage and add windows server iso

![01_3_Settings](D:\ITTelkom IT\SAS\UTS\assets\01_3_Settings.PNG)

![01_4_Add_ISO](D:\ITTelkom IT\SAS\UTS\assets\01_4_Add_ISO.PNG)

![01_5_ISO_Added](D:\ITTelkom IT\SAS\UTS\assets\01_5_ISO_Added.PNG)

After that, start the VM

![01_6_DiStart](D:\ITTelkom IT\SAS\UTS\assets\01_6_DiStart.PNG)

Click 'Install now' to start installing

![01_7_Install_Now](D:\ITTelkom IT\SAS\UTS\assets\01_7_Install_Now.PNG)

![01_8_OS_Setup](D:\ITTelkom IT\SAS\UTS\assets\01_8_OS_Setup.PNG)

Pick the custom one

![01_9_OS_Setup_Custom](D:\ITTelkom IT\SAS\UTS\assets\01_9_OS_Setup_Custom.PNG)

![01_10_OS_Setup_Unallocated](D:\ITTelkom IT\SAS\UTS\assets\01_10_OS_Setup_Unallocated.PNG)

Microsoft Server Operating System is installing, we just need to wait until it is installed

![01_11_Installing_OS](D:\ITTelkom IT\SAS\UTS\assets\01_11_Installing_OS.PNG)

Set the password to enter your windows server, after it is installed

![01_12_Set_Password](D:\ITTelkom IT\SAS\UTS\assets\01_12_Set_Password.PNG)

To open this lockscreen, we need to go to input, then keyboard, an then click ctrl+alt+del button

![01_13_Lockscreen](D:\ITTelkom IT\SAS\UTS\assets\01_13_Lockscreen.PNG)

It opens up  :)

![01_14_Masuk](D:\ITTelkom IT\SAS\UTS\assets\01_14_Masuk.PNG)

Before we  go on, we need to change the network to Bridge Adapter so that it can connect to the internet

![01_15_Bridge_Adaptor](D:\ITTelkom IT\SAS\UTS\assets\01_15_Bridge_Adaptor.PNG)

After that we need to go to settings, network and internet, network connection, and then properties to set the ip that we want, from DHCP to static

![02_1_Setting_DHCP](D:\ITTelkom IT\SAS\UTS\assets\02_1_Setting_DHCP.PNG)

You can the IP has changed or not from 'cmd', ipconfig. As we can see, the IP has changed

![02_2_cmd_ipconfig](D:\ITTelkom IT\SAS\UTS\assets\02_2_cmd_ipconfig.PNG)

The next step, we need to add roles and features. Just click number 2

![02_3_Server_Manager](D:\ITTelkom IT\SAS\UTS\assets\02_3_Server_Manager.PNG)

In here we just need follow the instruction to install Win Active Directory Domain Services, DNS Servers, and Net Framework 3.5

![02_4_Add_Roles](D:\ITTelkom IT\SAS\UTS\assets\02_4_Add_Roles.PNG)

![02_4_Add_Roles_2](D:\ITTelkom IT\SAS\UTS\assets\02_4_Add_Roles_2.PNG)

![02_4_Add_Roles_Active_Directory](D:\ITTelkom IT\SAS\UTS\assets\02_4_Add_Roles_Active_Directory.PNG)

![02_4_Add_Roles_DNS_Server](D:\ITTelkom IT\SAS\UTS\assets\02_4_Add_Roles_DNS_Server.PNG)

Check the checkbox for Win Active Directory Domain Services and DNS Servers

![02_5_Server_Roles](D:\ITTelkom IT\SAS\UTS\assets\02_5_Server_Roles.PNG)

And then check the checkbox for Net Framework 3.5 Features

![02_5_Features_Net_Framework](D:\ITTelkom IT\SAS\UTS\assets\02_5_Features_Net_Framework.PNG)

After all the steps are completed, we went to Confirmation, but don't click the install button yet. We need to click Specify Alternate Source Path button that will be filled with our path. Go to sources then sxs, we'll see 2 file like in the picture below, then we just need to copy the path

![02_6_Specify](D:\ITTelkom IT\SAS\UTS\assets\02_6_Specify.PNG)

And then paste it here

![02_7_Specify_Input_Path](D:\ITTelkom IT\SAS\UTS\assets\02_7_Specify_Input_Path.PNG)

After that, click 'Install' button, and wait until the installation are finished

![02_8_Confirmation_Install](D:\ITTelkom IT\SAS\UTS\assets\02_8_Confirmation_Install.PNG)

![02_9_Add_Roles_Installing](D:\ITTelkom IT\SAS\UTS\assets\02_9_Add_Roles_Installing.PNG)

Finished!! :)

![02_10_Add_Roles_Installation_Success](D:\ITTelkom IT\SAS\UTS\assets\02_10_Add_Roles_Installation_Success.PNG)

As we can see, it shows the Net Framework 3.5 Features are installed

![02_11_Add_Roles_Installed](D:\ITTelkom IT\SAS\UTS\assets\02_11_Add_Roles_Installed.PNG)

------

Next, we click the flag icon, then we click 'Promote this  server to a domain controller'

![03_1_Post_Deploy_Promote_Server](D:\ITTelkom IT\SAS\UTS\assets\03_1_Post_Deploy_Promote_Server.PNG)

We need to add a new forest, then type 'vm.local'

![03_2_Deploy_Config](D:\ITTelkom IT\SAS\UTS\assets\03_2_Deploy_Config.PNG)

Next step is password setting

![03_3_Domain_Controller_Set_Password](D:\ITTelkom IT\SAS\UTS\assets\03_3_Domain_Controller_Set_Password.PNG)

Then click next  and the install

![03_4_Paths](D:\ITTelkom IT\SAS\UTS\assets\03_4_Paths.PNG)

![03_5_Prerequisites_Check](D:\ITTelkom IT\SAS\UTS\assets\03_5_Prerequisites_Check.PNG)

Installation is started

![03_6_Installing](D:\ITTelkom IT\SAS\UTS\assets\03_6_Installing.PNG)

After the installation is finished, we need to check whether the promote server really installed or not, We need to go to tools, active directory users and computers

![03_7_vmlocal_installed](D:\ITTelkom IT\SAS\UTS\assets\03_7_vmlocal_installed.PNG)

Then we need to go to cmd, and ping vm.local. We did it. 'Promote' is installed successfully!

![03_8_ping_vmlocal](D:\ITTelkom IT\SAS\UTS\assets\03_8_ping_vmlocal.PNG)

------

## Thank You

------

