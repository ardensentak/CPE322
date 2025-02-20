# Lab 6
## Node.js and Pystache
### Instructions:
Go to lesson 6 in the GitHub repository. Install Node.js and run hello-world.js, hello.js, and http.js. For each, refresh the webpage to see the server activities. Then, installl Pystache 
and run say_hello.py that uses the template say_hello.mustache. Document your results to your GitHub repository.

---
## Node.js:
Node.js was already installed on my mac so I was able to start with running the scripts. To do this I executed the following series of commands: 
- `cd ~/iot/lesson6`
- `node hello-world.js` (I pressed ctrl C to exit the server)
- `node hello.js` (I pressed ctrl C to exit the server)
- `node http.js` (I pressed ctrl C to exit the server)
![node.js terminal code](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab6/lab6images/nodejscode.png)

Each running webpage displayed different server activity. As can be seen in the image above, hello-world.js did not display any server activity. Hello.js responded to a refresh with outputting
"response end call done" and "request end event fired" to the terminal. Lastly, http.js responded with a count of how many times the webpage had been refreshed. 

The following images show what each webpage looked like: 

### hello-world.js:
![hello-world.js webpage](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab6/lab6images/helloworldjsserver.png)

### hello.js:
![hello.js webpage](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab6/lab6images/hellojsserver.png)

### http.js:
![http.js webpage](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab6/lab6images/nodehttpjspage.png)

---
## Pystache:
I installed Pystache on my mac using the command `pip3 install pystache`. Then I executed the following commands in order to 
run say_hello.py that uses the template say_hello.mustache.
- `cd ~/iot/lesson6`
- `cat say_hello.mustache`
- `cat say_hello.py`
- `python3 say_hello.py`

The results of these commands are shown below: 
![pystache results](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab6/lab6images/pystache.png)

---
## Summary:
By completing this lab I learned how to run webpages using node.js and how to use Pystache, which is a python implementation of Mustache. 

---

Author: Arden Sentak </br>
I pledge my honor that I have abided by the Stevens Honor System. 
