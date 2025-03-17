# Lab 9 
## YANG
### Instructions: 
Review lesson 9 in the GitHub repository. Install pyang and PlantUML. Copy ~/iot/lesson9/intrusiondetection.yang to ~/demo. Run pyang to generate intrusiondetection.yin and intrusiondetection.uml. Run PlantUML to generate intrusiondetection.png. Document results to your GitHub repository. 

---

## Installing pyang and PlantUML
To install pyang and PlantUML on my Mac I used the following commands: 
- `pip3 install -U lxml pyang`
- `pip3 install -U plantuml`

## Pyang
I copied intrusiondetection.yang into demo & switched to the demo directory with: 
- `cp ~/iot/lesson9/intrusiondetection.yang ~/demo`
- `cd ~/demo`

Then I executed the following commands to generate intrusiondetection.yin & intrusiondetection.uml while also showing the instrustiondetection file in .yang, .yin, and .uml forms.
- `cat intrusiondetection.yang`
- `pyang -f yin -o intrusiondetection.yin intrusiondetection.yang`
- `cat intrusiondetection.yin`
- `pyang -f uml -o intrusiondetection.uml intrusiondetection.yang --uml-no=stereotypes,annotation,typedef`
- `cat intrusiondetection.uml`

Pictured below are the contents of the intrusiondetection file in each format.
</br>

### .yang:
![.yang1](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/lesson9catyang1.png)
![.yang2](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/lesson9catyang2.png)

</br>

### .yin:
![.yin1](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/lesson9catyin1.png)
![.yin2](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/lesson9catyin2.png)

</br>

### .uml: 
![.uml](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/lesson9uml.png)

</br>

## PlantUML
I ran the command `python3 -m plantuml intrusiondetection.uml` to create a sequence diagram in PNG format. Then I installed & ran GIMP and Pinta in order to display the PNG file. To do this I used the following commands: 
- `brew install gimp pinta`
- `cd ~/demo`
- `open -a Pinta ~/demo/intrusiondetection.png` Note: I used this command since `pinta intrusiondetection.png` was not working on my computer
- `gimp -h`
- `gimp -a intrusiondetection.png`

The same PNG image was shown within both the Pinta and GIMP applications. 
### PNG image
![PNG](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab9/lab9images/intrusiondetection.png)

--- 
## Summary
In this lab I explored what a file looks like in .yang, .yin, .uml, and .png forms. Pyang is a helpful tool to use when you need to convert YANG models to YIN or UML form. PlantUML is a helpful tool that can create PNG images/diagrams from a UML file. 

---
Author: Arden Sentak </br>
I pledge my honor that I have abided by the Stevens Honor System.
