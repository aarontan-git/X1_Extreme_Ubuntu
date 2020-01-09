# Installation Guide

Before installation:
- Update BIOS through Lenovo Vantage App
- Graphics: Discrete mode

press F1 to enter BIOS, F12 to enter boot menu

I followed the following link for general installation:

https://bauklimatik-dresden.de/privat/nicolai/index.html?https&&&bauklimatik-dresden.de/privat/nicolai/html/en/lenovo_x1_extreme_ubuntu1804.html

I did the partionining based on what's mentioned in this post:

https://askubuntu.com/questions/726972/dual-boot-windows-10-and-linux-ubuntu-on-separate-hard-drives?fbclid=IwAR3yOPaAmhdyi9DpglQblluWYORU3ga7ElPkQZeaNZfjhuzRDuRIQcSqghI

# Wifi Issue
Currently the wifi doesnt work because the wifi card within the X1E Gen 2 needs Kernel 5.1 and above whereas Ubuntu 16.04 is on Kernel 4.15

https://www.phoronix.com/scan.php?page=news_item&px=Intel-WiFi-6-AX200-Cyclone-Peak

https://www.intel.com/content/www/us/en/support/articles/000005511/network-and-i-o/wireless-networking.html

To fix this issue, I ordered the following wifi card and it fixed the wifi problem:

https://www.amazon.ca/gp/product/B07G42J6KQ/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1


# Nvidia graphics card

If you are following Nicolaie's way of installing nvidia drivers, your comptuer will not be able to boot. You will fix it by doing the method in the following link:
 
 https://askubuntu.com/questions/352093/need-to-deactivate-nvidia-driver-from-recovery-mode-or-using-ubuntu-12-04-instal/352099

and the proper way to install nvidia driver should be through tensorflow

 https://www.tensorflow.org/install/gpu

To be able to switch between Nvidia and Intel:

 https://askubuntu.com/questions/412452/getting-hybrid-graphics-to-work-nvidia-prime-gt650m


## To Connect to UofT Wifi
Click on the wifi icon and click edit connections. Remove all previous uoft connection you used before. There might be one or more.

Then attempt to connect to UofT network.

It will give you a menu to fill out.

The EAP method should be set to "PEAP" from drop down menu

Phase 2 authentication should be "MSHAPV2"

no CA certificate

no anonymous identity

no user certificate

Identity is UTORid password is "you password for your UTORID"

## Reinstall Ubuntu
- use gparted to combine partitions
- swap should be turned off before moving

## problem with pip

'''
hash -d pip
'''