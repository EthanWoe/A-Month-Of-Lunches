# Lab 15

### 1. What method of a DirectoryInfo object (produced by Get-ChildItem) will delete the directory?
*AWNSER* 
* For this i went to ```Get-ChildItem | Get-Member -MemberType Method``` This produced a bunch of methods and i found the delete method
<img width="667" height="485" alt="image" src="https://github.com/user-attachments/assets/d5123aa1-19c9-442e-9381-c2bb9709dbde" />


---

### 2. What method of a Process object (produced by Get-Process) would terminate a given process?
*AWNSER* 
* Similiar to the last except i used ```get-prcoess | get-member -membertype Method``` which produced the kill method to terminate the process
<img width="681" height="461" alt="image" src="https://github.com/user-attachments/assets/94765f3b-4522-4031-8d1e-879d947b5a69" />

---

### 3.Write three commands that could be used to delete all files and directories that have deleteme in the name, assuming that multiple files and directories have this in the name
*AWNSER* 
*I did ```help remove``` which gave me remove-item which then lead me to doing  ```Get-ChildItem *deleteme* | Remove-item -recursive -force``` this is similiar to linux as to recursivly remove something its ```rm -rf```

---

### 4. Assume you have a text list of computer names but want to display them in all uppercase. What PowerShell expression could you use?
*AWNSER* 
* It would be ```get-content (file) | foreach {$_ToUpper() }```

---
