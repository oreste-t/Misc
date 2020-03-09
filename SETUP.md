# MacOS TurboSETI Setup
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

First, open up your terminal and type the following command to
install pipenv:

```brew install pipenv```

Next, we need to setup the virtual environment. We can do this by typing
the following command into terminal:

```pipenv --two```

Note that the 'two' denotes python version 2. To enter the virtual
environment, we can type 

```pipenv shell```

Now that you are in the virtual environment, typing
```python --version```
should let you know that you are using python version 2.
Now we have to install the dependencies for turboSETI. Type

```pip install cython numpy blimpy pandas```

to install the required dependencies. Now our virtual 
environment is all set up for whenever we want to use turboSETI.
## TurboSETI
The first thing you'll want to do is clone the turboSETI repository
from github. You can do this by navigating to
 
[https://github.com/UCBerkeleySETI/turbo_seti](https://github.com/UCBerkeleySETI/turbo_seti)

and hitting clone or download. Copy the link it gives you then go back to 
terminal. Navigate to a directory you want to clone into, then type

```git clone https://github.com/UCBerkeleySETI/turbo_seti.git```

Enter the folder that gets created, then make sure ```setup.py``` is
in there. You will need it for the next part.
#### Setup
While in your python2 virtual environment shell, navigate 
to the folder where you have downloaded turboSETI. To make
sure you are in the right folder, type ```ls```. In the output,
there should be a file called ```setup.py```. Once you
are in the correct folder, type 

```python setup.py install```

Installation is now complete. Any time you want to use turboSETI from 
terminal, simply boot up your virtual environment with ```pipenv shell```,
navigate to the folder where your argument files are (or don't if you'd rather type out their path)
and run the command as stated in the repository's README. You can exit
the shell by typing ```exit```.

