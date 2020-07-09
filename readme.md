# URL SHORTENER WEB APP USING FLASK

### List of contents

- [Introduction](#introduction)
- [Working](#working)
- [Installation](#installation)
- [Running](#running)


## Introduction
---
[(Back to top)](#list-of-contents)

url shortener is web app created using flask , The purpose of this app is to convert long complex url's into simpler url and it also stores the visits you make to those url's


## Working
---
[(Back to top)](#list-of-contents)

The step-by-step procedure of the Project:

+ The database is created using SQLAlchemy orginal url is stored .


+ To shorten the link python random choices() method is used which will randomly pick string of length 3 using characters in A-Z , a-z , 0-9


+ Shorten link is also stored in database and visits variable (which will store when number of times you visited shorten url) to that url is set default to zero and will be incremented after user visits through shorten url. 

+ One can view database in /stats page .

 

## Installation
---
[(Back to top)](#list-of-contents)

Install  required packages using pip or any other method specified in requirement.txt.
pip3 intall -r requirement.txt


## Running

- submitting original link to shorten

![img](https://imgur.com/ifYEMlw.png)

- generating new url
![img](https://imgur.com/cHNjQxP.png)

- /stats page which stores original url , shorten url , number of visits to that url
![img](https://imgur.com/WxMEfbF.png)
