# Lab 7
## ThingSpeak and Google Sheets 
### Instructions: 
Review Lesson 7 in the GitHub repository. Sign up and log in to MathWorks ThingSpeak. Run thingspeak_cpu_loop.py or thinkspeak_feed.py in a demo folder. Install gspread and oauth2client. Log in the Google Cloud Platform Identity and Access Management, create a project called cpudata, enable both Drive API and Sheets API, and create and download service account JSON key file. Then, start a new Google sheet called cpudata, share it with the client email in the JSON file, delete Rows 2 to 1000, and edit the header cells. Run cpu_spreadsheet.py with the JSON key file in a demo folder. Document results to your GitHub repository. 

--- 
## Running thingspeak_feed.py 
I already had a MathWorks account, so all I had to do was log in in order to get access to ThingSpeak. On 
ThingSpeak, I created a new channel called "cpu_loop," labelled field1 "cpu_pc," and labelled field 2 "mem_avail_mb." 
![ThingSpeak channel image](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/ThingSpeakchannellab7.png)
After saving the channel, I went to the API Keys tab and copied the Write API Key. After doing so I executed the following code to run thingspeak_feed.py:
```
$ sudo pip3 install -U psutil
$ cd ~/demo
$ cp ~/iot/lesson7/thingspeak_cpu_loop.py .
$ cp ~/iot/lesson7/thingspeak_feed.py .
$ cat thingspeak_cpu_loop.py
$ cat thingspeak_feed.py
$ python3 thingspeak_feed.py
```
</br>

Upon executing `python3 thingspeak_feed.py` the terminal gave me an option to enter the Write API Key.
I entered the Write API Key I copied from ThingSpeak and then said yes to save the key for future use. 
![Enter API Key](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/lab7ss3%20copy.png)

</br>

Once the key was entered and saved, thingspeak_feed.py began running. The output of this program is pictured below: 
![thingspeak_feed.py output](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/lab7thingspeakoutput.png)

---
## Installing gspread and oauth2client
I used the following command to install gspread and oauth2client: `pip3 install -U gspread oauth2client`

---
## Google Cloud Platform & Google Sheets
I logged into the Google Cloud Platform and created a new project called "cpudata." Then from the APIs & Services menu I enabled both Google Drive API and Google Sheets API. After I went to the credentials menu under APIs & services. I clicked create credentials -> service account key. I named the service account cpudata. Then I navigated to the keys tab for cpudata, created a JSON key, and downloaded a copy of it. In order to prepare to run cpu_spreadsheet.py I ran the following lines of code:
```
$ cd demo
$ cp ~/iot/lesson3/system_info.py .
$ cp ~/iot/lesson7/rpi_spreadsheet.py .
$ mv ~/Downloads/rpidata-*.json ~/demo 
```
After executing the code, I went to Google Sheets and started a new spreadsheet called "cpudata." 
I shared the spreadsheet with the "client_email" address in my .json file and allowed that email to have edit access. To set up the spreadsheet I deleted rows 2-1000 and entered the following header cells: Date / Time, CPU Usage (%), Memory Available (GB).

</br>

Then, in the terminal I ran `nano cpu_spreadsheet.py` to edit the file. A picture of my edits are shown below. 
![nano spreadsheet image](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/lab7nanofile.png)

</br>

After doing this, I ran cpu_spreadsheet.py by executing `python3 cpu_spreadsheet.py`. The results of this program are shown below: 
![terminal results](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/terminalOutputlab7.png)
![sheets results](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab7/lab7images/googlesheetsOutputlab7.png)

</br>

Note that this Python script, continually collected CPU data every 10 seconds until the script was quit. 

---

## Summary
By completing this lab, I learned how to upload data to ThingSpeak for IoT visualization and how to use the Google Cloud Platform and Python scripts to write information to Google Sheets. 

---
Author: Arden Sentak
I pledge my honor that I have abided by the Stevens Honor System.






