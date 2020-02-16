# Evil Twin

Learn how to set up a fake authentication web page on a fake WiFi network.

Read the comments in these two files to get a better understanding on how all of it works:

* [index.php](https://github.com/ivan-sincek/evil-twin/blob/master/src/evil-twin/index.php)
* [MyPortal.php](https://github.com/ivan-sincek/evil-twin/blob/master/src/evil-twin/MyPortal.php)

You can modify and expand this project to your liking. You have everything that needs to get you started.

You can make it look like Starbucks, Facebook or something else entirely.

Tested on WiFi Pineapple NANO with firmware v2.6.2 and modules Evil Portal v3.2 and Cabinet v1.1.

Additional set up and testing was done on Windows 10 Enterprise OS (64 bit).

Made for educational purposes. I hope it will help!

## How to Set up a WiFi Pineapple NANO

Follow the instructions below:

1. [Setup Basics](https://docs.hak5.org/hc/en-us/articles/360010555313-Setup-Basics)

2. [Windows Setup](https://docs.hak5.org/hc/en-us/articles/360010471434-WiFi-Pineapple-NANO-Windows-Setup)

3. [Install the Network Driver](https://www.techspot.com/drivers/driver/file/information/17792/)

## How to Run

In the WiFi Pineapple's dashboard go to `Modules -> Manage Modules -> Get Modules from Hak5 Community Repositories` and install modules `Evil Portal` and `Cabinet` (preferably on an SD card storage).

Connect to your WiFi Pineapple (preferably with [FileZilla Client](https://filezilla-project.org/download.php?type=client)) and copy all the content from ['\\src\\'](https://github.com/ivan-sincek/evil-twin/tree/master/src) to `/sd/portals/` (preferred) or `/root/portals/`.

In the WiFi Pineapple's dashboard go to `Networking` and change your Open SSID name to a desired one, then, connect your fake WiFi network to a real working WiFi network in the WiFi Client Mode section in order to tunnel network traffic back and forth from the Internet.

In the WiFi Pineapple's dashboard go to `Modules -> Evil Portal` and activate the `evil-twin` portal, then, start the Captive Portal.

In the WiFi Pineapple's dashboard go to `Modules -> Cabinet`, navigate to `/sd/logs/` or `/root/logs/` and click on "Edit" for `evil_twin.log` to view its content or download the file trough FileZilla Client.

## Images

![Landing Page Mobile](https://github.com/ivan-sincek/evil-twin/blob/master/img/landing_page_mobile.jpg)

![Landing Page PC](https://github.com/ivan-sincek/evil-twin/blob/master/img/landing_page_pc.jpg)

![Log File](https://github.com/ivan-sincek/evil-twin/blob/master/img/log.jpg)