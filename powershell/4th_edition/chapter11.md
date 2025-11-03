# Overview
# Lab 11

### Question 1. Display a table of processes that includes only the process names, IDs, and whether they’re responding to Windows (the Responding property has that information). Have the table take up as little horizontal room as possible, but don’t allow any information to be truncated
*Awnser*
* Using previous commands and piping this one was pretty easy to figure out. ```get-process | Select-Object Name,ID,Responding```
<img width="576" height="177" alt="image" src="https://github.com/user-attachments/assets/86cf826e-8f73-4e13-b2e9-c0a7e49eb68d" />

### Question 2. Display a table of processes that includes the process names and IDs. Also include columns for virtual and physical memory usage, expressing those values in megabytes (MB).
*Awnser*
* I initally found the awnser without converting it to MB's by using ```Get-Process | Select-Object Name,Id,VirtualMemorysize64,WorkingSet64```
  to convert to megabytes i used math ```Get-Process | Select-Object Name, Id,
    @{Name="VirtualMemory(MB)"; Expression = { [math]::Round($_.VirtualMemorySize64 / 1MB, 2) }},
    @{Name="PhysicalMemory(MB)"; Expression = { [math]::Round($_.WorkingSet64 / 1MB, 2) }}```
<img width="891" height="255" alt="image" src="https://github.com/user-attachments/assets/7118f842-add1-4e61-953e-6cb4e307cdee" />


---

### Question 3.  Use Get-Module to get a list of loaded modules. Format the output as a table that includes, in this order, the module name and the version. The column headers must be ModuleName and ModuleVersion.
*Awnser
* Aftwer figuring out question two I also got the same thing but under the wrong names. So i had to create the command
* ```Get-Module | Format-Table @{Name="ModuleName";Expression={$_.Name}}, @{Name="ModuleVersion";Expression={$_.Version}}```
* <img width="866" height="162" alt="image" src="https://github.com/user-attachments/assets/8a73501a-51f9-4ff2-b9ed-b242bba86e20" />


---


### Question 4. Use Get-AzStorageAccount and Get- AzStorageContainer to display all of your storage containers so that a separate table is displayed for storage containers that are accessible to the public and storage containers that are not. (Hint: Piping is your friend . . . use a -GroupBy parameter.)
*Awnser
* I do not have a azure account so this one is difficult for me so i will  just give my best educated guess ```Get-AzStorageAccount | Get-AzStorageContainer | Format-Table -Groupby Public```
  
---


### Question 5. Display a four-column-wide list of all directories in the home directory.
*Awnser
* Looked back at readings and found command to make it wide format ```ls | Format-Wide -col 4```
  <img width="932" height="252" alt="image" src="https://github.com/user-attachments/assets/72081e47-54cf-499d-950b-7ec17e570b9a" />

---


### Question 6. Create a formatted list of all .dll files in $pshome, displaying the  name, version information, and file size. PowerShell uses the Length property, but to make it clearer, your output should
show Size
*Awnser
* ls $pshome | ft Name,VersionInfo,@{Name='Size';Expression{$_.Length}}
<img width="848" height="467" alt="image" src="https://github.com/user-attachments/assets/6b88c35b-3ff3-4f73-a988-8e2e48d663a2" />

---
