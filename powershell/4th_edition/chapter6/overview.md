# Overview
* Today I felt pretty good about learning everything in powershell. It's a lot of looking at the documentation to understand how it works and sometimes a bit
frustrating when looking over it for a while. Either way I like the challange as it helps me think and troubleshoot and it feels satisfying when I find the answer to my problem.
# Lab 6

### 1. Create two similar, but different, text files. Try comparing them by using Compare-Object. Run something like this: ```Compare-Object -Reference (Get-Content File1.txt) -Difference (Get-Content File2.txt)```. If the files have only one line of text that’s different, the command should work.
*Awnser*
* I used the initial command that was given, and that did not work. I then looked at the documentation and found the correct way to do it
 ```Get-Content -ReferenceObject (Get-Content .\Test.txt) -DifferenceObject (Get-Content .\TestComapre.txt)```

<img width="857" height="165" alt="image" src="https://github.com/user-attachments/assets/2727fc30-ab14-423f-95d9-d12e9df44978" />

---

### What happens if you run Get-Command | Export-CSV commands.CSV | Out-File from the console? Why does that happen?
*Awnser*
* An Error appears because the path is not specified in Out-File
 <img width="858" height="76" alt="image" src="https://github.com/user-attachments/assets/bea9bcc1-bffa-433c-a034-9cbd08502654" />

---

### Apart from getting one or more jobs and piping them to Stop-Job, what other means does Stop-Job provide for you to specify the job or jobs you want to stop? Is it possible to stop a job without using Get-Job at all
*Awnser*
* This question felt like a trick question because as soon as I looked at the documentation, i found out that piping was not needed at all
  , and that is the case.
<img width="627" height="362" alt="image" src="https://github.com/user-attachments/assets/a76138a7-5a3c-4518-8776-62d49daf6ebd" />

---

### 4. 
*Awnser*
* This one was a bit more difficult, but after reading the documentation and parameters again, it was pretty easy to figure out
* ```Get-Process | Export-Csv -Path Processes.cv -Delimiter '|'```
  
  <img width="797" height="528" alt="image" src="https://github.com/user-attachments/assets/bd3b6279-fe90-4c86-9927-2adbff022b21" />

---
  
### 5. How do you include the type information in the # comment line at the top of an exported CSV file?
*Awnser*
* This also took me a bit to read through the documentation, but I eventually found it. ```Export-Csv -IncludeTypeInformation```
  would print the first line of the CSV in #.

 <img width="847" height="158" alt="image" src="https://github.com/user-attachments/assets/270d247b-989e-43d8-a0c2-1a94340333de" />

---

### 6. Export-Clixml and Export-CSV both modify the system because they can create and overwrite files. What parameter would prevent them from overwriting an existing file? What parameter would ask whether you were sure before proceeding
to write the output file?
*Awnser*
* I remember this command from a previous assignment, and that I've been reading the documentation I'm starting to learn what every parameter does
 to prevent overwrite it uses the parameter ```-NoClobber``` and to ask for confirmation use ```-Confirm```

<img width="852" height="261" alt="image" src="https://github.com/user-attachments/assets/161c97d7-de7d-4640-bc8f-5c38ff6667fd" />
<img width="660" height="226" alt="image" src="https://github.com/user-attachments/assets/41c21647-a1d0-470c-97b2-ffa7dd9eb160" />

---

### 7. The operating system maintains several regional settings, which include a default list separator. On US systems, that separator is a comma. How can you tell Export-CSV to use the system’s default separator rather than a comma?
*Awnser*
* This command frustrated me as I've been reading documentation, and I just didnt understand what "Culture" meant when reading it over
  I did have to look it up to see what it was, and it is ```-UseCulture```.

  <img width="828" height="265" alt="image" src="https://github.com/user-attachments/assets/54080911-509f-4b99-b31f-c480feba8cc7" />

---



