
# File Integrity Monitoring with Wazuh 

## Objective
In this lab we will simulate a File Intergrity Monitoring check (FIM) on Wazuh SIEM on the Ubuntu system. 

## Tools Used: 
Software: 
 - Ubuntu
 - Wazuh 4.7

# Steps:
  1. With Wazuh installed and booted up and endpoint system started, start up terminal enter in the following commands:
     
     ![image](https://github.com/dilocho/File-Intergrity-Monitoring/assets/38048735/231999e7-288c-4b22-9484-d57c4c12629c)
     
      *Ref 1. Change Directory and open file contents*

  3. Using Nano will open up the ossec.conf file for changing, scroll down to directories to change and add the desired directory to monitor. In my case it was my documents folder. 

     ![image](https://github.com/dilocho/File-Intergrity-Monitoring/assets/38048735/fafac0f0-2def-4f46-bdde-368bc1381a66)

      *Ref 2. Nano function acts as a terminal text editor and will display the contents of the document in the terminal window.*
     
  4. Note that in the <> that you can define the specifics of the monitoring, in this case I wanted all checks, changes and in real-time reporting.
  6. Press Ctrl X to exit, y to save and enter to leave the filename as is. 
  7. Then restart your agent with the follwing code:

     ![image](https://github.com/dilocho/File-Intergrity-Monitoring/assets/38048735/d7105f20-fa37-471e-b3b2-af0a9d839bd8)
     
      *Ref 3. Restart code for wazuh-services*
     
  9. Once restarted head over to the Wazuh dashboard and go to Modules, <Device Name> then Security Event to monitor the changes. 
  10. In the directory which you added to the ossec.conf file add a new file and make some changes. In my case I added one new file, saved it then made two changes on two separate occasions. 
  11. Looking now at Wazuh you will be able to see the changes as shown below:

      ![image](https://github.com/dilocho/File-Intergrity-Monitoring/assets/38048735/c0f53139-6e63-4ef3-b915-95095cf257b1)
      
      *Ref 4. Wazuh Dashboard showing File changes*
       
# Skills Learned: 
In this lab I learned how to: 
- Navigate through Linux system using the nano cd functions 
- Changed configuration files with Wazuh to specifically target directories 
- To recheck all changes and configurations to ensure that it was correct as I recieved some errors upon trying to restart the Wazuh agent
- Observing changes in Wazuh and rule id’s FIM falls under.
      
# Conclusion: 
After testing the FIM I found that using the SIEM can be very helpful in monitoring file change activity, displaying alerts and notifying SIEM analysts of potential breaches or changes within users systems. 

# References: 
  https://documentation.wazuh.com/current/proof-of-concept-guide/poc-file-integrity-monitoring.html 
      
