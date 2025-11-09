# Overview
  * Honestly way harder to do ssh in powerhsell for some reason. i think the way the book wanted to do it was kinda bad considering you  can isntall it thorugh the settings easily and it takes like a billion years for the
    ssh server and client to install.
# Lab 13

### 1. 
*Awnser*
* ```Enter-PSSession -ComputerNam localhost``` then ```notepad```. it will open but we wont see it.

---

### 2. 
*Awnser*
* ```Invoke-Command -ComputerName localhost -ScriptBlock { Get-Process } | Format-Table -AutoSize```


---

### 3. 
*Awnser*
* ```Invoke-Command -ComputerName localhost -ScriptBlock {Get-Process | Sort-Object -Property VM -Descending | Select-Object -First 10}```

---

### 4. 
*Awnser*
* ```Invoke-Command -ComputerName (Get-Content computers.txt) -ScriptBlock {Get-ChildItem ~ | Sort-Object LastWriteTime -Descending | Select-Object -First 10}```



---

### 5. 
*Awnser*
* ```Invoke-Command -ComputerName localhost -ScriptBlock {$PSVersionTable.PSVersion}```

---



---
