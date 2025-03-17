# Lab 8
## Data Analysis 
### Instructions: 
Go to the GitHub repository lesson 8. Install the Python packages mentioned. Save the Google Sheet from
Lab 7 in CSV format to ~/demo. Copy ~/iot/lesson8/plt_final.py and plt_cv2.py to ~/demo. Edit plt_final.py and plt_cv2.py to read your CSV file with customized plot/data titles. Run plt_final.py and plt_cv2.py. Running these scripts will result in seven figures including time series, two histograms, two box plots, a scatter plot, and a cross-validation predicition. Document the results to your GitHub repository. 

--- 
## Installing Python Packages:
To install the Python packages needed for this lab I ran the command: </br>
`pip3 install numpy scipy scikit-learn matplotlib pandas tensorflow keras`

---
## Data Analysis: 
In order to set up for data analysis, I downloaded my Google Sheet from Lab 7 called "cpudata" as a .csv file. Then I moved this file into ~/demo. After doing so I executed the following commands:
- `cd ~/demo`
- `cp ~/iot/lesson8/plt_final.py .`
- `cp ~/iot/lesson8/plt_cv2.py .`
- `nano plt_final.py`
- `nano plt_cv2.py`

The nano commands were used to change the Python scripts to fit my data. In these files I changed plot titles, axis titles, and made sure that any commands involving reading my file were switched to correspond to my file name (cpudata.csv) or, similarly, my column titles. Note that in lab 7 I recorded CPU Usage and Memory Available instead of CPU Usage and Temperature. Therefore, all plots that have a comment to be a temperature plot were switched to Memory Available plots so that my data was fit. 

</br> 

Here is my final version of plt_final.py:
![nano plt_final](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab8pltfinalss.png)


</br> 

Here is my final version of plt_cv2.py:
![nano plt_cv2](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab8cv2ss.png)

</br> 

After editing these files I ran the following two commands: 
- `python3 plt_final.py`
- `python3 plt_cv2.py`

</br>
These commands resulted in 7 plots being displayed. All plots are pictured below.

## Time Series Plot: 
![Time Series Plot](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab8timeseries.png)

## 2 Histograms & 2 Box Plots:
![Histograms & Box Plots](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab84plots.png)
## Scatter Plot: 
![Scatter Plot](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab8scatter.png)
## Cross-Validation Plot: 
![Cross Validation Plot](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab8/Lab8images/lab8crossvalidation.png)

</br>

These plots allowed me to gain insight regarding CPU Usage and Memory Available on my personal MacBook. 

--- 
## Summary

In this lab, I learned how to utilize Python to write/edit scripts that can plot data. Data plots are extremely useful for data analysis as it allows you to easily comprehend trends found in large quantities of data points. 

---
Author: Arden Sentak </br>
I pledge my honor that I have abided by the Stevens Honor System.
