# MacOS Setup
## Virtual Environment
TurboSETI runs on python2. Many devices are instead running
 the latest version of python, python3. In order to get turboSETI 
 to work correctly, you must run its setup using python2. We can
 use a virtual environment to allow turboSETI to run with python2
 while still having python3 on our device.
#### Pipenv
Any program that allows you to make a python2 virtual environment
should work, however I have found pipenv to be the easiest to use
and so will provide instructions for it.
##### 
First, open up your terminal and type the following command to
install pipenv:
#####
```brew install pipenv```
#####
Next, we need to setup the virtual environment. We can do this by typing
the following command into terminal:
#####
```pipenv --two```
##### 
Note that the 'two' denotes python version 2. To enter the virtual
environment, we can type 
#####
```pipenv shell```
#####
Now that you are in the virtual environment, typing
```python --version```
should let you know that you are using python version 2.
Now we have to install the dependencies for turboSETI. Type
#####
```pip install cython numpy blimpy pandas```
#####
to install the required dependencies. Now our virtual 
environment is all set up for whenever we want to use turboSETI.
## TurboSETI
#### Setup
While in your python2 virtual environment shell, navigate 
to the folder where you have downloaded turboSETI. To make
sure you are in the right folder, type ```ls```. In the output,
there should be a file called ```setup.py```. Once you
are in the correct folder, type 
#####
```python setup.py install```
#####
