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

Once venv setup is done, we will start cloning the repository using the following commands

6)git clone {repolink}       #cloning a repository

7)cd slash         	#navigating to slash folder

8)pip install -r requirements.txt    #to install dependencies and libraries

      **ERROR**:environment error due to denied access. 
      
        So, we will use pip3 to install the requirements and the below command is used.
               
        pip3 install -r requirements.txt

9)cd src    #navigating to src folder

10)python main.py   #to run the backend
