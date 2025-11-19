# Lab 19
***Disclaimer could not get it to be able to connect to localhost so will type commands anyway***

### 1. Close all open sessions in your shell
*ANSWER*
* looked up session `help session` found ```get-pssession``` then ```exit-pssession```
  <img width="340" height="47" alt="image" src="https://github.com/user-attachments/assets/c83669b1-801f-4475-9e66-f033e7cf4658" />

---

### 2.
*AWNSER*
* This starts a localhost instance ```$s = New-Pssession``` 
<img width="342" height="27" alt="image" src="https://github.com/user-attachments/assets/740aa3fe-152c-4fe8-8577-d459059b832c" />

---

### 3.
*AWNSER*
* ```enter-pssession $session``` then ```gett-process``` then ```exit```

---
### 2.
*AWNSER*
* using ```help invoke-command -example``` then  ```help time``` i found the command is ```invoke-command -computername localhost server01 -Sriptblock {get-Timezone}

---
### 2.
*AWNSER*
* using ```help recent``` i found ```get-eventlog``` which then lead me to ```Invoke-Command -ComputerName localhost Server01 -ScriptBlock {Get-EventLog -newest 20}```

---
### 2.
*AWNSER*
*

---
### 2.
*AWNSER*
*

---
### 2.
*AWNSER*
*

---
### 2.
*AWNSER*
*

---
### 2.
*AWNSER*
*

---
