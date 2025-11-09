# Overview
* Today felt ok it felt easy and hard for some parts but pretty easy nonetheless.
# Lab 8

### 1. Identify a cmdlet that produces a random number.
*Awnser*
* ```help-random``` then i using what the output gave me i did ```help get-random``` to confirm that the command was coreect then
  finally did ```get-random```
<img width="323" height="47" alt="image" src="https://github.com/user-attachments/assets/6aa20cc7-d61c-446e-b652-6ca73994aa5c" />

---

### 2. Identify a cmdlet that displays the current date and time
*Answer*
* ``` Help Date``` then ```Get-Date``` to display current date and time.

<img width="378" height="77" alt="image" src="https://github.com/user-attachments/assets/3d00a0b5-754e-44d5-a8a5-7e7a9bfe5dcf" />

---

### 3. What type of object does the cmdlet from task 2 produce? (What is the TypeName of the object produced by the cmdlet?
*Answer*
* To find the typename of the object i needed to do ```Get-Date | gm ``` this was a command previously used in the lab description section.
* <img width="378" height="70" alt="image" src="https://github.com/user-attachments/assets/1abbfb51-d5f6-4322-9e2e-8fdf92bfd3de" />

---

### 4. Using the cmdlet from task 2 and Select-Object, display only the current day of the week in a table like the following (caution: the output will right-align, so make sure your PowerShell window doesn’t have a horizontal scrollbar)
*Answer* 
* To do this I looked at the names of the properties in ```get-date | gm``` and then did ```Get-Date | Select-Object DayOfWeek```
<img width="606" height="106" alt="image" src="https://github.com/user-attachments/assets/17898a3e-30a5-4d0e-8cd5-f61bcb158025" />

---

### 5. dentify a cmdlet that will show you all the times in a directory.
*Answer*
* For this one i was thinking too one dimeensionaly I kept trying to search and look through ```help time``` and ```help directory```
  But the awnser is ```get-childitem```

<img width="513" height="327" alt="image" src="https://github.com/user-attachments/assets/1b4a6041-fd2d-4262-bb28-951e8a171c5e" />

---

### 6. Using the cmdlet from task 5, display all the times in the directory of your choice. Then extend the expression to sort the list by the time the items were created and display only the filename(s) and the date created. Remember that the column headers shown in a command’s default output aren’t necessarily the real property names—you need to look up the real property names to be sure.
*Answer*
* To find this i just did similiar to what i did before. ```Get-ChildItem | Select-Object Nmae,CreationTime```
<img width="596" height="467" alt="image" src="https://github.com/user-attachments/assets/411f4d09-864a-4cd8-b2a0-bcc94f5815fb" />

---

### 7. Repeat task 6, but this time sort the items by the last write time; then display the filename, creation time, and the last write time. Save this in a CSV file and an HTML file.
*Awnser* 
* Essentially the same but i have to add a sort object cmdlet. ```Get-ChildItem | Sort-Object LastWritetTime | Select-Object LastWriteTime,Name | Outtfile childitem.html/csv```
* <img width="872" height="522" alt="image" src="https://github.com/user-attachments/assets/da95a72b-6059-4a49-bd2e-a9f367e941d8" />




