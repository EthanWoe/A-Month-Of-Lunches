# Overview
* Hard becuase i dontt have a azure subscription and using multiple commands in () is difficutlt for me to remember.
# Lab10

### 1. Would the following command work to retrieve a list of commands from modules that start with Microsoft.* on the current machine? Why or why not? Write an explanation, similar to the ones we provided earlier in this chapter.
*Answer*
* Yes it returns as it just gets all aviable by name of Microsoft.(anything).
  <img width="871" height="148" alt="image" src="https://github.com/user-attachments/assets/5077d3be-3443-4d6b-b093-460f1574733e" />

### 2. Would this alternative command work to retrieve the list of commands from the same modules? Why or why not? Write an explanation, similar to the ones we provided earlier in this chapter.
*Awnser*
* No as this is trying to recieve a command and not and not a module.
  <img width="866" height="322" alt="image" src="https://github.com/user-attachments/assets/19736529-ae64-41a1-9b39-6fef3be437c1" />

### 3. Would this set the subscription in the Azure context? Consider ifGet- AzSubcription retrieves multiple subscriptions. ```Get-AzSubscription | Select-AzSubscription```
*awnser*
* Whicever Subscription is done the most recently will be selected by this command.

### 4. Write a command that uses pipeline parameter binding to retrieve the first subscription and set that in the Azure context. Don’t use parentheses.
*Awnser*
```Get-AzSubscription | Select-Object -First 1 | Select-AzSubscription```

### 5. Write a command that uses pipeline parameter binding to retrieve the first subscription and set that in the Azure context. Don’t use pipeline input; instead, use a parenthetical command (a command in parentheses).
*Awnser*
* ```Select-AzSubscription -SubscriptionObject (Gett-AzSubscription | Select-Object -First 1)```

#### 6. Sometimes someone forgets to add a pipeline parameter bindingto a cmdlet. For example, would the following command work to set the subscription in the Azure context? Write an explanation, similar to the ones we provided earlier in this chapter.
*Awnser*
* This will not  work as  the first input is a string  so it wont  go down the  pipe.
