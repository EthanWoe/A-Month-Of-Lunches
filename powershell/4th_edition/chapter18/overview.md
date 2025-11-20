# Lab 19
***Disclaimer: could not get it to be able to connect to localhost, so will type commands anyway***

### 1. Close all open sessions in your shell
*ANSWER*
* looked up session `help session` found ```get-pssession``` then ```exit-pssession```
  <img width="340" height="47" alt="image" src="https://github.com/user-attachments/assets/c83669b1-801f-4475-9e66-f033e7cf4658" />

---

### 2. Establish a session to a remote computer. Save the session in a variable named $session.
*AWNSER*
* This starts a localhost instance ```$s = New-Pssession``` 
<img width="342" height="27" alt="image" src="https://github.com/user-attachments/assets/740aa3fe-152c-4fe8-8577-d459059b832c" />

---

### 3. Use the $session variable to establish a one-to-one remote shell session with the remote computer. Display a list of processes and then exit.
*AWNSER*
* ```enter-pssession $session``` then ```gett-process``` then ```exit```

---
### 4. Use the $session variable with Invoke-Command and list the time zone of the remote machine.
*AWNSER*
* using ```help invoke-command -example``` then  ```help time``` i found the command is ```invoke-command -computername localhost server01 -Sriptblock {get-Timezone}

---
### 5. If you are on a Windows client, use Get-PSSession and Invoke-Command to get a list of the 20 most recent security event log entries from the remote computer.
*AWNSER*
* using ```help recent``` i found ```get-eventlog``` which then lead me to ```Invoke-Command -ComputerName localhost Server01 -ScriptBlock {Get-EventLog -newest 20}```

---
### 6. If you are on a macOS or Linux client, count the number of items in the /var directory. Tasks 7–10 can only be performed on a Windows machine.
*AWNSER*
* To do this, you need to ```invoke-command -scriptblock {import-module ServerManager} -Session $session

---
### 7. `Use Invoke-Command and your $session variable to load the ServerManager module on the remote computer`
*AWNSER*
* To then do this, you must do `Import-PSSession -Session $session -Prefix rem -Module ServerManager```

---
### 8.  Run the imported Get-WindowsFeature command'' 
*AWNSER*
* ```Get-RemWindowsFeature```

---
### 9. Close the session that’s in your $session variable.
*AWNSER*
* ```Remove-PSSession -Session $session```

---
