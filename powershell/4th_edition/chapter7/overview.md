# Overview

# Lab 7 

### 1. Browse the PowerShell Gallery. Find a module or two that you think sounds interesting and install it.
*Awnser*
* The one that I chose was Az.Monitor as I expect to be doing work monitoring networks, traffic, devices, or other things similar to that.

---

### 2. Browse the available commands for the module you just downloaded.
*Answer*
* To list all commands of the module, I did ```Get-Command -Module Az.Monitor```
<img width="837" height="516" alt="image" src="https://github.com/user-attachments/assets/131f0cb9-8fe2-45d0-8890-330a094a3372" />

---

### 3. Use the commands from section 7.2 to find and install (if needed) the latest-version module by Microsoft for working with archives that contain the command Compress-Archive.
*Answer*
* It was already installed I checked by doing ```help *-archive```
<img width="836" height="161" alt="image" src="https://github.com/user-attachments/assets/ad5c3752-43ed-4896-8acf-0123c9ed7bbb" />

---

### 4. Import the module you just installed.
*Answer* 
* I assume this was already imported since i did not have to do anything so i decided to still go through it as I'm learning and need all the
  practice that I can get. So I needed to find the module that the command was in using ```Find-Module -command Compress-Archive``` then I did
  ```import-module Microsoft.PowerShell.Active```
  <img width="800" height="68" alt="image" src="https://github.com/user-attachments/assets/d72a10ee-20c4-49bf-858a-d0e6bfe464fb" />
  
---

### 5. Create a Tests folder for the next step with 10 files in it, and name it ~/TestFolder
*Answer*
 This one was actually surprisingly cool. I did it all, making them one at a time, then checked to make sure that's what the lab wanted me to do, and saw
  a cool way to do it would be using ```1..10```. After seeing their example, i could not get it to work, so i changed to up.
 ```1..10 | ForEach-Object { New-Item -Itemtype File -Name $_ - Value $_}```
 <img width="852" height="356" alt="image" src="https://github.com/user-attachments/assets/f585ab00-3730-4aa4-9eb0-ca4b179c053a" />

---

### 6. Use Compress-Archive to create a zip of the contents of/TestFolder, and name the archive TestFolder.zip.
*Answer*
* Initially, I just guessed what the parameters were going to be and tried ```Compress-Archive -Path .\TestFolder\ -Name TestFolder.zip```
 this did not work as ```--Name``` was not a parameter. So I read the documentation and found the right parameters, leading me to the command
 ```Compress-Archive -Path .\TestFolder\ -DestinationPath TestFolder.zip```
<img width="828" height="37" alt="image" src="https://github.com/user-attachments/assets/c9b35666-2c01-4da8-b500-1c946b3de61b" />
<img width="698" height="520" alt="image" src="https://github.com/user-attachments/assets/b3f794cc-bfcb-4ef3-a757-b6fc2520f033" />

---

### 7. Expand the archive to ~/TestFolder2
*Answer*
* Since it was made by the samem people I figured documentation was the same
  when it came to parameters. So I ran ```Expand-Archive .\TestFolder.zip -DesintationPath TestFolder2```
  
<img width="540" height="487" alt="image" src="https://github.com/user-attachments/assets/dfc54acf-17fa-423a-a784-f9b6a2009de4" />

### 8. Use Compare-Object and Select-Object - ExpandProperty Name to compare just the names of the files in the folders to verify you have the same files.
*Awnser*
* This one was extremely frustrating as I was doing the command and nothing was returning when I was entering the command, but it was just because
 i did not have ```-IncludeEqual``` as a parameter :').The command i used to find the difference was ```Compare-Object (Get-ChildItem .\TestFolder\ | Get-Object -ExpandProperty -Name) (Get-ChildItem .\TestFolder2\TestFolder\ | Get-Object -ExpandProperty -Name)```.
  
<img width="867" height="297" alt="image" src="https://github.com/user-attachments/assets/dc20026f-1eba-4863-9667-dc4f132719b5" />





