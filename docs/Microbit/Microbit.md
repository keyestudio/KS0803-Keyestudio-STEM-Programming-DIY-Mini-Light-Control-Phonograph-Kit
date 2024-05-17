# Micro:bit Phonograph Projects

## 1. Projects

1. Photoresistor: Light Detector

Photoresistor

![img](img/96c8270974492cfeccf977e05847c900.jpg)

Photoresistor, also known as photoelectric sensor, is a sensor that converts optical signals into electrical ones (voltage, current, resistance, etc.) through photoelectric devices. In the circuit, there is a resistor whose resistance value depends on light intensity.

The photoresistor enters the circuit in series, and we add an appropriate voltage. When there is no light, the resistance is infinity, so the circuit is close to open. When there is light, its resistance reduces and the current increases. If the light is bright enough, it is equivalent to a short circuit.

Herein, we write code on the Microbit to read the value of the photoresistor.

Principle Diagram

Light hits the photoresistor. The harder the light is, the smaller the resistance value will be, and the greater the voltage (VCC passing through the resistor) will be.

![img](img/e08561c3a64ee7ac18d37f4c4302f932.png)

------

Wiring Diagram

![img](img/d8b75c39f3edcf490ff23bf5242e06bf.png)

------

Parameters

- Voltage: 3~5V

- Current: 0.2mA
- Power: 1mW
- Spectral peak: 540nm
- Bright resistance (10lux): 5~10KR
- Dark resistance: 0.5MR

------
Test Code 1

- Initialize the serial port.

  ![img](img/3caf2f252f3216257d296e33ebd28a93.png)

  ![img](img/786d6a082a609792dc652bce3f4241d5.png)

- Read the analog value of pin.

  ![img](img/027677c85b030b3216d303a1b125c112.png)

- Set pin to P1

  ![img](img/a3464f242eea500519259f8040ac896a.png)

- Complete code

  ![img](img/309fa6df8cbe74c4c67eda5ad65ae3aa.png)

------

Test Result 1

A hole is reserved on the phonograph and the photoresistor is under it, as shown below:

![img](img/8393d254d21c9e3b8c02902bd5b60ab9.png)

------

Move the tone arm above the hole, and open the CoolTerm serial monitor to set baud rate.

![img](img/53a805c8df0c01aadacc25a115e56234.png)

Set the COM port (the port number varies from devices).

![img](img/a23aee46d22e265f08e22f53dccac2c2.png)

![img](img/09d440c2f83b190eeef74fd9fbb8ced5.png)

![img](img/359729de13f9b2db3062355a68631cdc.png)

------

If we move the tone arm away, 

![img](img/3ea894f3ec6bad4bfe9888c6f75bcb7b.png)

the serial monitor will print analog values of the photoresistor.

![img](img/84d2cf2ccafd7f7d3462810316335ee3.png)

------

Test Code 2

If no light is detected, light up RGB dot matrix; when there is light, turn off RGB dot matrix.

- Define a variable to store the detected light values.

![img](img/acc1bb28ec668e706fb23bad33df6c3e.png)

![img](img/76d147ed6e0696df3444a5e288120b93.png)

- Assign the detected light value to the variable and print it.

  ![img](img/ac931decc1138c161b68e915f0d0649d.png)

- Create a logic code.

  ![img](img/5d2c00dc884821641308a48cfc60ab45.png)

  ![img](img/4071ad13ca9156384db94de48ff5be92.png)

- Determine whether the value is lower than or equals 10.

  ![img](img/01c6a659479eedd9bc6d006905ccdb7a.png)

  ![img](img/36bc184dfcf765669f69a87af61cd7bb.png)

- Complete code

  ![img](img/8e1730d7e934fe4e5acd5bd7a069afa9.png)

------

Test Result 2

- Put the tone arm above the hole position, and the RGB dot matrix will light up.

  ![img](img/6b9af4004672c8189e90d38395b64f87.png)

- Remove the arm and RGB dot matrix will turn off.

  ![img](img/d636383f337bbec86a1190568f6ddcbd.png)

------

2. Power Amplifier: Music Box

Power Amplifier

The power amplifier mainly consists of a potentiometer, a speaker, and an audio amplifier chip. This module amplifies the small audio signals about 8.5 times, and plays audio through its built-in speaker. Therefore, it can be used to play music or as an external amplifier for some music players.

![img](img/d462bd9e090272cad154dc8e041bd869.jpg)

Principle Diagram

![img](img/80765898fa3afe1f45fad42a07e1919a.png)

------

Wiring Diagram

![img](img/d8b75c39f3edcf490ff23bf5242e06bf.png)

------

Test Code 1

- Find **music**

  ![img](img/9b7516ee3a49e3fee0822611c833ac24.png)

- Set melody.

  ![img](img/195032660231e8592c8a3cf695c2adee.png)

- Complete code

  ![img](img/6a5cae90ef575b75fcfa46ee127ea8db.png)

Test Result 1

The amplifier will play the 8 basic tones. 

Rotate the potentiometer on the module to adjust the volume.

<span style="color:red">**ATTENTION: The louder the volume is, the more the current will be consumed, so it may suffer from a power shortage. Thereby, the Microbit hard disk will fail to appear on PC due to its disabled USB port, so then codes are unable to be uploaded. Solution: When uploading code, adjust the volume to its minimum.**</span>

![img](img/28ded1e8523e76435bd31a4b3eed0422.png)

Test Code 2

Find a play block in music.

![img](img/dac3574360654fbd60ffc60e9f07c64d.png)

![img](img/8cf633623c9bd8b0793400a8b692ef1d.png)

Test Result 2

The module plays the set music.

------

3. Light Control Phonograph

Introduction

![img](img/d83fdd7f1ec60e744c58c4c95c92c1ef.png)

In this project, we try to simulate a real phonograph: when the tone arm is placed on the turntable, it plays music; When we remove it, it finishes the current music and then stops singing.

Test Code

- Define a variable to store the detected light value.

  ![img](img/acc1bb28ec668e706fb23bad33df6c3e.png)

  ![img](img/76d147ed6e0696df3444a5e288120b93.png)

- Assign the detected light value to the variable and print it.

  ![img](img/ac931decc1138c161b68e915f0d0649d.png)

- Create a logic code.

  ![img](img/5d2c00dc884821641308a48cfc60ab45.png)

- Determine whether the value is less than or equals 10.

  ![img](img/882666d24084603ffcd9ac668c059859.png)

- If the value is greater than 10, turn off the RGB dot matrix and the music. If it is less than 10, turn on the RGB dot matrix and play music.

  ![img](img/8f9629e0f1bd9acce5d5db9d72dde8f4.png)

  <span style="color:red">**ATTENTION: The louder the volume is, the more the current will be consumed, so it may suffer from a power shortage. Thereby, the Microbit hard disk will fail to appear on PC due to its disabled USB port, so then codes are unable to be uploaded. Solution: When uploading code, adjust the volume to its minimum.**</span>

Test Result

Put the tone arm above the hole position, and it starts to play music with RBG lighting up. Remove the arm, and the music and RGB dot matrix both turn off.

![img](img/6b9af4004672c8189e90d38395b64f87.png)

------

4. Button Control Phonograph

![img](img/ca2deada03ca62874731045f7719e91f.png)

There are two button (A and B) on the board. Herein, we utilize these buttons to have a switchover of songs: press A for the previous song with a left arrow showing on the dot matrix; press B for the next song with a right arrow showing on the dot matrix.

Test Code

- Add a button input block.

  ![img](img/fd2ce81b5c3c69b08136f855ef241edc.png)

- Show “<” when A is pressed; show “>” when B is pressed.

  ![img](img/a9c4bae1ed5fa891481d4dea7be0acc9.png)

- Define two variables **”button_value”** and **”play“**.

  ![img](img/10a9e1ba12b014c442ba69bc5111c2ac.png)

  ![img](img/cd719c1a3f3363ff4af2712a36ae147d.png)

  ![img](img/4f9305a4f3b95e9f9a551d79aa8f4490.png)

- We have enrolled four song numbered as 0, 1, 2 and 3. Variable **”button_value”** stores the song number.

  1. To ensure button_value is within 0~3, we set button_value to 0 when it is less than 1, and set it to 3 when it is greater than 2. 

  2. When we press button A/B, we set **“play”** to 1 to play music.


- Press button A and button_value-1

  ![img](img/8276ab2bc80b53500c6dce34dd0c082f.png)

- Press button B and button_value+1

  ![img](img/2adaa86717228c49eb1ab30a37c61fb1.png)

  ![img](img/16af051b9fc2c6d5884d4803a5492b72.png)

- Read the value of **”button_value”** to determine which song to play. After finishing a song, set **play** to 0 to pause.

  ![img](img/1bc67e96fea9aafdcd742492a03fca60.png)

-  Complete code

  ![img](img/200d49dfc14e198449714918dfc8c16c.png)

   <span style="color:red">**ATTENTION: The louder the volume is, the more the current will be consumed, so it may suffer from a power shortage. Thereby, the Microbit hard disk will fail to appear on PC due to its disabled USB port, so then codes are unable to be uploaded. Solution: When uploading code, adjust the volume to its minimum.**</span>

Test Result

-  Music is being played:

  ![img](img/5cea9e7e7a3b442df872b2d12a277a20.png)

-  Pause:

  ![img](img/b89607df2b5aa68a5bee27850310d72a.png)

-  The next song:

  ![img](img/0635c9903c6d999a382dd488f49d52e9.png)

-  The previous song:

  ![img](img/ff91d23fd4deaf4d55179939391c8575.png)

------

## 2. Troubleshooting

2.1  Code fails to download to Micro:bit

Problem

Recently, many users encounter the issue that Micro:bit board doesn’t respond when download code.

If the way you operate is correct, maybe you accidentally press the reset button and enter the Maintenance mode or the firmware is lost due to mis-operation.

Plug in Micro:bit board, the “MAINTENANCE” drive appears, which means the program can’t be downloaded.

![img](img/fbf34cde50ffc6968bcd6c536198d930.png)

Solution

1. Download the **hex file** from this page to your computer.

	Down load the latest micro:bit firmware-0255: https://www.microbit.org/get-started/user-guide/firmware/ 
	If you do not want to download from this website, we also provide it in our tutorial.

2. After the latest firmware is downloaded, then drag it into the “MAINTENANCE” to make Micro:bit back to normal mode.

![img](img/245608a56fcc099ff871d1dc5154dfa0.png)

Avoid to Enter “MAINTENANCE”

1. Make sure the Reset button is **not** pressed when plugging the board by USB cable.

      ![img](img/079b3cca9e73d19f3a2dc1ab05e62078.png)
      
2. Don't unplug the cable suddenly during downloading micro:bit program, otherwise, the firmware will be lost and micro:bit will enter “MAINTENANCE” mode.
3. In the experiment, wrong wiring also cause a short circuit or firmware lost.

------

2.2 Troubleshooting-Download with WebUSB

Having trouble pairing the Micro: bit with WebUSB (/ device/usb/webusb)?

Step 1: Check cable

Make sure that your micro:bit is connected to your computer with a micro USB cable. You should see a **MICROBIT** drive appear in Windows Explorer when it’s connected.

![img](img/14372e65bfb53fed3fb87034b187ad18.png)

**If you can see the MICROBIT, please go to step 2**.

If you can’t:

- Make sure that the USB cable is working. Does the cable works on another computer? If not, find a different cable to use. Some cables may only provide a power connection and don’t actually transfer data.
- Try another USB port on your computer. 
- Is the cable good but you still can’t see the **MICROBIT** drive? Hmm, you might have a problem with your micro:bit. 
- Try the additional steps described in the [falut finding](https://support.microbit.org/support/solutions/articles/19000024000-fault-finding-with-a-micro-bit) at microbit.org.
- If this doesn’t help, you can create a [support ticket](https://support.microbit.org/support/tickets/new) to notify the Micro:bit Foundation of the problem. If you do so, **skip the rest of these steps**.

Step 2: Check firmware version

It’s possible that the firmware version on the micro:bit needs an update. Let’s check:

1. Go to the **MICROBIT** drive.
2. Open the **DETAILS.TXT** file.

![img](img/cc6c8b10eddfc36a096557a63a5fadfa.png)

3. Look for the version number. It should say **Version: ...**

	![img](img/6448d964b5ab226f4875e6ba07dc93a9.png)

	Or **Interface Version: ...**

	![img](img/abfa01737de5a6b6902550462da28fbd.png)

	If the version is **0234**, **0241**, **0243**, you need to update the [firmware](https://makecode.microbit.org/device/firmware) on your micro:bit. Go to **Step 3** and follow the upgrade instructions.

	If the version is **0249**, **0250** or higher, you have the right firmware, just go to **step 4**.

Step 3: Update firmware

1. Put your micro:bit into **MAINTENANCE Mode**. 

	To do this, please unplug the USB cable from the micro:bit and then re-connect the USB cable after pressing and holding the reset button. Once you insert the cable, you can release the reset button. You should now see **MAINTENANCE** instead of the **MICROBIT** drive. Also, a yellow LED indicator will stay on. 

![img](img/0486c9f06d1ec1e96a9bfc1cbd311a76.png)

2. Download firmware .hex file: <https://microbit.org/guide/firmware/>
3. Drag the file into the **MAINTENANCE** drive.
4. The yellow LED will flash while the HEX file is copying. After that, the LED will go off and the micro:bit resets. The **MAINTENANCE** drive now changes to **MICROBIT**.
5. The upgrade is complete! You can open the **DETAILS.TXT** file to check the firmware version that matches the one of the **HEX** file you copied.

If you want to know more about connecting the board, MAINTENANCE Mode, and upgrading the firmware, please refer to [Firmware guide](https://microbit.org/guide/firmware/).

Step 4: Check version of Browser

WebUSB may require you to update your browser. 

Check that your browser version matches one of these: **Android**, **Chrome OS**, **Linux**, **macOS** and **Windows 10 Chrome 65+**.

Step 5: Pair device

Once you’ve updated the firmware, open the **Chrome Browser**, go to the editor and click on **Pair Device** in settings. 

See [WebUSB](https://microbit.org/get-started/user-guide/web-usb/) (/ device / usb / webusb) for pairing instructions.

------

## 3. Resource

Keyestudio Official:

[https://www.keyestudio.com/](https://www.keyestudio.com/)

Keyestudio wiki:

[https://wiki.keyestudio.com/Main_Page](https://www.keyestudio.com/)

Microbit Makecode:

<https://makecode.microbit.org/>

Microbit Official:

<https://www.microbit.org/>