# BBC Micro:bit



## 1. What is Micro:bit?

Micro:bit is an open source hardware platform based on the ARM architecture launched by British Broadcasting Corporation (BBC) together with ARM, Barclays, element14, Microsoft and other institutions. The core device is a 32-bit Arm Cortex-M4 with FPU micro-processing. 

Though it is just the size of a credit card, the Micro:bit main board is equipped with loads of components,including a 5*5 LED dot matrix, 2 programmable buttons, an accelerometer, a compass, a thermometer, a touch-sensitive logo and a MEMS microphone, a Bluetooth module of low energy, and a buzzer and others. Thus, it also boasts multiple functions. 

The buzzer built in the other side of the board plays all kinds of sounds without any external equipment. The golden fingers and gears provide a better fixing of crocodile clips. Moreover, this board has a sleeping mode to lower power consumption of batteries when users long-press the Reset & Power button on the back. It is capable of reading the data of sensors, controlling servos and RGB lights, and it is attaching with a shield so as to connect with various sensors. It also supports a variety of programming platforms and is compatible with almost all PCs and mobile devices. Also, driver is required. It is of high integration of electronic modules, and has a serial monitoring function for easy debugging.

The board has found wild applications. It can be applied in programming video games, making interactions between light and sound, controlling a robot, conducting scientific experiments, developing wearable devices. Basically, it always be utilized to make some cool inventions like robots and musical instruments.

------



1.1 Micro:bit V2 Mainboard Layout

![img](img/cd473f8a2c62eba43590328ecc9b6215.png)

------



1.2 Micro:bit V2 Pin-out

![img](img/e0f000fcb898203b89acc6c693d7d86c.png)

Micro:bit pin functions:

|       Function       | Pin                                                          |
| :------------------: | :----------------------------------------------------------- |
|         GPIO         | P0, P1, P2, P3, P4, P5, P6, P7, P8, P9, P10, P11, P12, P13, P14, P15, P16, P19, P20 |
|       ADC/DAC        | P0, P1, P2, P3, P4, P10                                      |
|         IIC          | P19(SCL), P20(SDA)                                           |
|         SPI          | P13(SCK), P14(MISO), P15(MOSI)                               |
|  PWM(commonly used)  | P0, P1, P2, P3, P4, P10                                      |
| PWM(uncommonly used) | P5, P6, P7, P8, P9, P11, P12, P13, P14, P15, P16, P19, P20   |
|       occupied       | P3(LED Col3), P4(LED Col1), P5(Button A), P6(LED Col4), P7(LED Col2), P10(LED Col5), P11(Button B) |

Visit the official website for more details:

[Microbit hardware](https://tech.microbit.org/hardware/edgeconnector/)

https://microbit.org/guide/hardware/pins/

------



1.3 Notes for the Application of Micro:bit

- It is recommended to cover it with a silicone protector to prevent short circuit for it has a lot of sophisticated electronic components.
- Its IO port is very weak in driving since it can merely handle current less than 300mA. Therefore, do not connect it with devices operating in large current, such as servo MG995 and DC motor or it will get burnt. Furthermore, you must figure out the current requirements of the devices before you use them and it is generally recommended to use the board together with a Micro:bit shield.
- It is recommended to power the main board via the USB interface or via the battery of 3V. The IO port of this board is 3V, so it does not support sensors of 5V. If you need to connect sensors of 5 V, a Micro: Bit expansion board is required.
- When using pins(P3, P4, P6, P7 and P10) shared with the LED dot matrix, blocking them from the matrix or the LEDs may display randomly and the data about sensors connected maybe wrong.
- Pin 19 and 20 can not be used as IO ports though the Makecode shows they can. They can only be used as I2C communication.
- The battery port of 3V cannot be connected with battery more than 3.3V or the main board will be damaged.
- Forbid to operate it on metal products to avoid short circuit.

To put it simple, Micro:bit V2 main board is like a microcomputer which has made programming at our fingertips and enhanced digital innovation. And as for programming environment, BBC provides a website: <https://microbit.org/code/>, which has a graphical MakeCode program easy for use.

------



## 2. Micro:bit Installation

**Micro:bit is free of driver installation. However, in case your computer fail to recognize the main board, you can install the diver too.**

**Driver installation: Please download tutorials in network disk.**

Connect micro:bit mainboard to computer via USB cable.

![img](img/9e91e6f5890c7b725e5bfbf16aea1580.png)

Click the driver file ![img](img/a509068450456bfaf0543c6d0877f2e6.png) and "Install".

------

![img](img/0dfae4cc4cefe4ebef032e3036f5e809.png)

------

Click Install.

![img](img/d4713966ae2769c174f4da9d90e4ac68.png)

------

Click “Install” and “Finish”.

![img](img/8f583e09ee48cadd11a7da27a8bad1aa.png)

------

![img](img/161269041ca90e3ffded0b3add2a03ff.png)

------

Click “Computer”  —> “Properties” —> “Device manager”:

![img](img/2bd409a5d1dafbac6733cffad85ef233.png)

------



## 3 Programming

The following instructions are applied for Windows system but can also serve as a reference if you are using a different system.

3.1 Procedures

This chapter describes how to write program and load the program to the Micro: Bit mainboard. Visit official website for more details: <https://microbit.org/guide/quick/>

3.1.1 Step 1: Connect to Micro:bit

Connect the board to computer via USB cable. 

For how to program via mobile deceives: <https://microbit.org/get-started/user-guide/mobile/>

Multiple operation systems are compatible with this board, including Macs, PCs, Chromebooks and Linux (Raspberry Pi). 

![img](img/9e91e6f5890c7b725e5bfbf16aea1580.png)

------

If the red LED on the back of the board is on, that means the board is powered. When your computer communicates with the main board via the USB cable, the yellow LED on it will flashes. For example, it will flash when you burn a “hex” file.

Then Micro: bit main board will appear on your computer as a driver named “MICROBIT(E:)”. Please note that it is not an ordinary USB disk as shown below.

![img](img/9b7d0149612d1c6f1799a942d3d3f9e0.png)

------



3.1.2 Step 2: Write programs

Online version of Makecode: <https://makecode.microbit.org/>

Click **New Project**;

The dialog box **Create a Project** appears, fill it with **heartbeat** and click **Create √** to edit.

If you are Windows 10 system, it is also viable to edit on the APP MakeCode for micro:bit , which is exactly like editing in the website. 

Windows 10 App download: [https://www.microsoft.com/](https://www.microsoft.com/zh-cn/p/makecode-for-micro-bit/9pjc7sv48lcx?ocid=badgep&rtc=1&activetab=pivot:overviewtab)

Here we demonstrate on Google Chrome.

![img](img/c91af45c9080a4989041721173320010.png)

![img](img/5302ffe734b655170e52aa8d7e97ea05.png)

------

Write a micro:bit code. 

You can drag some **Blocks** to the editing area and then run your program in Simulator as shown below: we demonstrate how to edit **heartbeat** program. 

![img](img/330a1abce965fc1443971f3dbf5f64e0.png)

------

Click “ JS JavaScript” to check JavaScript language.

![img](img/bd486c28ff0c4e47a0512a76fc3e8202.png)

------

Click the arrow to switch to “Python” language.

![img](img/aeceb6d3c3060ee4cfd904a1a0ad05c2.png)

------



3.1.3 Step 3: Download code

If your computer is Windows 10 and you have downloaded the APP MakeCode, what you will only have to do is to download the program to your Micro: Bit board.

If you are writing program through the website, following these steps:

1. Click the ‘Download’ in the editor to download a "hex" file, which is a compact program format for Micro: Bit to read;
2. Copy the "hex" file to your board. For Windows, you can also click and select ‘Send to → MICROBIT(E:) ‘to copy the hex file to the Micro: Bit board. 

![img](img/89ea1ca4d2d77c7e65655f4b19be6e90.png)

![img](img/21281760f14f8ce1df012a1b9f3760a8.png)

------

Or, you may directly drag the “hex” file in **MICROBIT**.

![img](img/af5507affc14795d33a327e3deeb7f7f.png)

![img](img/c16c7963ad5024f5cef8e8f385a3f9d1.png)

During the process of copying the hex file to the Micro: bit, the yellow LED on the back of the board flashes. When the duplication is completed, the LED will stop flashing and remain on.

3.1.4 Step 4: Run program

After the program is uploaded to the Micro: bit, you can power it via USB cable or an external power. Then the 5 x 5 LED dot matrix displays a heartbeat pattern.

**Power via USB**

![img](img/8cdc49308884d1c5b2ba32fa37e01a0c.png)

------

**Power via external 3V**

![img](img/a694469c23d92c28aa5f5ece0ade4a63.png)

**Caution:**

- When you programs each time, the driver of Micro: bit will automatically eject and return so the hex files will disappear. 
- The board only has access to hex files rather than save them.

------

3.1.5 Step 5: Other programming languages

This chapter has described how to use the Micro:bit main board.

Except for the Makecode graphical programming, if you want to write Micro:bit programs in other languages, visit <https://microbit.org/code/> to learn more, or visit <https://microbit.org/projects/> to find something you want to have a go.



3.2 Makecode

Google Chrome online version: <https://makecode.microbit.org/>

Or open the Windows 10 App makecode.

![img](img/10e140d7d8ff3b2d3ad8fec4339a8cea.png)

------

Click “New Project” and enter “heartbeat” to edit the code. Here is the main interface of Makecode.

![img](img/ea0adf2aa87facc3cadd4c4901c96373.png)

There are blocks “on start” and “forever” in the code editing area. 

When the power is plugged or reset, “on start” means that the code in the block only executes once, while “forever” implies that the code runs cyclically.

------



3.3 Quick Download

As mentioned before, if your computer is Windows 10 and you have downloaded the APP MakeCode. you can quickly download codes to the Micro: Bit main board  by selecting ‘Download’.

While it is a little more trickier if you are using a browser to enter Makecode. However, if you adopt Google Chrome that is suitable for Android, ChromeOS, Linux, macOS and Windows 10, the process can be easier, too.

We use the webUSB of Chrome to access the hardware device connected by USB.

You could refer to the following steps to connect and pair devices.

**Devices Pairing**

Connect the board to computer via USB cable. 

![img](img/9e91e6f5890c7b725e5bfbf16aea1580.png)

------

Click “...” and “Connect device”.

![img](img/25c31c73cff635b6348da7b45df63b21.png)

------

“Next”.

![img](img/e574b7286ff61c1d689cf87ffdea1e93.png)

------

“Next”.

![img](img/52556be4f5a27100bc6bbc48a8d76671.png)

------

Then select the corresponding device and click “Connect”. If no device shows up for selection, please refer to: <https://makecode.microbit.org/device/usb/webusb/troubleshoot>

If the links are too troublesome, we also provide **Troubleshooting** in tutorial. 

For how to update micro:bit firmware: <https://microbit.org/guide/firmware/>

![img](img/7cca59d37bc73eac24f017995d3c3174.png)

------

Click “Done”.

![img](img/383f451f6dd0a1b06ea2ee9c299b1e39.png)

![img](img/ee3131908d2502ffd7b5e164e18c2b7f.png)

------

**Download program**

After connection, click ![img](img/d2df9fa4e4e008c23e0545e894c16963.png) and it will change into ![img](img/63a5052cba26eb41b180a516aa1aa8b9.png).

![img](img/96fbd5a50eb87de8ad464cbbd09624f1.png)

------



3.4 Makecode Extension Library

3.4.1 Add library

Please follow the steps to add extension files:

Open makecode to enter a certain project, click the gear-shaped icon(settings) in the upper right corner to choose “Extensions”.

![img](img/597024d689a51501957758a6af91b468.png)

------

Or click Advanced to add Extensions.

![img](img/b73fa343859638361e37e954ada69e28.png)

------

Search the library you want. 

![img](img/ed4cfcb654e76f3dc6dc4d77755e0a34.png)

------

For instance, a servo library is required, so you can search "servo" to add one.

![img](img/cd840405fb3892f2d0d4e0eac1aff085.png)

------

Back to the interface and you can see a **Servos** library.

![img](img/3c4864e80f5a38e9798bfba948ea8406.png)

------

3.4.2 Update/Delete library

Click **Js JavaScript** to switch to text code.

![img](img/a0185a999e46caa08810ba6820e7df55.png)

------

Click Explorer.  

![img](img/f1f7abcf1d5a0b5eab79212c6888c929.png)

------

Find the library you want to remove and click to delete it.

![img](img/9b99bcbbd085a7ea3f29f1aca4b0a592.png)

------

Click **Remove it**.

![img](img/6781c980ca7a4e1dba18376aa799ea7d.png)

------

Click **Blocks** to return to graphical programming. 

![img](img/68ac58c7cf98d93fb89767bd315d0246.png)

------

![img](img/434ac955304762c30d4d2ddff1d01636.png)

------



3.5 Resources and Test Code

Download: https://fs.keyestudio.com/KS0801

3.5.1 Import code

We provide hexadecimal code files (project files) for each project. The file contains all the contents of the project and can be imported directly, or you can manually build the code blocks. 

**For simple projects, dragging a block of code to complete the program is recommended.**

**For complex ones, it is recommended to conduct the program by loading the hex code files.**

Let's take the "Heartbeat" project as an example to show how to load the code. Open the Web version of Makecode or the Windows 10 App Makecode, and click “Import”.

![img](img/ca04eb74ddeea7403e418974a655329f.png)

------

Click “Import File...”.

![img](img/77d138b1113ae1cee2cbdbefc3cb919c.png)

------

![img](img/1d9f0b8c2d20f18a1f3412dc01bc3b24.png)

Choose “Heart beat.hex”.

![img](img/b1800213ab7d7183f29d4139bdf8df08.png)

![img](img/7bf878d223fc2108f6198a59adb1a2e4.png)

------

In addition to the above method, you can also drag the the test code into the code editing area, as shown below:

![img](img/8201abe30dc053fc9cdcc6e0ace2acfe.png)

------

Wait for loading.

![img](img/b9a528f9b9eb9ca66471149955bf154b.png)

------



3.5.2 Install CoolTerm

If your computer is Win7/8, the pairing cannot be done via Google Chrome. Therefore, digital signal or analog signal of sensors and modules cannot be shown on the serial simulator. So what can we do? CoolTerm software is a nice choice to read the serial data.

CoolTerm download: <https://freeware.the-meiers.org/>

1. We take PC Windows as an example to download and unzip CoolTerm Win, and Mac/Linux can take it as a reference. 
    ![img](img/9be1cc303f8a2a8baf9eabe2661799d0.png)
    
2. Make sure the driver is connect to computer, and click to execute the software.

    ![img](img/6b14a0a5e02c8cbc7a3d5849da2ebca1.png)

3. The functions of each button on the Toolbar are listed below: 

    ![img](img/f842eec5ce7625c645ee5b6aa6f7dc4f.png)

|        Icon         |                     Function                     |
| :-----------------: | :----------------------------------------------: |
| ![img](img/c329f8f0f5c1d3fd4936e6799434e242.png) |             Opens up a new Terminal              |
| ![img](img/68b8321a0dba7dafc860a77e9bb769e8.png) |             Opens a saved Connection             |
| ![img](img/300e3e83cce49325d4081991e476de7d.png) |       Saves the current Connection to disk       |
| ![img](img/59f4d60ca5b55d6b5f3c8708bbb96d58.png) |           Opens the Serial Connection            |
| ![img](img/a49e2505552f58ea14cbbd16c8072414.png) |           Closes the Serial Connection           |
| ![img](img/b194b2f73706d38597b4411bde90fa3f.png) |             Clears the Received Data             |
| ![img](img/e8a3c0d8688aed3e49972d11598eaa1e.png) |       Opens the Connection Options Dialog        |
| ![img](img/136e95a61a70779c777438792d7a6651.png) | Displays the Terminal Data in Hexadecimal Format |
| ![img](img/3fd3de6ad029cbac4961c5be5035714a.png) |             Displays the Help Window             |

  

------



## 4. Micro:bit Basic Projects

Project 1: Heartbeat

![img](img/f4bb21a8fec96e4d46e7cb17ec925180.png)

1. Introduction
This project is easy to conduct with a micro:bit main board, a Micro USB cable and a computer. The micro:bit LED dot matrix will display a beating heart. It serves as a start for your entry to the programming world!

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code
Please check code in Project 1 file.

![img](img/e32339a32211f731bb81ab7287e07060.png)

![img](img/f4e308bf5276f85b8d0af38bbb4911a2.png)

Visit <https://makecode.micro:bit.org/reference> to find more information about micro: bit blocks. 

Visit <https://makecode.micro:bit.org/> for programming helps.

**Find code blocks:**

![img](img/121d7a0ffa3352593d46b4b30d7e5269.png)

**Build blocks:**

![img](img/83062720cfedf7f3b7a92a04dc29176f.png)

Click “JSJavaScript” to see Java code:

![img](img/dc6234afcf116b2fe25450a94e0632b0.png)

Pull down to click “Python” to see Python code:

![img](img/75b13cf7fc1ccaae4396ee5052d61abe.png)

------



5. Test Result

After uploading test code to micro:bit main board and keeping the connection with the computer to power the main board, the LED dot matrix shows pattern “❤” and “![img](img/d92f7fd157047fdb954e0c31a943bb54.png)”,  alternately.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：)

**If the downloading is not smooth, please remove the USB cable from the main board and then reconnect them and reopen Makecode to try again.**

------------

Project 2: Single LED Blinking

![img](img/f4bb21a8fec96e4d46e7cb17ec925180.png)

1. Introduction

In this project, we intend to control a certain LED of the micro:bit main board to light up.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Knowledge
The LED dot matrix consists of 25 LEDs arranged in a 5 by 5 square. 

In order to locate these LEDs quickly, as the figure shown below, we can regarded this matrix as a coordinate system by marking 0~4 from top to bottom and from left to right. Therefore, the LED sat in the second of the first line is (1,0) and the LED positioned in the fifth of the fourth column is (3,4), and others likewise.

![img](img/090725a52b6ad4ecd864627ef9dc4e74.png)

5. Test Code

**Find code blocks:**

![img](img/7ef144fbaa3fbd27e73cdbd529370a58.png)

![img](img/b18ca954b915771bb16c973edf55d6d5.png)

![img](img/23be490409b77e1007e36d4ae65ec6ad.png)

**Build blocks:**

![img](img/8521733c78ab255116cc47c7ad7a1817.png)

6. Test Result

After uploading test code to micro:bit main board and powering the main board via the USB cable, the LED in (1,0) lights up for 1s and the one in (3,4) shines for 1s and this sequence will repeat.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

-------------------

Project 3: LED Dot Matrix

![img](img/f4bb21a8fec96e4d46e7cb17ec925180.png)

1. Introduction

Dot matrices are very commonplace in daily life. They have found wide applications in LED advertisement screens, elevator floor display, bus stop announcement and so on.

The LED dot matrix of Micro: Bit main board contains 25 LEDs in a grid. Previously, we have succeeded in controlling a certain LED to light by integrating its position value into the test code. Theoretically, we can turn on many LEDs at the same time to show patterns, digits and characters. 

What’s more, we can also click ”show icon“ to choose the pattern we like to display. Last but not the least, we can design patterns by ourselves as well.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code

**Find code blocks:**

![img](img/451ab1a5b6f829455aaf4a7a6fb59235.png)

**Build blocks:**

![img](img/e754f92495f107ad407530aeac469a6d.png)

5. Test Result
After uploading test code to micro:bit main board and powering the main board via the USB cable, we find that the 5*5 dot matrix start to show numbers 1, 2, 3, 4 and 5, and then it alternatively shows ![img](img/7e45ac1892618e97755923f31cce6640.png), “Hello!”, ![img](img/174ebc72a1f4101c9b179dff555c0e5e.png), ![img](img/aacfdbc806a532159aebf0ecbbf7d084.png), ![img](img/575ef9e667f0d8ac6723a65edebf7929.png), ![img](img/73c29beb6db96a1c8010e2882b1b96f4.png) and ![img](img/e59606abcf37b86e82d15bf4814d4254.png)!

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

--------------------

Project 4: Programmable Buttons

![img](img/ca2deada03ca62874731045f7719e91f.png)

1. Introduction
Buttons can be used to control circuits. In an integrated circuit with a button, the circuit is connected when the button is pressed and if you release the button, the circuit is open.

Micro: Bit main board boasts three buttons: two programmable buttons (marked with A and B), and a reset button at back. By pressing the two programmable buttons, three different signals can be input. We can press button A or B or both so that the LED dot matrix shows A, B and AB respectively. 

Let’s get started!

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection

Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/d97f4afddf9db00511cae4be70294445.png)

![img](img/e52ba3f32c56c1703189c38ea1a63b0f.png)

**Build blocks:**

![img](img/8c54bc2627ec5aa808d7df16e0b4a22b.png)

5. Test Result 1

After uploading test code and powering on, the 5*5 LED dot matrix shows A if button A is pressed and then released, B if button B pressed and released, and AB if button A and B pressed together and then released.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

6. Test Code 2

**Find code blocks:**

![img](img/48e31ab095ee86330fe54c5542ab1d2b.png)

------

![img](img/3933353fab3f558ca7a71babd27864cb.png)

------

![img](img/9647b233542011bce3286849e7c09f25.png)

------

![img](img/1d47d2a7f252153e9f945f93f61e65bb.png)

------

![img](img/2cbe63c82f3b4f5e3e8f6537e8c50b8a.png)

**Build blocks:**

![img](img/e6c10859d53910af0c6bc1fb33bcf129.png)

------



7. Test Result 2
After uploading test code and powering on, when the button A is pressed, the LEDs in red increase; when the button B is pressed, the LEDs in red reduce.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

-------------------

Project 5: Temperature Detection

![img](img/8a4f1503d3b7099cd6f5f1b62ffa2727.png)

1. Introduction
The Micro:bit main board is actually not equipped with a temperature sensor, but uses nNFR52833 chip for temperature detection. Therefore, the detected value is much closer to the temperature of the processor, so there maybe deviation from the ambient value. 

Its detection range is -40 ~ 105℃.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/1f593c36350bfeaeccda31cf94bb0679.png)

------

![img](img/3faf90a9f88b3f0878e2774d42b22168.png)

------

![img](img/339d4c3a3237eb684fed3a7bf52f209b.png)

------

**Build blocks:**

![img](img/aba7ed7980fcee54521b844f73f4854a.png)

5. Test Result 1
After uploading test code 1 to micro:bit main board, powering the main board via the USB cable, and click “**Show console Device**”, the temperature value shows in the serial monitor as shown below.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

![img](img/5c755aa88a6aae787483bed56a87e0a1.png)

When you touch the processor nNRF52833 on the board for a while, its temperature will rise gradually and the CoolTerm serial monitor will show this change:

![img](img/02e50d9b3985cc988d3b742be3f4bf11.png)

If you're running Windows 7 or 8 instead of Windows 10, Google Chrome won't be able to match devices. so you'll need CoolTerm.

Open CoolTerm and click **Options** to select **SerialPort**, set COM port and put baud rate to 115200 (after testing, the baud rate of USB SerialPort communication on Micro: Bit main board is 115200), and then click **OK** and **Connect**. 

![img](img/1168f97aa42d694b3bac105dfa0ffb4f.png)

------

![img](img/c1637185df07a59d243ab38363d07438.png)

The CoolTerm serial monitor shows the change of temperature in the current environment, as shown below:

![img](img/66e293a8fdc1210f5d909b1170e9371f.png)

6. Test Code 2

**Find code blocks:**

![img](img/a2004dbc88d2a60fc509303979bc0de2.png)

------

![img](img/8f01b14e4e5adcadc4e9d7a9d9197a64.png)

------

![img](img/3faf90a9f88b3f0878e2774d42b22168.png)

------

![img](img/cfb61e03166148d7ad0b220d540c7929.png)

------

**Build blocks:** 35 in the code can be modified according to actual conditions.

![img](img/1130b39024fbd82ee60d5492e003e16f.png)

7. Test Result 2

After uploading the code 2 to the board, when the ambient temperature is less than 35℃, the 5*5 LED dot matrix shows ![img](img/48239af0c8a3088ec1427d643f19a71c.png). You may cover the sensor on the board to make the temperature equal to or become greater than 35℃, and then ![img](img/eda453c4d1884a5818d65e31f3b2125a.png) will appear.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

-----------

Project 6:  Geomagnetic Sensor

![img](img/0b8e941a34c873cfbea08f67ec4cf7e3.png)

1. Introduction

This project aims to explain the use of the Micro: bit geomagnetic sensor, which can not only detect the strength of the geomagnetic field, but also be used as a compass to find bearings. It is also an important part of the Attitude and Heading Reference System (AHRS). 

Micro: Bit main board uses LSM303AGR geomagnetic sensor, which supports four modes namely 100 kHz, 400 kHz, 1 MHz and 3.4 MHz and the dynamic range of magnetic field is ±50 gauss. In the board, the magnetometer module is used in both magnetic detection and compass. 

In this experiment, the compass will be introduced first, and then the original data of the magnetometer will be checked. The main component of a common compass is a magnetic needle, which can be rotated by the geomagnetic field and point toward the geomagnetic North Pole (which is near the geographic South Pole) to determine direction.

**Attention: this geomagnetic sensor built in the board can help us determine bearings by showing readings in the value from 0 to 360. And we need to calibrate it for the first by rotating. Please note that metal materials around may attenuate the accuracy of the reading and calibration.**

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/89122e46755b176d730df4e394b37679.png)

------

![img](img/3f5d0fc0ee19ac247028519970fc51f2.png)

------

![img](img/589371365e379425eee8a8ca87603c1f.png)

------

**Build blocks:**

![img](img/cd6f98bdbe9f838d506d48b050d784d1.png)

------

Note: it is imperative to calibrate the Micro:bit board because different geomagnetic fields exist in different places. And the board requires a calibration for the first using time.

5. Test Result 1
After uploading code and powering on, press the button A and the board need to be calibrate when you see LED dot matrix shows “TILT TO FILL SCREEN”. Rotate the board until all 25 red LEDs are on as shown below.

![img](img/20f477d9f9624bc97afa596be0911081.png)

After completing calibration, a smile ![img](img/2018782e6c693cc7f78ba1d9d011009d.png) will appear. Press button A, and the detected magnetometer value will show. And the direction north, east, south and west correspond to 0°, 90°, 180° and 270° respectively.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

6. Test Code 2

![img](img/014d600363f0ced7e7b38c3bf7a03917.png)

We read the value to determine direction: the arrow points to the current magnetic North Pole.

![img](img/21b186cbab0a21a911eba24b9edaabbb.png)

For the above picture, the arrow pointing to the upper right when the value ranges from 292.5 to 337.5. 

0.5 can’t be input in the code, so the values we get are 293 and 338. We add other statements to make a set of complete code.

**Find code blocks:**

![img](img/e827505c71838e80c91efdff67a950ce.png)

------

![img](img/1f5bc3d85ced13eaca10e9da63f21c27.png)

------

![img](img/9730e57665b5c9bce36e25110419f17b.png)

------

![img](img/22cf3e4414fc1843094da4ca76629269.png)

------

![img](img/ea205199be8489dbf426f9091381f62f.png)

------

 **Build blocks:**

 ![img](img/5979595913505c71904e95471972e4cd.png)

 ![img](img/f3aeae974d758ab504406fff1b3ead26.png)

 ![img](img/9f3ba48085872c4b0034c8b977b3c9ea.png)

7. Test Result 2
After uploading code and calibrating, tilt micro:bit board and the LED dot matrix displays the direction signs. 

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

----------------


 ### Project 7: Accelerometer

![img](img/0b8e941a34c873cfbea08f67ec4cf7e3.png)

1. Introduction
The micro:bit board boasts a built-in LSM303AGR acceleration sensor (accelerometer) which includes standard, fast, plus and high-speed mode (100 kHz, 400 kHz, 1 MHz and 3.4 MHz) of I2C serial bus interface and SPI serial standard interface for external communication, with resolution of 8/10/12 bits and range of ±2g, ±4g, or ±8g.

When the micro:bit board is at rest or in uniform motion, the accelerometer only detects the acceleration of gravity. If the board is slightly swung, the detected acceleration is much less than the that of gravity, but the difference can be ignored. Therefore, we mainly detect the change of gravitational acceleration on the x, y, and z axes.

In this project, we will introduce how to measure the position of the board with the accelerometer. And then we may have a look at the original three-axis value output by the accelerometer.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/5bdda251b0b166b4eeee0fe8b653455c.png)

------

![img](img/7aa6b4706b1d68432a3f7a63de989132.png)

------

![img](img/138cdcaf5804568ccf89bd54ab092fe7.png)

------

**Build blocks:**

![img](img/101a3c9829e2192a39ff7fa1ed2ab4f5.png)

------

5. Test Result 1
After uploading code and powering on, if we shake the Micro:Bit board(any direction), the LED dot matrix displays the digit “1”.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

When the logo is kept above, number 2 displays.

![img](img/71dc63c93fcba6efcade8bb5916b823a.png)

------

When it is kept upside down(logo below the LED dot matrix), it shows as below.

![img](img/015c2cb5d47b3ad48cfabd672efe235b.png)

------

When it is placed on the desk, the number 4 appears.

![img](img/044aea0f3a87074ed2179318635ee6f3.png)

------

When it is covered on the desk, the number 5 exhibits.

When the board is tilted to the left, the LED dot matrix shows the number 6 as shown below.

![img](img/422bd03a2b11150b0d75550caed8ae89.png)

------

When the board is tilted to the right , the LED dot matrix displays the number 7 as shown below:

![img](img/7340146fdc69ed39b9548b8351bd81ae.png)

------

When the board falls down to the floor (a free fall), the LED dot matrix shows the number 8. (Please note that this test is not recommended for it may damage the main board.)

If you’d like to try this function, you can also set the acceleration to 3g, 6g or 8g. But still ,we do not recommend.

6. Test Code 2

**Find code blocks:**

![img](img/66dd802181be5117ea158338921ca645.png)

------

![img](img/64249fa35ab671dea0f569826b0d75cf.png)

------

![img](img/03c261f2f06b583e63614ff9ab445a9f.png)

------

**Build blocks:**

![img](img/5bd9d21d322a3368b73c7b795e0087af.png)

7. Test Result 2
Upload test code to micro:bit main board, power the main board via the USB cable, and click “Show console Device”.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

![img](img/3f45cf37d7684557ebec490f34ddaae9.png)

After referring to the MMA8653FC data manual and the hardware schematic diagram, the accelerometer coordinate of the Micro: Bit are shown in the figure below:

![img](img/dc0be75af97895b865e5b48c9850271c.png)

The following interface shows the decomposition value of acceleration in X axis, Y axis and Z axis respectively, as well as acceleration synthesis (acceleration synthesis of gravity and other external forces).

![img](img/abb4a092dff94eb511e96600b2b83bf3.png)

If you're running Windows 7 or 8 instead of Windows 10, via Google Chrome won't be able to match devices. You'll need to use the CoolTerm serial monitor to read value.

Open CoolTerm and click **Options** to select **SerialPort**, and set COM port and baud rate to 115200. Click **OK** and **Connect**. The CoolTerm serial monitor shows the data of X axis, Y axis and Z axis , as shown in the figures below:

![img](img/be2df7cbbfe695f858013635810c25b8.png)

Project 8: Light Brightness Detection

![img](img/f4bb21a8fec96e4d46e7cb17ec925180.png)

1. Introduction

In this experiment, we will use the micro:bit board to detect light intensity. Since the micro:bit board does not contains its own photoresistor, the LED dot matrix will shoulder this job. The light signal will convert into input, and the voltage decay time is sampled so that the detected light intensity is a relative value. 

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code

**Find code blocks:**

![img](img/66dd802181be5117ea158338921ca645.png)

------

![img](img/9e7f25899c5050026fb1e2594b9c6c55.png)

------

![img](img/736d7bbc3c47fbed369b79638dd09776.png)

------

![img](img/6e194a232d3165f295e6804b435a6d4e.png)

------

**Build blocks:**

![img](img/fe52a894d942f2d39c02f97f3e9e004c.png)

5. Test Result
Upload the test code to micro:bit main board, power the board via the USB cable and click “Show console Device”. 

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

![img](img/0bd488278f2b494286af046811cdf5ea.png)

When the LED dot matrix is covered by hand, the light intensity is approximately 0; when the LED dot matrix is exposed to light, the light intensity gets stronger with the light as shown below:

![img](img/9296040795351b9b0bae50981daf9069.png)

20 in the code is an arbitrary value of light intensity. If the current light value is less than or equal to 20, the icon moon will appear on the LED dot matrix. If it's bigger than 20, the sun will appear.

If you're running Windows 7 or 8 instead of Windows 10, Google Chrome won't be able to match devices. CoolTerm will be required.

Open CoolTerm and click **Options** to select **SerialPort**, and set COM port and baud rate to 115200, click **OK** and **Connect**. The CoolTerm serial monitor shows the value of light intensity, as shown below:

![img](img/729aadada99133505f2c767781e4d175.png)

------------------

Project 9: Speaker

![img](img/afe0369ddeab3222446b0ef9566b233a.png)

1. Introduction
Micro: Bit board boasts an built-in speaker, which makes sound to the programs easier. It is also able to make sound such as utter giggles, greetings and yawning as well as all kinds of tones, like playing the song *Ode to Joy*.

You can also turn off the built-in speaker to enjoy the beautiful music via headphones connected to GND and P0. In MakeCode, you need to turn off the speaker by "Turn off built-in speakers" block.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/de9eb71979c4135de5cc530507a6f56d.png)

------

![img](img/817bb46143c9e84d4fe988a0c4ba3406.png)

------

![img](img/0b369696f2ce6477989b154f0de7d2a4.png)

------

**Build blocks:**

![img](img/86dc82b8b626a6899d8d106d8371ac5e.png)

5. Test Result 1
After uploading code and powering on, the speaker utters sound and the LED dot matrix shows the logo of music.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

6. Test Code 2

**Find code blocks:**

![img](img/de9eb71979c4135de5cc530507a6f56d.png)

------

![img](img/817bb46143c9e84d4fe988a0c4ba3406.png)

------

![img](img/362f9859f277dd2bee2d4737c08cb734.png)

------

**Build blocks:**

![img](img/d4de687740dfc60c08be4318b94cadba.png)

![img](img/b2237a79e226d26039614e99d6b76a01.png)

![img](img/b5be9c3fc0e32b15b43120cd0e82f147.png)

![img](img/3f986904a7ffa3483636f2879be9b2cd.png)

![img](img/b674c01a0b5ff717c5fc96bb1ddedd59.png)

![img](img/e600d94f99d152faafe71f8487d1d4a4.png)

*Ode to Joy*:

![img](img/b230b10da5b9276184ad2d1a18b978bb.png)

For more information about musical notations: <https://en.wikipedia.org/wiki/Numbered_musical_notation>

-----------------

Project 10: Touch-sensitive Logo

![img](img/6c5540180f33419adcf01c5228a32538.png)

1. Introduction

The Micro: Bit main board is equipped with a golden touch-sensitive logo, which can act as an extra button. This capacitive touch sensor senses small changes in the electric field when it is pressed or touched.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code

**Find code blocks:**

![img](img/bd9540f5c85c27ba7ac0743356081675.png)

------

![img](img/a736ece71e98596f5c8b574e161a4cfe.png)

------

![img](img/2c2b5f596eb4d9de7b6fb2067440be3f.png)

------

![img](img/2ff4797a58a94f595257a637f7f38984.png)

------

![img](img/b9a40d0458ce24c1ea80f758af6ed043.png)

------

![img](img/8f87c2be16fe231efc21257854b0373e.png)

------

**Build blocks:**

![img](img/8ff46a5f8e4914f1499c8cdc7aeff9ec.png)

5. Test Result

After uploading the code and powering on, the LED dot matrix exhibits the heart pattern “❤” when the logo is pressed or touched, and it displays digit when the logo is released. The longer it is pressed, the bigger the number is when it is released.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

---------------------

Project 11: Microphone

![img](img/b12fb68f5b6af59848b2dcfabd936d6b.png)

1. Introduction
The Micro:bit mainboard is built with a microphone which can test the volume of ambient environment. When you clap, the microphone LED indicator turns on. So, you can make a disco lighting changing with music. The microphone is placed on the opposite side, and an LED indicator is next to the hole that lets sound pass. When the board detects sound, the LED indicator lights up.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code 1

**Find code blocks:**

![img](img/2a9b922f99622c6697c29942572d10a8.png)

------

![img](img/db4be680adf422bc533765ae26f17d19.png)

------

**Build blocks:**

![img](img/4087268a169730cc2f80cc94df04d131.png)

5. Test Result 1
After uploading test code to micro:bit main board and powering the board via the USB cable, the LED dot matrix displays “❤” when you clap, and “![](img/48239af0c8a3088ec1427d643f19a71c.png)” appears when it is quiet around.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

6. Test Code 2

**Find code blocks:**

![img](img/d601751461648348d2a9abb3cdb96239.png)

------

![img](img/b64c806b260c1296d704b6330130d276.png)

------

![img](img/0b577869af5a8795f675b1cf27ba3280.png)

------

![img](img/06ce00bf888669f861897c1a76ace3b5.png)

------

![img](img/046b3f7e6a6f6f375bfda46b71f45b3b.png)

------

![img](img/31386c49ad3b6aaac6510cae3991b988.png)

**Build blocks:**

![img](img/6414c2c467850d0e027e270c309f0e57.png)

7. Test Result 2
Upload test code and power on and click “Show console Device” as shown below: 

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

![img](img/28f81decae0cec3d650766d961b78b3b.png)

The louder the sound is, the greater the sound value will show on the serial monitor:

![img](img/bfcd31bbb5cd77eaf925bbd7e8b51513.png)

When the button A is pressed, the LED dot matrix displays the value of the biggest volume. Please note that the biggest volume can be reset via the Reset button. When you clap, the LED dot matrix shows the pattern of the sound.

----------------

Project 12: Play Music

1. Introduction

In the previous projects, we have learned about the touch-sensitive logo and the speaker respectively.

In the project, we will combine these two components to play music. We will apply the Logo to control the speaker to sing songs.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Test Code

**Find code blocks:**

![img](img/672cfe3afa0705f37ae7e7d4cdc4f016.png)

------

![img](img/5232f00248170030a939b5e41c119b5d.png)

------

![img](img/9299a54aac89d8abbe9eddebb6ed97e9.png)

------

![img](img/817bb46143c9e84d4fe988a0c4ba3406.png)

------

![img](img/5e37e62ce5fb64c9658fe6fb56e25319.png)

------

**Build blocks:**

![img](img/2cf06393519341e4c6ed3a91833ae219.png)

5. Test Result
After uploading test code to micro:bit main board and powering the board via the USB cable, the speaker plays *Birthday Song* when the logo is touched.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

--------------------


Project 13: Dodge Bullets

1. Introduction

We have learned about the two programmable buttons: button A and B. In this project, we will combine them with LED dot matrix to design a game: Dodge Bullets.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png) |
| --------------------- | ------------------ |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Game 1

Dodge bullets! Don't get hit!

**Find code blocks:**

![img](img/56e391676a53658405b358850ebea8a2.png)

------

![img](img/07c2af080d719fc6651813e6f40b9f1a.png)

------

![img](img/970e505bf55bdf6edaf0fdec8105d3eb.png)

------

![img](img/91cd323013bae5970f77618bba714d24.png)

------

![img](img/dfecfbf2602c74bc7951b5ceb7377b2f.png)

------

![img](img/b01448970f19c43b9304f299094e116c.png)

------

![img](img/4978513824b479a7bf10d582322bd579.png)

------

![img](img/d39b623b06feff89a45dbd5dfc1c03d8.png)

------

**Build blocks:**

![img](img/53be1a205a8281697fb6f8072311488e.png)

------

![img](img/fda72c97af9cc39e2b6bcc91077605c1.png)

6. Test Result 1
The game begins when the code is uploaded to the main board. The bullets fall off and we need to control the role G by Button A and B to shun them. If the role fail to avert the attacks, game is over.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

7. Game 2
Dodge bullets! Earn points!

Get one point for dodging one bullet; Game over when the role G is hit by bullet and the points will be output. Press A and B together, restart the game.

**Find code blocks:**

![img](img/ac8bf91c9213693f6eb850068fda20d3.png)

------

![img](img/dc1899ff6fc6368fd92aee55c21ef334.png)

------

![img](img/489a0784fc25181c8cf6fe9eae96de92.png)

------

![img](img/09179001236c5c08cc3293b92de90357.png)

------

![img](img/2729ab66454fc9bfce14e2893a78b96e.png)

------

![img](img/dfecfbf2602c74bc7951b5ceb7377b2f.png)

------

![img](img/b01448970f19c43b9304f299094e116c.png)

------

![img](img/c916263f893183a0a53de7ace92369fc.png)

------

![img](img/4978513824b479a7bf10d582322bd579.png)

------

![img](img/28bb3966c613184072c8fed600259f6c.png)

------

**Build blocks:**

![img](img/5594269620042e3eec81a94ca2327128.png)

------

![img](img/f17778dde9101afd0361e24e1a295728.png)

------

![img](img/20522f7247ce087ada68c73dae3dc5ae.png)

------

![img](img/71c09b8c51bdca3c3180c8fbb1cbd84d.png)

8.  Test Result 2
The game begins when the code is uploaded to the main board. The bullets fall off and we control the role G by Button A and B to shun them. 1 score will be tallied for each successful dodging. If the role fail to avert the attacks, the game is over and gained scores displays.

Press buttons A and B at the same time, and the game starts again.

[How to download?  How to quick download?](#3.1.3Step 3: 下载代码：) 

---------------------

Project 14: Bluetooth Wireless Communication

![img](img/3278b0f23d908e69bef17d6552da3a21.png)

1. Introduction

The Micro:bit main board comes with a nRF52833 processor with a built-in BLE(Bluetooth Low Energy) Bluetooth 5.1 device and a 2.4GHz antenna for Bluetooth wireless communication, so that the board is able to communicate with a variety of Bluetooth devices, including smart phones and tablets.

In this project, we mainly concentrate on the Bluetooth wireless communication to transmit code or signals. Firstly, we should connect a device (a phone or an iPad) to the board. 

Since setting up Android phones to achieve wireless transmission is similar to that of Apple devices, no need to illustrate again.

2. Components

| Micro:bit mainboard*1 | ![img](img/d827138a074f135b861c14a50ad3d6ea.png)   |
| --------------------- | -------------------- |
| Micro USB cable*1     | ![img](img/ea6bddc5a2be925abc8b955426c6279a.png)   |
| smart phone/IPad*1    | ![img](img/274ba2573e1b8804cfa7de16e60c05a5.png) |

3. Connection
Connect the board to your computer via micro USB cable.

![img](img/017d4b0d60f1111a675c614c55d4fc14.png)

4. Procedures

We will demonstrate on iPhone/iPad/MAC devices. Android/Windows devices may take these as a referance.

(1) Firmware (iOS/MAC only)

iOS/MAC: <https://www.microbit.org/get-started/user-guide/ble-ios/>

Click “Download pairing HEX file” to download the Micro: Bit firmware and upload the downloaded firmware to the Micro: Bit main board.

![img](img/5b0caf021cf4b99b2484882b4fad3543.png)

------

![img](img/d0aae7bbb7657614ac84e98bcffa2f0a.png)

------

![img](img/e4c32c6173b32cbeaa21eb728d1d3e7b.png)

(2) Micro:bit APP

Open App Store![img](img/55ae6afd33c16d257de54f896f168520.png) and search “micro bit” and click “![img](img/35f6d695d661991ae13584f535d40bcb.png)” to download the APP.

![img](img/f6e8610ad574cc53b6dd2336bb4b9a21.png)

(3) Connection

Connect your Apple device with Micro: Bit main board.

- Turn on Bluetooth on the device.
- Open ![img](img/4245848e9c7c2dcbd0d5ca4f3988179f.png) APP, ensure the board is connected to the device and select “Choose micro:bit”to start pairing Bluetooth.

![img](img/f1d8100dd51826145a523704293dc5d8.png)

  - Pair a new micro:bit.

    ![img](img/194d14b1a5454398e7870e2b753a7911.png)

  - Following the instructions to press button A and B at the same time(do not release them until you are told to) and press Reset & Power button for a few seconds. 

![img](img/1445da9d348071873438dd9a1107333e.png)

- Release the Reset & Power button, you will see a password pattern shows on the LED dot matrix. Now , release buttons A and B and click “Next”.


![img](img/ce70080c5446b3e83091caaddb5be555.png)

  - Set the password pattern on your Apple device as the same pattern showed on the matrix and click “Next”.  

![img](img/1cda3783ac4d939077f6c543c0081106.png)

  - Still click “Next”and a dialog box props up as shown below. Then click "Pair". A few seconds later, the match is done and the LED dot matrix displays the "√" pattern.

    ![img](img/e559d2f2570bd785a52a84547dd078bb.png)

    ![img](img/17aa4a0c0508f1e246d024a0975a0fa8.png)

    ![img](img/73fb126cc1c5e07ece15758347bd0350.png)

    ![img](img/325747215a759538e8ec0de254f7d165.png)

  - After the match with Bluetooth, write and upload code with the App.

(4) Create Code

Click “Create Code” to enter the programming page and write code.

Click "New Project" and you will see ![img](img/6a8eef38b371231abdf28888bdc6f038.png), and then select “Create √”. 

![img](img/c9bef91dc00af1fcf5f82b23269ee0d9.png)

![img](img/6a4b4dd5a7f21e3b369790ad94746753.png)

![img](img/d7041ca65ce1ae97f150f7348491552f.png)

![img](img/5a85891e2295f773c02bd253bc4725df.png)

Name the project as “1 “and click “![img](img/32a569c1ee8da1f0f1a3dab969fee8b5.png)” to save the code.

![img](img/afa5c3e7799acb35b75fe0512c11f88a.png)

Click “Flash” to enter the uploading page. 

The default code program for uploading is the one saved just now and named "1" and then click "Flash" to upload the code program "1".

![img](img/dee1a68b7b4e3ee5bfef66c4488e2304.png)

![img](img/a2211125ae2617026a97dcd7b973d7a9.png)

![img](img/62ed1f8ffa2639e136bc54271adca735.png)

If the program “1” is uploaded successfully a few seconds later, the App will show as below and the LED dot matrix will display a heart pattern.

![img](img/e26d237aa5c0c8bb9267c567ad9e9e1b.png)

------

