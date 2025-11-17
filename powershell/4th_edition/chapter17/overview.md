# Lab 17

### 1. Use Write-Output to display the result of 100 multiplied by 10
*awnser*
* This was easier than I thought it's just basic math expressions ```write-output (100*10)```
<img width="373" height="45" alt="image" src="https://github.com/user-attachments/assets/7aafd49e-95fc-4ac7-b3b7-e9f15009ca89" />

---

### 2. Use Write-Host to display the result of 100 multiplied by 10
*awnser*
* Same here ```write-host (100*10```
<img width="342" height="53" alt="image" src="https://github.com/user-attachments/assets/5e701c7a-1f2b-41dd-9360-902a146deacd" />

---

### 3. Prompt the user to enter a name, and then display that name in yellow text
*awnser*
* This one I was stuck on for a bit because I kept trying to do it in one command. I was doing ```name = read-host "name" | write-host $name -ForegroundColor yellow```
unfortauntly since you cannot have a read and write in the same pipeline, i could not do this. So I just separated them into ```$name = read-host "name"``` and ```write-host $name -Foregroundcolor yellow```
<img width="568" height="78" alt="image" src="https://github.com/user-attachments/assets/286ae569-b2bf-41e0-b87e-2009c1c8d962" />


---

### 4. Prompt the user to enter a name, and then display that name only if it’s longer than five characters. Do this all with a single PowerShell expression—don’t use a variable
*awnser*
* For this one i initially did ```$name = read-host "name" | where-object $name {$_length -gt 5}``` which was wrong, the right one is ```$name = read-host "name" | where {$_.length -gt 5}```
<img width="562" height="90" alt="image" src="https://github.com/user-attachments/assets/ad0cc4c9-35a6-4b3c-85c5-7cc0bac117c1" />


---
