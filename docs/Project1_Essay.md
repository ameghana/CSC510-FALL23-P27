**Introduction**:

Slash is an open-source web framework that makes use of FastAPI to scrape the best deals from various e-commerce websites such as eBay, Amazon, BestBuy, Costco, Target, and Walmart. Slash makes it easy for users to filter and organize search results and also provides visualization in the form of charts and graphs.

**Steps and difficulties while running the project in Windows**:

_**Python installation for backend**_:

Since we need the python 3.9 version, we need to setup a virtual environment(venv). Following are the steps to setup venv:

1)Install python 3.9   #installing python

2)py --list   #to view all versions on python present

3)py -3.9 -m venv {virtual environment name}    #creating a virtual environment

4)cd {virtual environment name}    #navigating to virtual environment

5)Scripts\activate 	         #activating virtual environment

_**Once venv setup is done, we will start cloning the repository using the following commands**_
6)git clone {repolink}       #cloning a repository

7)cd slash         	#navigating to slash folder

8)pip install -r requirements.txt    #to install dependencies and libraries

      **ERROR**:environment error due to denied access.       
        So, we will use pip3 to install the requirements and the below command is used.            
        pip3 install -r requirements.txt
        
9)cd src    #navigating to src folder

10)python main.py   #to run the backend

_**Node installation for front-end**_
11)Install node 18.17.1     #installing older version of node.js 

12)cd client    #navigating to client directory

13)npm install     #to install all npm dependencies

           Here we are getting ERROR: upstream dependency conflict, so to resolve this, the below command is executed
            	npm install --force
             
14)npm run start

	Faced an ERROR: Digital envelope routines unsupported, so we add the below lines to package.json in the client directory.
            	"scripts": {
            	 "start": "react-scripts --openssl-legacy-provider start",
            	 "build": "react-scripts --openssl-legacy-provider build",
               }

**Code Analysis on higher level**

To develop the backend of the project, python was used. Initially to scrape the data from e-commerce websites and to parse the data, BeautifulSoup library was imported. For the API calls, when an item related to a particular website is called, FastAPI was implemented. FastAPI is a modern robust web framework to build APIs with python. It is also compatible with node.js, which was used to develop the front-end of the project. For production using FastAPI, an ASGI server was necessary. Hence, Uvicorn is installed. <br/>
Front-end of the project was implemented using node.js specifically coded in React.js. Material UI which is an open source React component library was used to design components like navigation bar, app bar, buttons, select and tables. To display graphical data in Graphs page, chart.js, a free java-script library was implemented. Also to establish HTTP requests, axios library is used. It is used to perform CRUD operations and communicate with the backend.



