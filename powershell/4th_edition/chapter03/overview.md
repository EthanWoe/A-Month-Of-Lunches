# General Overview
* This chapter was pretty good I thought. I find it hard to read and i see myself going back to it to reference during the lab as its hard for me to learn by just reading it. But this Lab and the chapter are good skills to know as it is mostly about learning how to search and find awnsers. for yourself.
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
* Again similiar to before ```Get-Command alias```
<img width="647" height="292" alt="image" src="https://github.com/user-attachments/assets/d5e93266-b12d-46ab-b378-0fc33f14263a" />

---

### 7. Is there a way to keep a transcript of everything you type in the shell, and save that transcript to a text file?

**Answer:**  
* ```Get-Command -Noun transcript```

<img width="651" height="182" alt="image" src="https://github.com/user-attachments/assets/032af984-1a71-4e65-9296-7e22ffde70d4" />


---

### 8. Getting all processes can be overwhelming. How can you get processes by the name of the process?
**Answer:**  
* This one i spent a bit more time on. I initally did ```Command-Get -Noun Process``` Then based on the commands given I assumed that ```Get-Process``` was the most accurate one. I then looked inside doing ```Help Get-Process``` which gave me a lot of information on the command. To make the command give me exactly what i wanted i found that you can use ```Parameter``` so the final command ending up being ```Help Get-Process -Parameter Name```.
<img width="636" height="295" alt="image" src="https://github.com/user-attachments/assets/766a3fff-13fc-43a7-80ac-d5106677b04b" />

---

### 9. Is there a way to tell Get-Process to tell you the user who started the process?
**Answer:**  
* Similiar to the last one but i saw in the first line that it was there. ```Help Get-Process -Parameter IncludeUserName```
<img width="631" height="297" alt="image" src="https://github.com/user-attachments/assets/d27e209e-d645-4d99-a4fd-29a6bd9a4672" />

---

### 10. Is there a way to run a command on a remote host? (Hint: Invoke is the verb for running something now.)
**Answer:**  
* I found the command pretty much right away by using ```Get-Help -Verb Invoke``` This led to me to ```Invoke-Command```. After this though i was stuck on what to do so I looked at the Awnser and saw that it Included ```-Parameter -Hostname or -Computername``` Seeing this I was confused on how I was supposed to find these but that is the point. I spent around 20ish minutes looking in online documentation and the full documentation to understand wherer i was supposed to go and the steps to get there. Final awnser is ```Help Invoke-Command -Parameter -Hostname/Computername```


<img width="721" height="450" alt="image" src="https://github.com/user-attachments/assets/c873aeab-a44f-4170-a0da-b3f6403263bc" />


---

### 11. Examine the help file for the Out-File cmdlet. The files created by this cmdlet default to a width of how many characters? Is there a parameter that would enable you to change that width?
**Answer:**  
* After learning how to look at parameters and help files this one was a breeze. I typed ```help Out-File``` Then searched until i saw width. The awnser is ```help Out-File -Parameter Width```

---

### 12. By default, Out-File overwrites any existing file that has the same filename as what you specify. Is there a parameter that would prevent the cmdlet from overwriting an existing file?
**Answer:**  
* Same as above. ```help Out-File -Parameter NoClobber```

<img width="845" height="371" alt="image" src="https://github.com/user-attachments/assets/c2c1ca0b-55ad-4fcf-8349-4dc35c7a1c2f" />

---

### 13. How could you see a list of all aliases defined in PowerShell?
**Answer:**  
* I intillay did ```help *alias``` Then i saw ```Get-Alias``` and did ```help Get-Alias``` Finally running it geiving me the awnser ```Get-Alias```.
 
<img width="537" height="285" alt="image" src="https://github.com/user-attachments/assets/24d479ea-8752-48d0-a6df-e8bdaa0099b4" />

---

### 14. Using both an alias and abbreviated parameter names, what is the shortest command line you could type to retrieve a list of commands with the word process in the name?
**Answer:**  
* Using ``Get-Alias`` I found the shortened git command and I found the other command by messing around trying to shorten the noun got me to the shorter noun. Tried to research how to find but could not come to a proper conclusion. Command ```Gcm -No Process```
<img width="862" height="277" alt="image" src="https://github.com/user-attachments/assets/a3f0988d-0b4f-4a28-a4d4-d7d40346287e" />

---

### 15. How many cmdlets are available that can deal with generic objects? (Hint: Remember to use a singular noun like object rather than a plural one like objects.)
**Answer:**  
* I thought this was harder then it was considering the research i had to do previously but its literally just ```gcm -noun object```

<img width="847" height="317" alt="image" src="https://github.com/user-attachments/assets/aaa96328-7292-4a2c-a04a-506d91f0a142" />

---

### 16. This chapter briefly mentioned arrays. What help topic could tell you more about them?
**Answer:**  
* ```help arrays```
<img width="731" height="352" alt="image" src="https://github.com/user-attachments/assets/d5ec1bbf-cc61-4a2f-9c42-b5e3dec03b79" />
