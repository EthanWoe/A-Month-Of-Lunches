# Overview

# Lab

### 1. Create a new directory called Labs.
*Awnser*
*  I just used basically the same thing I did yesterday```New-Item -ItemType Directory -Name Test``` Then I realised
that I accidentally named it the wrong thing. So to find out how to fix it i did ```help rename``` and found the command ```Rename-Item```
which I then did ```help Rename-Item``` to figure out the file paths and see the examples. Finally, I got the answer to
```Rename-Item -Path .\Test\ -Newname Lab```.
<img width="703" height="330" alt="image" src="https://github.com/user-attachments/assets/e9e778b4-bb1e-450e-a799-40132448d7d9" />

---
### 2. Test
*Awnser*
* ```New-Item -ItemType Directory -Name Test.txt -Path .\Lab\```
<img width="621" height="132" alt="image" src="https://github.com/user-attachments/assets/49c737b9-2656-42a4-86f7-f8165702d356" />

---
### 3. Is it possible to use Set-Item to change the contents of /Labs/Test.txt to -TESTING? Or do you get an error? If you get an error, why?
*Awnser*
* After searching for a bit to find what parameter to use, I decided to use ```Set-Item -Path .\Test -Value "-Testing"```
  and received an error saying it does not support this operation. I think this is the case because it's changing the actual file's
  value and not the content, like what the question wanted.
 <img width="842" height="53" alt="image" src="https://github.com/user-attachments/assets/63f3052d-dc57-46f2-9b1b-17e570fabebe" />

 
 ---
 
### 4.  Using the Environment provider, display the value of the system environment variable PATH.
*Awnser*
* I originally thought that the answer to this question was ```Get-Item -Path Env``` which shows all of the variables and their values, but the true answer
* was ```Get-Item -Path env:PATH``` which lists the specific variable named ```PATH```
<img width="647" height="161" alt="image" src="https://github.com/user-attachments/assets/1bb48ae3-e7b8-4543-bab8-86ed298aa2f4" />

---

### 5. Use help to determine what the differences are between the - Filter, -Include, and -Exclude parameters of Get-ChildItem
*Awnser*
* -Filter:
  * Specifies a filter to qualify for the Path Parameter. Such as .txt
* -Include:
  * Specifies an array of one or more string patterns to be matched as the cmdlet gets child items. Chooses specific items
-Exclude:
  * Specifies that arrays of one or more strings are matched to the cmdlet to get child items. Skips specific items



