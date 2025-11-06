# Overview
# Lab 12

### 1. Get the commands from the PSReadLine module
*Awnser*
* Using a previous command i got ```get-command -Module (Get-module -ListAvailable -Name PSReadLine)```
 <img width="782" height="202" alt="image" src="https://github.com/user-attachments/assets/66fa220e-b7a9-464f-874d-84258c471a23" />

 ---

 ### 2. Get the commands using the verb Get from the PSReadLine module.
*Awnser*
* Similiar to before and using previous knowlege ```get-command -Module PSReadLine -name Get*```
<img width="873" height="116" alt="image" src="https://github.com/user-attachments/assets/fae7bd43-fba1-451e-b02e-03c533360215" />

 ---

 ### 3. Display all files under /usr/bin that are larger than 5 MB
*Awnser*
* Do not have usr folder but this is what it would look like ```get-childitem C:\Users/ethan | Where-Object
{$_.length –gt 5MB}```
 ---

 ### 4. Find all modules on the PowerShell Gallery that start with PS and the author starts with Microsoft.
*Awnser*
* Using previous commands and the chapter i got ```Find-Module -name PS* | where-object {$_.Author -like Microsoft}
<img width="877" height="323" alt="image" src="https://github.com/user-attachments/assets/b651b4d1-8696-4ade-b7a9-5396b8e9a0f2" />

 ---

 ### 5. Get the files in the current directory where the LastWriteTime is in the last week. (Hint: (Get- Date).AddDays(-7) will give you the date from a week ago.)
*Awnser*
* This one was a bit harder. I started off with ```get-childitem | get-date``` which got me the date of all the previous files but nothing else importat. I tried reading get-dates help but it did not show anyhting imporatnt.
* I then assumed it was something under where-object and looked through help to see last write time which got me ```get-childitem C:\Users/ethan | where-object LastWriteTime -ge (get-date).AddDays(-7)```
<img width="868" height="165" alt="image" src="https://github.com/user-attachments/assets/c9cd817b-8033-45e1-8040-4d7684e89d76" />

 ---

 ### 6. Display a list of all processes running with either the name pwsh or the name bash.
*Awnser*
* This one felt kind of like a trick question because we were doing all this stuff with name in the chapter but the awnser is truly ```get-process -name pwsh,bash```
<img width="865" height="132" alt="image" src="https://github.com/user-attachments/assets/1cd33201-e428-42bf-b56e-8d18e12069f0" />

 ---
