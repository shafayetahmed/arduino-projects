Hello there, today we are going to look at how you can deploy a thing on the tuya IoT Platform. I am going to show you the step-by-step process to make a smart light on your home using the Tuya IoT platform. By the end of this article, you will be able to make a smart light at your home.

To start making this you will need:

Arduino UNO
Node MCU development kit (ESP8266)
A relay module
Male to female Jumper wires

At first, create an account on Tuya’s platform. Then you need to create a product. To create a product go to iot.tuya.com and log in with your credentials. Then go to products > lighting and select the option “light source” as we are making a smart light.

Then select the custom solution option as we are making a custom one, then name your product and the product model as your wish then set the protocol to wifi and power type to standard power consumption, and then hit create.

Now you don’t need to change anything here except in the device panel. Just select any panel from the given presets or you can also make a custom one.

Now copy the product id (PID) and send that to Tuya’s developer team Dev@tuya.com along with the Gmail associated with your account. then after some time, you will get a reply with your token id. Copy the token id and head over to pms.tuya.com and log in with your credentials. then from the left sidebar go to Production Management > Work Order Management > Activation Code Verification. Then paste your activation code and confirm that.

As we are not using any tuya’s module. We need to flush esp8266 with tuya’s firmware. For that please download this software called TYDA. Download link

After downloading the software, open that and log in with your account credentials. Then please make sure that the value is the same as shown in the below image.

Then connect your node MCU development board with your computer and enter the token, checkmark the firmware download box, and set the work station to Burning authorization, and then hit run. If there is no issue then the process will finish successfully after some time.

After flushing the esp8266 with tuya’s firmware successfully close the TYDA software and open Arduino Ide to program the Arduino board. Make sure to install a library called Tuya_WiFi_MCU_SDK. After installing the library connect your Arduino Uno with the computer.

Then go to file > Examples > Tuya_WiFi_MCU_SDK > start and then please change the default product id (PID) with your product id (PID). Then upload the program to the Arduino board. (Note: Please select the board type, port number properly, otherwise you will receive an error)

After uploading the code successfully to the Arduino, it’s time to connect all the components together, for that please follow the below circuit diagram.

After the wiring is done, download the Tuya smart app from the play store and log in with your credentials, and then, please connect pin 7 of the Arduino board to the ground pin for three-four seconds to put the device into the pairing mode.

Then start the device adding process to the app. After some time the device will be added, and you will be able to control the light bulb using your smartphone.


