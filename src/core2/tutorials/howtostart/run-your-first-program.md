---
title: 'Run your first program'
platform_title: 'CORE2'
core2: true
autotoc: true
layout: layout.hbs
order: 1
---

# Run your first program #
## Preparing hardware ##

First, connect your CORE2 hardware to the WiFi gateway. For your convenience, you can choose the configuration that suits you best. 
Choose one of the following configurations to connect your CORE2 to the WiFi gateway:

### Option #1: ESP32 as a removable module to CORE2 ###
Choosing this option, you will be able to easily run CORE2 in a different configuration in the future (e.g. with Raspberry Pi Zero).


<div class="gallery gallery-6">

![1. Elements you need](/assets/img/howToStart/esp_removable-01.png "[1/6] You will need: 2 nuts, stand-off, 7x2 goldpin female header, 7x2 goldpin male header, CORE2 and ESP32 module")
![2. Place the male goldpin header](/assets/img/howToStart/esp_removable-02.png "[2/6] Place the 7x2 goldpin male header on the CORE2 hRPI connector]")
![3. Then solder it](/assets/img/howToStart/esp_removable-03.png "[3/6] Solder the 7x2 goldpin male header to the CORE2 hRPI connector")
![4. Solder the female header to the ESP](/assets/img/howToStart/esp_removable-04.png "[4/6] Solder the 7x2 goldpin female header to the ESP32")
![5. Put it all together](/assets/img/howToStart/esp_removable-05.png "[5/6] Use 2 nuts, and spacer to reliably connect CORE2 and ESP32 module")
![6. Done!](/assets/img/howToStart/esp_removable-06.png "[6/6] Well done! Now you are ready to connect your CORE2 to the Husarion cloud")

</div>


### Option #2: CORE2 + Raspberry Pi 2 or 3 ###

Follow these steps to assemble CORE2 with Raspberry Pi 2 (or Raspberry Pi 3). A Linux computer is useful if you need to run complex software on your connected device (e.g. ROS libraries, video processing etc.).

<div class="gallery gallery-6">

![1. Elements you need](/assets/img/howToStart/raspberry_Pi2-01.png "[1/6] You will need: 8 x nut, 4 x stand-off, 7x2 goldpin female header \(with long pins\), CORE2 and Raspberry Pi 2 computer")
![2. Place female goldpin header](/assets/img/howToStart/raspberry_Pi2-02.png "[2/6] Place 7x2 goldpin female header on the pins #1-14 of Raspberry Pi 2 male header") 
![3. Screw CORE2 to RaspberryPi2](/assets/img/howToStart/raspberry_Pi2-03.png "[3/6]  Use 8 x nut, and 4 x stand-off to reliably connect CORE2 and Raspberry Pi 2")
![4. Now it should look like this](/assets/img/howToStart/raspberry_Pi2-04.png "[4/6] Make sure that your CORE2 and Raspberry Pi 2 are joined together like on the picture")
![5. Solder header to the CORE2](/assets/img/howToStart/raspberry_Pi2-05.png "[5/6] Solder 7x2 goldpin female header to the CORE")
![6. Done!](/assets/img/howToStart/raspberry_Pi2-06.png "[6/6] Well done! Now you are ready to connect you CORE2 to the Husarion cloud")

</div>

Download and flash your SD card with Husarion RPi Image - instructions

1. Download image for Raspberry PI from [](https://files.husarion.com/rpi-image-stable.img).
2. Follow the official guide for writing an image to SD card - [](https://www.raspberrypi.org/documentation/installation/installing-images/).

## Power supply ##

Connect your CORE2 to a DC power supply. The power connector is a standard DC 5.5/2.1 (center-positive), and provides 6 to 16V output. You can use:

* DC adapter
* Li-poly/Li-ion packages - 2S or 3S (e.g. 18650 batteries)
* AA alkaline batteries (4-10 pieces)

## Connecting to the Cloud ##
Before you perform the next steps, install the hConfig mobile application on your smartphone or tablet:
* [Google Play](https://play.google.com/store/apps/details?id=com.husarion.configtool2&hl=en)
* [AppStore - comming soon](https://husarion.com)

You also need to register your own account on [Husarion Cloud](https://cloud.husarion.com).

Open the hConfig app on your smartphone and follow the wizard that will show you how to connect CORE2 to your Wi-Fi network and your Husarion cloud account. After you select the Wi-Fi network for your CORE2 in the hConfig app, you can proceed to the next steps.

hConfig app will ask you to add a new device. Open https://cloud.husarion.com in your browser and sign in

![image](/assets/img/howToStart/1_signin.png)

Click "Add new device"

![image](/assets/img/howToStart/2_addNewDevice.png)

Enter a name for you CORE2 powered device

![image](/assets/img/howToStart/3_enterName.png)

Scan QR code using your hConfig app

![image](/assets/img/howToStart/4_scanQr.png)

Well done! You just added your first device to the cloud!

![image](/assets/img/howToStart/5_devAdded.png)

## Writing your first program ##

Click "+" next to your device name ane sellect "IDE"

![image](/assets/img/howToStart/6_openWebIDE.png)

Click "Create" button to open new project wizard

![image](/assets/img/howToStart/7_createNewProj.png)

Select CORE2 board, version 1.0.0, HowToStart project template and enter name, eg. myFirstProject, and click "Create project" button

![image](/assets/img/howToStart/8_projSettings.png)

This is a web Integrated Development Enironment in which you can write a firmware for your device, and upload the firmware through the Internet

![image](/assets/img/howToStart/9_webIDEmain.png)

Click "<none>" next to "selected device" and select "myFirstDev" device.

![image](/assets/img/howToStart/10_webIDEselectDev.png)

Click a button with a "cloud with arrow" to upload new firmware to your device. Well done! now you can check how your first program works.

![image](/assets/img/howToStart/11_webIDEprogram.png)

In the previous step you have uploaded the firmware into your CORE2. Let's check how it works!<br/>

Go to https://cloud.husarion.com and click the myFirstDev's avatar. It's web user interface will start loading.

![image](/assets/img/howToStart/12_openDevUI.png)

After a while your device UI will appear. Now spend a few seconds playing with a dev's interface.

![image](/assets/img/howToStart/13_devUI.png)

## Share your device with friends ##
Husarion Cloud allows you to share your devices conntected to Husarion cloud with other people with just a few clicks.

Click "+" next to your device name at https://cloud.husarion.com and select "Share"

(/assets/img/howToStart/14_shareSelect.png)

Select "Share via Link" and click "Generate link". Now you can send this link to anybody you want to access your device.

(/assets/img/howToStart/15_shareDetails.png)

3. When you open generated link, you’ll see your device’s web UI.

(/assets/img/howToStart/16_shareUI.png)

Now you can share the link with anybody!
