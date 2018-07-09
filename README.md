````
#############
Parte 1
sudo apt update
sudo apt -y upgrade
sudo apt install -y mailutils
sudo apt install -y python3 python3-pip
export LC_ALL=C
sudo pip3 install --upgrade pip
sudo pip3 install --upgrade setuptools
sudo pip3 install pandas bs4 jupyter selenium

#############
Parte 2
sudo apt install -y libxss1 libappindicator1 libindicator7
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome*.deb
sudo apt install -y -f

#############
Parte 3
sudo apt install -y unzip
curl -sS chromedriver.storage.googleapis.com/LATEST_RELEASE
	-> Ultima version, reemplazar ultima version en 2.4
sudo wget https://chromedriver.storage.googleapis.com/2.40/chromedriver_linux64.zip
sudo unzip chromedriver_linux64.zip
sudo chmod +x chromedriver
sudo mv -f chromedriver /usr/local/bin/chromedriver
sudo apt install -y xvfb
sudo pip3 install pyvirtualdisplay

#############
Parte 4
sudo nano test.py
////////////////////////////////////////
from pyvirtualdisplay import Display
from selenium import webdriver

display = Display(visible=0, size=(800, 600))
display.start()

options = webdriver.ChromeOptions()
options.add_argument('--no-sandbox')

driver = webdriver.Chrome(chrome_options=options)
driver.get('http://nytimes.com')
print(driver.title)
////////////////////////////////////////

sudo apt-get install apache2 -y
sudo nano /etc/apache2/ports.conf
-> Listen 8080
sudo service apache2 restart
sudo apt-get install php libapache2-mod-php
sudo systemctl restart apache2

sudo nano index.php
MINUMUN

exec('pkill -9 Xvfb');
exec('pkill -9 selenium');
exec('pkill -9 python');
exec('pkill -9 python3');
exec('pkill -9 chrome');

from pyvirtualdisplay import Display
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.common.exceptions import TimeoutException
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.desired_capabilities import DesiredCapabilities

import sys
import time

options = webdriver.ChromeOptions()
options.add_argument('--no-sandbox')
options.set_headless(headless=True)
driver = webdriver.Chrome(chrome_options=options)


```
