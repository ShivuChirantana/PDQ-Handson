
# Steps to setup Active Directory in windows server 2022

## Step 1: Launch the Server Manager Program
Launch the Server Manager program, press the Windows Logo Key and search for “Server Manager”. An application should show up on the list. Click on it to launch the program.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/6a145514-dda0-448d-90c1-e511eb6d1221)

 
## Step 2: Set up Add Roles & Features
Look for “Manage” on the top right of the menu bar. Click on it and then select “Add Roles and Features.” A pop-up window will open immediately. This pop-up window is the installer wizard that guides you with the roles and features setup.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/cfa08af9-b8e3-40ee-9e69-6206f90bb979)
 
On the left side of the window, you’ll see a list of all the checkpoints you encounter in this stage. Click “Next”.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/52c0ff76-1ba7-4bfd-82ac-2c423a56c074)

## Step 3: Select Installation Type
At the “Installation Type” checkpoint select “Role-based or feature based installation” radio button and then click “Next”.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/a6ed67d0-007d-4393-999b-db2fa8749df4)
 

## Step 4: Configure your Server Selection and Roles
On the “Server Selection”, select “Select a server from the server pool” radio button. This lists a server installed on your machine. Please, click on the desired server once to select it and click “Next.”

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/32ec7dc2-dfc4-48c2-b06d-23377b31317f)

 
## Step 5:  Add features.
At the “Select Server Roles”, select the role for the server. In the centre of the window, there is a list of all the roles that you can assign to your server machine. Search for “Active Directory Domain Services”. 

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/0ba413ac-b402-4127-9f9c-cbeaef0de53b)

Click on “Add Features”

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/b7a99494-2cca-4eb8-8783-2aed42be0f09)

Make sure “Active Directory Domain Services” is selected. Click “Next”

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/f1af6893-0676-40ac-aef7-732bf682f70a)

 Next simply click “next” without making modifications to any other settings.

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/f319163b-0192-456d-9468-c31ef91eb273)

 You will be redirected to the adding “Active Directory Domain Services” feature once the previous step is complete. On the installer wizard window, click “Next”.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/d6f81734-6cb0-4ce2-808d-1f9f31e54bd7)

## Step 6: Summary and confirmation
You’ll see a summary of your selected options here. Have a look at them carefully, and if you think you’ve made a mistake at any of the earlier checkpoints, you can go back and fix it by clicking “previous.” 

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/1cc900ee-1cd0-4dc6-a13d-1796b348202a)

 
 The wizard will then begin installation. The time of install depends on your machine’s hardware configuration and what features you’ve selected to be installed. Please make sure not to interrupt the installation. Once the installation is complete, click the “Close” button.

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/5773b17e-914f-4769-a944-0cb0a158be58)

 
## Step 7: Promoting Your Server to a Domain Controller
So far, you’ve just added the required feature “Active Directory Domain Services.” The feature “Active Directory Domain Services” you’ve just added needs to be promoted to a DC (Domain Controller). Here are the following steps needed to do so:
1. Relaunch “Server Manager” if you have already closed it. On your Server Manager dashboard, you’ll should see a yellow triangle warning sign on the top right of the window near the menu bar. This sign appears only if Active Directory Domain Services was properly installed.
2. Click on the warning sign and a dropdown list will show you the required actions termed “post-deployment configuration.”
3. Look for the “Promote this server to a domain controller” option and click on it.

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/616b9837-bb37-48a8-9aff-92e322d68467)

## Step 8: Add A Forest
At this checkpoint, a configuration wizard will open on your screen, which will guide you throughout your deployment configuration. The first step of the deployment configuration is to add a new forest.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/a43189e5-34ed-40c6-92bc-09ffed856a2f)

 
## Step 9: Deployment Configuration
At the first checkpoint “Deployment Configuration”, please select the “add a new forest” radio button and enter your root domain name as desired. Then click “next”. (When adding a new forest, you’ll see multiple options. You don’t necessarily have to add a new forest and you choose any option from the given list.)

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/128ac27d-b43b-4012-b4d3-c17858866e11)

 
## Step 10: Setting Domain Controller options.
At the “Domain Controller Options” checkpoint, leave all the settings untouched and enter your password and confirm it. Make sure to keep a note of this password as changing it later on is troublesome.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/f9c0fbb1-4408-46b6-a733-5188971d6ec3)

 
## Step 11: Configuring DNS Options
On the DNS Options page, you will see an error message stating that there’s no parent zone found and no delegation for your DNS server could be created. Ignore this message and click the “next” button, leaving all the settings at this checkpoint unchanged.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/f5f3c69e-e85d-4d8e-9fcb-9f68cbcac688)

 
## Step 12: Configure Additional Options
On the Additional Options page, enter your desired NetBIOS domain name in the given textbox. Click “Next”.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/51d9bc84-99c5-41fd-a337-c5637949733e)

 
## Step 13: Confirm Preselected Paths
 Three or more paths will be listed on your screen. Do not change these paths. You’re not required to keep a note of these paths either. Click “next”.

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/165ae810-c948-4e36-a7b8-c1db789b6606)


## Step 14: Review your Selections.
Whatever options you’ve selected so far will listed on the configuration wizard at this checkpoint. Have a look at them and if needed, move to the previous checkpoints using the “previous” button and make the desired changes. Once you’re satisfied with the selected options, click “next” on the “Review Options”.

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/137fe161-f11e-4087-a93a-0a701fbf03f7)

 
## Step 15: Run Prerequisites Check
 Next, head to the “Prerequisites Check” checkpoint. At this stage you’ll see, if all the prerequisite checks were successfully completed. If not, then a list of errors will be displayed on the window. If there are any errors, you’ll need to go to the stated checkpoint and fix the errors. Once you’ve fixed all the errors, a green check mark with a success message will be displayed. Then click “Install” to begin the installation.

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/e2802077-4eed-4c90-8f8a-31ec6b89905b)

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/f5262cfa-50e9-48fd-9e2c-55d163814cdc)

  
Your server machine will be restarted once to get promoted to Domain Controller.
 
![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/06aa7df6-5920-4ad9-8fe1-76a2fcbb37f3)


## Step 16: Verify Installation by running below PowerShell commands
To verify if the Active Directory installation was successfully completed:

``` 
    Get-Service adws,kdc,netlogon,dns
```

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/2f4c612e-9b46-4141-ade9-738227278172)

 
To get the details of your Domain Controller:

```
    Get-ADDomainController
```

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/463145bc-67e3-4aa5-9f4c-aa70c9a884df)

 
To get the details of your domain, use this command:

```
    Get-ADDomain mylocaldomain.net
```

 ![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/2d59e5dc-d0e9-4e0f-9f5d-ed50c606dfa4)


## Step 17: Join Windows Computer to domain from PowerShell commands

1. Update the DNS entry in this machine is to Domain Controller IP address.  Let the “Obtain an IP address Automatically” be selected.

	```
     Set-DNSClientServerAddress "InterfaceAlias" –ServerAddresses ("preferred-DNS-address", "alternate-DNS-address")
	```

InterfaceAlias  Get from Get-DNSClientServerAddress <br />
Preferred-DNS-Address  IP address of Domain Controller Machine. <br />
Alternate-DNS-address  Leave it blank <br />

2. PowerShell command to Join a windows computer to active directory domain.

   ```
  	Add-Computer -DomainName mylocaldomain.net -restart
   ```

## Step 18: Join RHEL/CentOS/Fedora/Amazon AMI Computer to domain 

1. Update /etc/hosts file with Domain Controller IP address.

2. Make sure the domain controller is accessible from Linux machine using ping command.

3. Install the realmd and  dependency packages.
```
	#sudo yum install sssd realmd oddjob oddjob-mkhomedir adcli samba-common samba-common-tools krb5-workstation openldap-clients policycoreutils-python
```

5.  Execure command to join to domain
```
	#sudo realm join --user=[Domain User Account] [Domain Name]
```

[Domain User Account] : Administrator <br />
[Domain Name] : mylocaldomain.net <br />

Provide Domain Controller Machine Administrator Password when prompted.<br />

## Step 19: Verify Computers are added to Domain controller 
Run the below PowerShell command in Domain Controller Machine

```
	Get-AdComputer -Filter ‘*’
```

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/da65ad05-6d79-4cb9-aef6-5e7b9ee87367)


 

