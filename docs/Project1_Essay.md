**Introduction**:

Slash is an open-source web framework that makes use of FastAPI to scrape the best deals from various e-commerce websites such as eBay, Amazon, BestBuy, Costco, Target, and Walmart. Slash makes it easy for users to filter and organize search results and also provides visualization in the form of charts and graphs.

**Steps and difficulties while running the project**:

_**Python installation for backend**_:

Since we need the python 3.9 version, we need to setup a virtual environment(venv). Following are the steps to setup venv:

1)Install python 3.9   #installing python

2)py --list   #to view all versions on python present

3)py -3.9 -m venv {virtual environment name}    #creating a virtual environment

4)cd {virtual environment name}    #navigating to virtual environment

5)Scripts\activate 	         #activating virtual environment

_**Python installation for backend(MacOS)**_:

Since we need the python 3.9 version,
1)Install Homebrew:

	/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2)Now install PyEnv to switch between different version of python

 	brew install pyenv

3)Now to install required version of python using PyEnv, run this command:

	pyenv install 3.9.2


4)To SetUp MacOS path for pyEnv in ZSH or OhMyZSH

	echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
	echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc

5)Then Run this:

	echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init --path)"\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
	pyenv global 3.9.2
	pyenv versions

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

      	   We may encounter this issue in MacOS:
	  	ImportError: cannot import name 'NotRequired' from 'typing_extensions' 		(/Users/sravyakaranam/.pyenv/versions/3.9.2/lib/python3.9/site-packages/typing_extensions.py)

	To resolve that, We have to execute: pip install typing_extensions==4.7.1 –upgrade
             
14)npm run start

	Faced an ERROR: Digital envelope routines unsupported, so we add the below lines to package.json in the client directory.
            	"scripts": {
            	 "start": "react-scripts --openssl-legacy-provider start",
            	 "build": "react-scripts --openssl-legacy-provider build",
               }
	       
**Learnings**:

This is an interesting project, and we were able to learn new/valuable things. The following are our learnings and these are helpful to improve and add new features to the existing project. 
**Importance of Virtual environment**: Setting up a virtual environment was an essential part of this project. Since the software versions used in the project are different from what we have, having a virtual environment is helpful. This virtual environment will not disturb the existing softwares in the system.
**Evaluation of Rubrics**: As we evaluated the project based on each metric, we have a good understanding of the code and workflow of the project. 
**Importance of Good repo**: The repo of the project is very understandable, clear and simple. The document clearly explains the problem and solution by providing all the steps. We will maintain the same format for repo.
**Test-cases**: In every project, all test-cases should be considered and testing has to be done accordingly. We’ve noticed that some of the test-cases are not validated, and proper error messages are not provided. We are going to include all the testcases, and provide user understandable error messages in our project 2 implementation.

**Code Analysis on higher level**

To develop the backend of the project, python was used. Initially to scrape the data from e-commerce websites and to parse the data, BeautifulSoup library was imported. For the API calls, when an item related to a particular website is called, FastAPI was implemented. FastAPI is a modern robust web framework to build APIs with python. It is also compatible with node.js, which was used to develop the front-end of the project. For production using FastAPI, an ASGI server was necessary. Hence, Uvicorn is installed. <br/>
Front-end of the project was implemented using node.js specifically coded in React.js. Material UI which is an open source React component library was used to design components like navigation bar, app bar, buttons, select and tables. To display graphical data in Graphs page, chart.js, a free java-script library was implemented. Also to establish HTTP requests, axios library is used. It is used to perform CRUD operations and communicate with the backend.



