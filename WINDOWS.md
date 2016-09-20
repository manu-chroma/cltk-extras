# Installation Guide : Setting up CLTK in WSL, Experimental Support for Bash On Ubuntu On Windows

**Step 0: [Settting up WSL on Windows 10](http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)**

### Installing required packages from ``apt-get``
``` bash
sudo apt update
sudo apt install git
sudo apt-get install python-setuptools 
sudo apt install python-virtualenv
```

There are two ways to install CLTK using pip
### 1. Installing Globally
```
[sudo] pip3 install cltk
```
### 2. Installing in a virtual environement
  - Creating environement  
``` bash
virtualenv -p python3 venv
```
  - Activating environment and installing CLTK
``` bash
source venv/bin/activate
pip3 install cltk
```
  - Deactivating environement 
``` bash
deactivate
```

**NOTE 1:** There are rendering issues with unicode text in the Bash Terminal. Fonts like ``SimSub-ExtB`` and ``Courier New`` render majority of the [Unicode text](https://www.cl.cam.ac.uk/%7Emgk25/ucs/examples/UTF-8-demo.txt) fine. Lot's of other fonts such as ``Consolas`` and ``Lucida Console`` don't.
Try experimenting with different fonts in the setting, see what works best for you.
A better way, for now, would be to use [ConEmu Windows Terminal](https://conemu.github.io/) which renderd Unicode text much better.  
  
**NOTE 2:** This support for Windows is currently experimental, since the platform is still young. 
Also, contributing to CLTK on Windows would bring unecessary technical overhead, that's why development on Windows is strictly discouraged for the time being. 
