# Lab 3
## Python 
### Instructions:
Go to the IOT GitHub repository and review lesson 3. Install required Python packages such as jdcal, astral, and geopy. Execute the following code: </br>
`cd ~/iot`,
`cd *3`,
`python3 julian.py`,
`python3 date_example.py`,
`python3 datetime_example.py`,
`python3 time_example.py`,
`python3 sun.py "New York"`,
`python3 moon.py`,
`python3 coordinates.py "Samuel C. Williams Library"`,
`python3 address.py "40.74480675, -74.02532861159351"`,
`python3 cpu.py`,
`python3 battery.py`,
`python3 documentstats.py document.txt`.
</br> 
Document the results to your GitHub repository. 

---

## cd ~/iot
This command changes directories to iot. Note that in a previous lab the iot GitHub repository was copied. The directory "iot" has access to all files/folders from this repository. 
![terminal view of cd iot](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss1.png)
## cd *3
This command changes directories to the first directory in iot that has a 3 in it. In this case this is the directory "lesson3"
![terminal view of cd *3](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss2.png)
## python3 julian.py
This command runs a python script called julian.py. It gives the calendar date, Julian date, and modified Julian date.
![terminal view of python3 julian.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss3.png)
## python3 date_example.py
This command runs a python script called date_example.py. It gets the current date, formats it in a couple different ways, and calculates the number of days since the first day of classes and until the last day of classes. 
![terminal view of python3 date_example.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss4.png)
## python3 datetime_example.py
This command runs a python script called datetime_example.py. It displays time in a couple different ways using the datetime and time modules.
![terminal view of python3 datetime_example.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss5.png)
## python3 time_example.py
This command runs a python script called time_example.py. It continuously prints the current local time every 10 seconds until interrupted. You can stop this by pressing Ctrl C.
![terminal view of python3 time_example.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss6.png)
## python3 sun.py "New York"
This command runs a python script called sun.py. It takes in a city, then gives data regarding the sun such as sunrise, sunset, dawn, dusk, and noon. 
![terminal view of python3 sun.py "New York"](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss7.png)
## python3 moon.py
This command runs a python script called moon.py. It prints out the phases of the moon for the next 30 days starting with the current day.
![terminal view of python3 moon.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss8.png)
## python3 coordinates.py "Samuel C. Williams Library"
This command runs a python script called coordinates.py. It takes in an address or landmark, uses the geopy library to find its geographical coordinates, and prints the full address along with its latitude and longitude.
![terminal view of python3 coordinates.py "Samuel C. Williams Library"](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss9.png)
## python3 address.py "40.74480675, -74.02532861159351"
This command runs a python script called address.py. It takes in geographical coordinates, uses the geopy library to find the corresponding address, and prints the full address along with its latitude and longitude.
![terminal view of python3 address.py "40.74480675, -74.02532861159351"](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss10.png)
## python3 cpu.py
This command runs a python script called cpu.py. It displays the number of physical and logical CPU cores and prints CPU utilization percentages for each core every second for 10 seconds.
![terminal view of python3 cpu.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss11.png)
## python3 battery.py
This command runs a python script called battery.py. It prints current battery statistics (percentage, seconds left, and whether or not computer is plugged in).
![terminal view of python3 battery.py](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss12.png)
## python3 documentstats.py document.txt. 
This command runs a python script called documentstats.py. It reads a text file (in this case document.txt), counts the occurrences of wordsmexcluding common stop words, and prints the total word count along with the top ten most frequent words.
![terminal view of python3 documentstats.py document.txt](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab3/lab3images/ss13.png)


