+++
date = '2025-03-06T22:11:17+05:30'
draft = false
title = 'Disable Suspend in Linux'
+++


If your Linux system is automatically suspending or sleeping and you want to disable this behavior, you can prevent it using `systemctl`.  

### **Disable Suspend and Sleep**  
Run the following command to disable both suspend and sleep modes:  

```
sudo systemctl mask sleep.target suspend.target
```  
After executing the command, restart your system for the changes to take effect.  

### **Re-enable Suspend and Sleep**  
If you need to restore the suspend and sleep functionality, use:  

```
sudo systemctl unmask sleep.target suspend.target
```  

This will allow your system to enter suspend and sleep modes again.  

