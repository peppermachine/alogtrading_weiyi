# AlgoTrading
Algorithmic Trading Installation Guide

### System Requirements
Make sure your system meets these requirements:
  - Operating system: MacOS 10.7 10.8 10.9 (it has been tested successfully on these)
  - RAM: 2GB.
  - Disk space: 2GB

### Step 1: Install Command Line Tools
  - Open terminal, type “xcode-select --install” in terminal (without quotes)
  - A pop-up windows will appear asking you about install tools, choose install tools, wait install to finish
  
### Step 2: Install Homebrew

  ```
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  brew tap samueljohn/python
  brew tap homebrew/science
  ```

### Step 3: Install gcc and its libraries

  ```
  brew install gcc
  ```

### Step 4: Install Python and its modules
    
  ```
  brew install python
  
  pip install virtualenv
  pip install nose
  pip install pyparsing
  pip install python-dateutil
  
  pip install numpy
  pip install scipy
  pip install matplotlib
  
  pip install pandas
  pip install scikits.statsmodels
  pip install scikit-learn
  pip install QSTK
  ```

### Step 5: Clone AlgoTrading and overwrite QSTK package

  ```
  git clone https://github.com/weiyialanchen/AlgoTrading.git
  cp -r  AlgoTrading/* /usr/local/lib/python2.7/site-packages/QSTK/
  ```

### Step 6: Set up alias to work directory. Note that your working directory is /usr/local/lib/python2.7/site-packages/QSTK/, to make alias

  ```
  vi ~/.bash_profile
  ```

  Add following line to the file (press 'i' to insert, ':wq' to write and quit)

  ```
  alias AlgoTrading='cd /usr/local/lib/python2.7/site-packages/QSTK/'
  ```

  Next time you want to go to the working folder, just run

  ```
  AlgoTrading
  ```