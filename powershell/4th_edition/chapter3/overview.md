# General Overview

# Lab 3

### 1. Run Update-Help, and ensure that it completes without errors so that you have a copy of the help on your local computer. You need an internet connection.
**Answer:**  

* In the lab initially, I already ran the ```Update-Help``` command,
so when I ran it again I did not receive any response. To see what was going wrong, I added a ```-Verbose``` and was getting an error that I had already updated within
24hrs and to do it again, I needed to add a ```-Force``` to the end of the file. So the result ended up being ```Update-Help -Force```

<img width="658" height="57" alt="image" src="https://github.com/user-attachments/assets/eba30dc6-58d9-411f-bc52-29844a5b5ccc" />

---

### 2. Can you find any cmdlets capable of converting other cmdlets’ output into HTML?
**Answer:**  

* To find this, I typed in ```Help *HTM``` and then pressed Tab to see if there were commands that would be similar to what I need
This then gave me a ```Help CovertTo-HTML``` and the description of it matched the question requirements.

<img width="913" height="137" alt="image" src="https://github.com/user-attachments/assets/343364d3-1cfd-4ac4-888f-6d693d014c26" />

---

### 3. Are there any cmdlets that can redirect output into a file?

**Answer:**  

* This one I got stuck on a bit because I did not understand the ``Get-Command`` naming conventions, including things like noun. After researching, I searched ```Get-Command -Noun file, printer``` and it generated the result ```Out-File```. I then used ```Help Out-File``` and its description is that it sends an output to a file.

<img width="477" height="353" alt="image" src="https://github.com/user-attachments/assets/44f2a989-f5c3-4a11-a0d0-da9248588148" />

---

### 4. How many cmdlets are available for working with processes? (Hint: Remember that cmdlets all use a singular noun.)
**Answer:**  

* After learning the previous command, this one was way easier. I typed ```Get-Command -Noun process``` which listed 5 different cmdlets.

<img width="438" height="235" alt="image" src="https://github.com/user-attachments/assets/c60bcabe-1c39-4be7-8bd1-3778a27cb53d" />

---

### 5. What cmdlet might you use to set a PowerShell breakpoint? (Hint: PowerShell-specific nouns are often prefixed with PS.)
**Answer:**  
* I tried to type something similar to the last two with the ```Get-Command -Noun PS,Breakpoint```. This did not work for me, and after messing around and using the hint in the question, I changed the command to ```Get-Command -Noun PSBreakpoint``` and it returned the cmdlets.


<img width="652" height="245" alt="image" src="https://github.com/user-attachments/assets/510d5247-1a92-4849-ac0d-1b1128de8115" />


---

### 6. You’ve learned that aliases are nicknames for cmdlets. What cmdlets are available to create, modify, export, or import aliases?
**Answer:**  
*Your answer here.*

---

### 7. Is there a way to keep a transcript of everything you type in the shell, and save that transcript to a text file?
**Answer:**  
*Your answer here.*

---

### 8. Getting all processes can be overwhelming. How can you get processes by the name of the process?
**Answer:**  
*Your answer here.*

---

### 9. Is there a way to tell Get-Process to tell you the user who started the process?
**Answer:**  
*Your answer here.*

---

### 10. Is there a way to run a command on a remote host? (Hint: Invoke is the verb for running something now.)
**Answer:**  
*Your answer here.*

---

### 11. Examine the help file for the Out-File cmdlet. The files created by this cmdlet default to a width of how many characters? Is there a parameter that would enable you to change that width?
**Answer:**  
*Your answer here.*

---

### 12. By default, Out-File overwrites any existing file that has the same filename as what you specify. Is there a parameter that would prevent the cmdlet from overwriting an existing file?
**Answer:**  
*Your answer here.*

---

### 13. How could you see a list of all aliases defined in PowerShell?
**Answer:**  
*Your answer here.*

---

### 14. Using both an alias and abbreviated parameter names, what is the shortest command line you could type to retrieve a list of commands with the word process in the name?
**Answer:**  
*Your answer here.*

---

### 15. How many cmdlets are available that can deal with generic objects? (Hint: Remember to use a singular noun like object rather than a plural one like objects.)
**Answer:**  
*Your answer here.*

---

### 16. This chapter briefly mentioned arrays. What help topic could tell you more about them?
**Answer:**  
*Your answer here.*
