# Lab 5
## Paho - MQTT
### Instructions: 
Go to the iot GitHub repository and review Lesson 5. Install Paho-MQTT. Change directories to the iot repository and update the repository with `git pull `. Then change directories to lesson5. Run `python3 subcpu.py` on one terminal and `python3 pubcpu.py` on another. Document the results to your GitHub repository.

---

## Installation:
I installed Paho-MQTT by executing the following commands on my mac:
- `brew install mosquitto`
- `brew services start mosquitto`
- `pip3 install paho-mqtt`

 ---
 
## Setting Up Terminals and Running Scripts:
I opened two terminal windows and typed the following commands on both: 
- `cd ~/iot`
- `git pull`
- `cd lesson5` </br>
Changing directories to the iot directory then using `git pull` ensured that I had the latest version of the iot GitHub repository on my device. Then I changed directories into lesson5 since the python files I ran in the next step were located there. </br>


After setup, on one terminal I ran the command `python3 pubcpu.py`.
![pub terminal setup](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab5/lab5images/setupPUB.png)

Similarly, after setup on the other terminal I ran the command `python3 subcpu.py `.
![pub terminal setup](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab5/lab5images/SUBsetup.png)


As a result of running these commands, the terminal that ran pubcpu.py published data relating to my CPU. Furthermore, the terminal that ran subcpu.py, subscribed to the pubcpu.py terminal and printed out the data coming from the pubcpu.py terminal. The image below shows the output of the terminal that published data on the left and the output of the subscribed terminal on the right. 
![subcpu and pubcpu terminal results](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab5/lab5images/lab5results.png)

---
## Summary:
In this lab I learned how to use paho-mqtt to publish messages from the terminal and how to subscribe one terminal to another. 
