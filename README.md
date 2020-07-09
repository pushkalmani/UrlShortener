# URL Shortener Web-Application Using Python's web framework: Flask

### List of contents

- [Introduction](#introduction)
- [Working](#working)
- [Installation](#installation)
- [Running](#running)


## Introduction
---
[(Back to top)](#list-of-contents)

URL shortener is a web app created by using flask ( python’s web framework ). The purpose of this app is to convert long complex url's into simpler and short URL and store the required information like URL mappings and number of visits to the URLs in the sqlite database. The website has been designed for small community usage and hence the algorithm used is simplistic enough. The algorithm is chosen in such a way that it can be scaled easily for public usage. More details can be found in the sections below.


## Working
---
[(Back to top)](#list-of-contents)

The steps involved in creating the website.

+ The backend has been developed in Flask and frontend involves the usage of HTML and CSS.

+ The URL shortening algorithm consists of a custom algorithm developed for small community usage. It involves the three characters concatenated at the end of the base URL. These three characters are chosen from a string of digits and ascii characters. The random character picker is created using python's *random.choices()* function. Since it is intended for small community usage hence only three characters are used in the end. But for public usage the number of combination of three characters can wipe off quickly. To handle this more characters can be taken or another algorithm can be used for scaling the application. Below is a code snippet to implement the algorithm described above.

```python
from random import choices
def generate_short_link(self):
        characters = string.digits + string.ascii_letters
        short_url = ''.join(choices(characters, k=3))
```  

+ Sqlite database is being used to store the mappings of the Long URL to the shortened URL. *FlaskSqlAlchemy* an ORM tool that provides methods to perform CRUD operations without having to write raw SQL statements is used to write and read the data from the sqlite database.

+ Using Flask-SQLAlchemy, URL shortener will be able to redirect links and keep stats on the number of times each link was visited.

+ Users can have a look at the stats or the data stored in the database using /stats route in the website. 

 
## Installation
---
[(Back to top)](#list-of-contents)

- Install  required packages using pip or any other method specified in requirement.txt :
  - pip3 intall -r requirement.txt
- Run the application using :
  - flask run


## Running

- submitting original link to shorten

![img](https://imgur.com/ifYEMlw.png)

- generating new url
![img](https://imgur.com/cHNjQxP.png)

- /stats page which stores original url , shorten url , number of visits to that url
![img](https://imgur.com/WxMEfbF.png)