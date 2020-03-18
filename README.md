# x750
This is the safe shutdonw & reading Battery voltage and capacity script for x750


* https://geekworm.com
* https://geekworm.aliexpress.com
* https://www.amazon.com/shops/geekworm
* Email:support@geekworm.com

##1. Enabled I2C support on the Raspbia.
```shell
 sudo raspi-config
```
Select 5 Interfacing Options and then  P5 I2C - Enable/Disable automatic loading. A prompt will appear asking Would you like the ARM I2C interface to be enabled?, select "Yes" 

##2. Install I2C-tools software package.
```shell
 sudo apt-get install python-smbus 
 sudo apt-get install i2c-tools 
```
##3. Download the required script
```shell
 git clone https://github.com/geekworm-com/x750.git
 cd x750
 chmod +x x750.sh
```
##4. Install&run the script
```shell
sudo bash x750.sh
```
##5. Setting up the command to turn off X750 from software
```shell
 printf "%s\n" "alias x750off='sudo x750shutdown.sh'" >> ~/.bashrc
 sudo reboot
```
##6. Test the safe shutdown command
```shell
 ./x750off
```
#7. How to read the battery voltage and percentage?
```shell
 sudo phthon x750ups.py
```

#About Geekworm

Geekworm is specialize in open source hardware research and developemnt,we aim to provide high quality products with reasonable price, fast shipping as customer's requirement and intimate after-sales service.The recognition and trust of customers is the greatest inspiration to Geekworm.
