# AD Part  From  Practical Ethical Hacking by TCM
------------------------------------------------------------------------
### Lab setup 
##### Server Part

Donwload and Install the **Microsoft Server 2019 Standard Evaluation** in Virtual Environment.

Donwload link : [Microsoft Server 2019 ISO](https://www.microsoft.com/en-in/evalcenter/download-windows-server-2019)

![[Screenshot 2022-06-15 at 10.09.00 AM.png]]

**Installation Table**

| Name        | Value           |
| ------------- |:-------------:| 
| RAM     | 2GB Min |
| Storage      | 60GB Min      |  
| Network | NAT      |  
| Password | 123.com@#     |  


Setup Server Machine

`note :After the installation of machine Install vmware tools for better environment (full screen shared clipboard..) in vmware / Guest addition CD image in virtual box`

Steps: 
 
Step 01 : Strat run using `Windows key + R` -> Type `sysdm.cpl` -> Hit `Enter`
Step 02 : Click `Change`

![[Screenshot 2022-06-15 at 10.57.56 AM.png]]

Step 03 : Put a new name `HYDRA-DC` -> `Apply` -> `Close` -> Auto reboot

After that install ADDS.

Steps : 

Step 01 : Got `Server Manager\Dashboard`
Step 02 : Click `Add roles and features` -> `Next`
Step 03 : `Role-based or feature-based installation` -> `Next`
Step 04 : Select Our Server `HYDRA-DC` -> `Next`
Step 05 : Tick `Active Directory Domain Service` -> `Next`
Step 06  : `Add features` -> `Next` -> `Next` -> `Next` -> `Install`
Step 07 : After fully install click `CLose`

After this installtions ADDS have a post deployment configuration 

Steps : 

![[Screenshot 2022-06-15 at 10.32.45 AM.png]]

Step 01 : Click `Promote this server to a domain controller`
Step 02 : Selecr `Add a new forest` -> Root Doamin : `MARVEL.local` (your domain) -> `Next`
Step 03 : Then setup a password for  `DSRM`

**Updated Password Table**

| Username        | Password           |
| ------------- |:-------------:| 
| Administrator     |123.com@# | 
| DSRM Password (Not a username)      | 123.com@#     |  

Step 04 : Then just Click on `Next` -> Wait and `Next` -> Wait and  `Next` -> `Install` Wait for auto reboot

##### Client Part

Donwload and Install the ** Windows 10 Enterprise ** in Virtual Environment.

Donwload link : [Microsoft Server 2019 ISO 64 Bit](https://www.microsoft.com/en-in/evalcenter/download-windows-10-enterprise)

![[Screenshot 2022-06-15 at 11.53.53 AM.png]]

`note : install windows 10 Enterprise`

**Installation Table**

| Name        | Value           |
| ------------- |:-------------:| 
| RAM     | 2GB Min |
| Storage      | 60GB Min      |  
| Network | NAT      |  
| Username | Frank Castle      |  
| Password | Password1    |  

Setup Client Machine

`note :After the installation of machine Install vmware tools for better environment (full screen shared clipboard..) in vmware / Guest addition CD image in virtual box`

Steps: 
 
Step 01 : Strat run using `Windows key + R` -> Type `sysdm.cpl` -> Hit `Enter`
Step 02 : Click `Change`
Step 03 : Put a new name `THEPUNISHER` -> `Apply` -> `Close` -> Auto reboot

After that i cloned the same Client Machine and changes Clinet Machine name to `STARKLAB` and Username : `Peter Parker` Password : `Password1`


Final Resutl we have `One Server : HYDRA-DC (Domain controler)` and `Two Client Machine Win10 64 Bit : THEPUNISHER & STARKLAB`

**Updated Password Table**

| Usernames        | Passwords           |
| ------------- |:-------------:| 
|Server Details                      |
| Administrator     |123.com@# | 
| DSRM Password (Not a username)      | 123.com@#     |  
|Client Details                      |
|Frank Catle      | Password1     |  




----------------------------------- End of Lab Setup -----------------------------------

![[Pasted image 20220617101545.png]]