# General Overview
* After yesterrdays lab this lab was way easier I could use the question to guide me to what the awnser is and read the documentation to find what specific command i needed to preform the task given. Overall I feel good about it and it feels satisfying doing these myself.
# Lab 4

### 1. Display a list of running processes.
**Answer:**  

* Did ```Get-Command -Noun Process``` saw a command named ```Get-Process``` to confirm this was right
  i did ```help git-process```

  <img width="613" height="177" alt="image" src="https://github.com/user-attachments/assets/97c655cf-cceb-4bf0-9242-432fc659ea7b" />

---

### 2. Test the connection to google.com or bing.com without using an external command like ping
**Answer:**  

* This was a reading that I used from the book. ```Test-Connection``` is the command that worked and the Targetname i put in
 ```8.8.8.8``` which is googles ip adress and got a successful response.
  
* <img width="781" height="320" alt="image" src="https://github.com/user-attachments/assets/85a10d34-50c5-4fe7-8fee-0e503fa48999" />
---

### 3. Display a list of all commands that are of the cmdlet type. (This is tricky—we’ve shown you Get-Command, but you need to read the help to find out how to narrow down the list as we’ve asked.

**Answer:**  

* After going into ```Help Get-Command``` I found a parameter named "CommandType" and it read that it returns all
  commands of a specific naming convention such as cmdlets, alias, and others. So the command is ```Get-Command -CommandType cmdlets```
<img width="767" height="320" alt="image" src="https://github.com/user-attachments/assets/f6a95a41-8c28-45e1-9613-95e48ec1ec98" />

---

### 4. Display a list of all aliases
**Answer:**  

* Just tried typing in ```Get-Al``` then pressed tab and got ```Get-Alias``` which displayed all aliases.
<img width="475" height="388" alt="image" src="https://github.com/user-attachments/assets/fd76a0f6-832c-4cdf-a3ff-6fe779e409f6" />
---


### 5. Make a new alias, so you can run ntst to run netstat from aPowerShell prompt.
**Answer:**  

* The first thing did was ```Get-Command -Noun Alias``` which led me into reading the help and getting and exanmple by using ```help New-Alias``` & ```help New-Alias -Example```
 after doing this it brought me to the awnser of ```New-Alias -Name "ntst" netstat```
 
<img width="711" height="507" alt="image" src="https://github.com/user-attachments/assets/14f83096-22ff-400c-bbcf-eb7030538160" />

---

### 6. Display a list of processes that begin with the letter p. Again, read the help for the necessary command—and don’t forget thatthe asterisk (*) is a near-universal wildcard in PowerShell.
**Answer:**  
* I figured that it was most likely ```Get-Process -Name``` then p somewhere. I tried two different variations one with ```*P``` and one with ```p*```
  the first one did not work the second one did work getting me the result of ```Get-Process -Name -p*```.
  
  <img width="617" height="133" alt="image" src="https://github.com/user-attachments/assets/9657af2f-182f-4234-8ec5-6708a980b6aa" />

---

### 7. Make a new folder (aka directory) using the New-Item cmdlet with the name of MyFolder1. Then do it again and call it MyFolder2, put this in the first folder. Use Help if you’re not familiar with New-Item.

**Answer:**  
* I typed in ```help new-item``` For step one after reading i created a foolder using ```New-item -ItemType Directory -Name Myfolder1```
* Then for part 2 after reading more of the help i ended up with this command ```New-Item -Itemtype Directory -Name MyFolder2 -Path MyFolder1```

<img width="382" height="116" alt="image" src="https://github.com/user-attachments/assets/7e134826-308d-4eff-8184-e7df3d7c97e6" />

---

### 8. Remove the folders from step 7 in a single command. Use Get- Command to find a similar cmdlet to what we used in step 7—and don’t forget that the asterisk (*) is a near-universal wildcard in PowerShell
**Answer:**  
* I intially looked up ```Get-Command Item``` and found the command ```Remove--Item``` with this command i typed ```Remove-Item -Path .\MyFolder1\``` and it removed everything.


<img width="672" height="463" alt="image" src="https://github.com/user-attachments/assets/1faee870-7445-4517-b57d-521dd3bcff48" />

---
