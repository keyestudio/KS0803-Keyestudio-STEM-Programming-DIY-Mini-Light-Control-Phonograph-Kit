## ESP32 Easy Coding Board Basic Projects

1 Heartbeat

![img](img/0cf1e7028ce5e6f4f9c9df7d50c4a995.png)

1. Introduction

This project is easy to conduct with an ESP32 Easy Coding Board, a USB type-C cable and a computer. The ESP32 Easy Coding Board RGB dot matrix will display a beating heart. It serves as a start for your entry to the programming world!

2. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

3. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

4. Test Code

Please check code in Project 1 file.

![img](./img/079bbc1db6550b30de5d7708d476f14e.png)

![img](img/cd24339303faa8efd162100fe9e9fc22.png)

Find RGB blocks to change its brightness and colors.

![img](img/8105c07199d9d1b8b35e71040496884d.png)

**Build blocks:**

Initialize the RGB dot matrix.

![img](img/53f48027e3d08a5ec3e0c4221d47a10a.png)

![img](img/1713063ff14d71ae06a35e195e227897.png)

![img](img/f8878b1ea9cf232b86b66d6827c60e4e.png)

**Complete code:**

![img](img/bfb050d6f17d28fee7f83c022c3cea8d.png)

5. Test Result

After uploading test code to ESP32 Easy Coding Board and powering via USB cable, the RGB dot matrix alternately shows patterns of a small and a large heart.

![img](img/b28d0c01c7abaeb2cae2bbe204b5ba38.png)

![img](img/ebcd3d3b7ab3595dfc355a5925e16156.png)

2 Single RGB Blinking

![img](img/0cf1e7028ce5e6f4f9c9df7d50c4a995.png)

1. Introduction

In this project, we intend to control a certain RGB of the ESP32 Easy Coding Board to be on and off. 

2. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

3. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

4. 5*5 RGB Dot Matrix

The RGB dot matrix has a total of 25 beads, and we mark them as number 0 to 24 from left to right and from top to bottom. 

The serial number is as follows:

![img](img/7756ebda7a04fb2f22d291dcd1457623.png)

5. Test Code

**Find code blocks:**

![img](img/12bc21c30e6c892da1a17df990d4df25.png)

Initialize RGB:

![img](img/53f48027e3d08a5ec3e0c4221d47a10a.png)

Set one RGB to light up in a certain color: 

![img](img/1edbbf615c7db919b572da642bbb59db.png)

Clear RGB display:

![img](img/fd53837d324e63cbb1ff6f6b6cd53314.png)

Refresh all RGB:

![img](img/072e85794e45aa2706bf0de24175ae2e.png)

**Build blocks:**

![img](img/f19bbdef681cbeea664b49c15a8010ce.png)

6. Test Result

The set RGB will light up once per second.

![img](img/f8f71addd63c7c6f09e6e93a3595e46f.png)

3 RGB LED Dot Matrix

![img](img/0cf1e7028ce5e6f4f9c9df7d50c4a995.png)

1. Introduction

Dot matrices are very commonplace in daily life. They have found wide applications in RGB advertisement screens, elevator floor display, bus stop announcement and so on.

The dot matrix of ESP32 Easy Coding Board contains 25 RGB in a grid. Previously, we have succeeded in controlling a certain RGB to light by integrating its position value into the test code. Theoretically, we can turn on many LEDs at the same time to show patterns, digits and characters. 

What’s more, we can also click ”show icon“ to choose the pattern we like to display. Last but not the least, we can design patterns by ourselves as well.

2. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

3. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

4. Test Code

**Find code blocks:**

![img](img/4032e017bf8ecb8d7214e6dcf8f6cac6.png)

**Build blocks:**

We set the icon to an arrow and set its brightness and color.

![img](img/c911a26ceb1d5491c8251bd004c338b8.png)

Set the full color brightness and delay time.

![img](img/aa3d90c76b63f910798b5578be65aee1.png)

**Complete code:**

![img](img/1da237c79a3a2687ca4f62f361cf6af3.png)

5. Test Result

After uploading test code, the dot matrix start to show arrows in many directions, and then it exhibits two light shows in full color with each for 5 seconds.

![img](img/7ab88973db2650f4d25716f9e2d1cc21.gif)

4 Programmable Buttons & Touch

![img](img/695a263fd2704e18d7feed137692f093.png)

1. Introduction

Buttons can be used to control circuits. In an integrated circuit with a button, the circuit is connected when the button is pressed and if you release the button, the circuit is open.

Capacitive touch detects the user's operation by measuring changes in capacitance. When you touch the capacitive sensing area, the charge of the human body affects the value of the capacitor, which can be sensed by the module due to this change.

ESP32 Easy Coding Board boasts three buttons: two programmable buttons (marked with A and B), and a reset button at back. By pressing the two programmable buttons, three different signals can be input. We can press button A or B or both so that the LED dot matrix shows A, B and AB respectively. 

Let’s get started!

2. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

3. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

4. Test Code 1

**Find code blocks:**

Find "if...then..." block to determine whether the buttons are pressed.

![img](img/07027f9177942e7e922faf412815dd25.png)

Add buttons and touch:

![img](img/1f3529a85a41b4faee21018ca7ac8351.png)

Choose button A or B in the condition.

![img](img/62119eb914fa1b9960867d2e8f68417f.png)

**Build blocks:**

![img](img/75b1fe72e55ba6278edf5bcab0624f37.png)

5. Test Result 1

After uploading test code and powering on, the 5x5 dot matrix shows A if button A is pressed, and shows B if button B is pressed, and shows AB if button A and B are pressed together. When the touching area is touched, it shows T.

![img](img/61dbbbdcf9767eb0f067ee35c92c30ea.png)

![img](img/b694932b7de0048a8a13c51f1a1d43df.png)

![img](img/9648b166c45be8a72d96ca9b8b4e15fc.png)

6. Test Code 2

Read the touching area analog values.

**Find code blocks:**

![img](img/f9f8fe3e08777a55414633b83dc228d5.png)

![img](img/d276a84f15414743a57ac0c932195693.png)

**Build blocks:**

![img](img/ae94e955cc4d9659a34de45268a7c265.png)

7. Test Result 2

After uploading test code and setting baud rate to 115200, when you touch this area, the value will reduce to about 10.

![img](img/7b7ae45b38772f911627890c9dde071e.png)

5  Passive Buzzer

![img](img/9d0c6c49067609427c2e62b5268cf4ee.png)

The board boasts an built-in passive buzzer, which is a device without an oscillating circuit so need an external driving signal to produce sound.

1. **Passive:** Unlike active buzzers, passive buzzers do not include a built-in oscillator circuit, so an external driving signal with a certain frequency is required. This is usually done by a microcontroller or other signal source.
2. **Frequency control:** The frequency of the driving signal determines the frequency at which the buzzer produces sound. By changing the frequency of the input signals, different tones of sound can be played.
3. **Applications:** Passive buzzers are widely used in various electronic devices to provide audio prompts or alerts, such as embedded systems, electronic products, alarm systems, etc.
4. **Driving:** Due to its passiveness, they have relatively low requirements for external drive signals, so they usually only need to provide enough current and the appropriate frequency.

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code

**Find code blocks:**

![img](img/895157b81b78c0573b77486bea61daaf.png)

**Build blocks:**

Play do, re, mi, fa, sol, la, si, or you may compose them by yourself.

![img](img/ffb185bda6ccb840cd17138d6a1959c1.png)

Integrated musics and songs:

![img](img/0f67eb911d018489d810ec67005fa45c.png)

**Complete code:**

![img](img/53a08e817681a0f9596f105f2da003d2.png)

4. Test Result 

Play do, re, mi, fa, sol, la, si, and a song.

6 Microphone

![img](img/0a220a3a627f88add9a5292e5cda430e.png)

Microphone is a device that converts sound into electrical signals, which is an important part of the audio field. It is widely used in voice recording, communication and audio playback.

Microphones can be divided into many types, including **Dynamic Microphone**, **Condenser Microphone**, **Wireless Microphone**, **USB Microphone** and **Laser Microphone**. 

In this project, we use a minimal capacitive microphone.

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code 1

**Find code blocks:**

![img](img/8df4223a920199cd763079b8c7a7f5af.png)

**Build blocks:**

![img](img/98735a71717889cabcad47aeffafa6c1.png)

4. Test Result 1

After uploading test code and setting baud rate to 115200, speak to the ESP32 Easy Coding Board or clap your hands or desks, and the analog value of sound will increase. The louder the sound is, the greater the value will be.

![img](img/ce87537c54e67d3f82ea825e0dd58316.png)

5. Test Code 2

We represent the sound on RGB dot matrix, and as the sound gets louder, more RGB will light up.

Initialize RGB.

![img](img/aa04be88281b2b8e5fde220ed800e9c1.png)

Determine the sound level and rate it.

![img](img/9a3ea7bc665ccf9101803ce6db2b5066.png)

RGB display:

![img](img/d8a385bbc7c63e300a54e4ab113627d5.png)

**Complete code:**

![img](img/a04e140360a6e353caf4c5d6a6fadd92.png)

6. Test Result 2

Upload test code and power on, and the louder the sound is, the more the RGB will light up.

![img](img/cd1e1afcb5b908e9b20bfbf3c91442fd.png)

![img](img/d520b6c07ec071744fcc3eb7241ec00d.png)

7 Temperature and Humidity Detection

![img](img/16852a0818b5c4cd2bdb481614ea2c43.png)

AHT11 temperature and humidity sensor is equipped on the board, which outputs digital signals. It uses special analog signal acquisition&conversion technology and temperature and humidity sensing technology to ensure that the sensor features good long-term stability and high reliability. The MCU on the ESP32 Easy Coding Board communicates with it via I2C.

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code

**Find code blocks:**

![img](img/af81635991bc0ed2597f080716945a4c.png)

![img](img/91ff82be2f6fa43fceddfc6c5a1a2284.png)

![img](img/2f4cc10ff40c70cdeba51705b05ea5be.png)

**Build blocks:**

![img](img/09b670f0ef45eeb1574bce2891152ab2.png)

4.  Test Result

After uploading test code, open the serial monitor and set baud rate, and the **temperature**, **humidity** and **Dewpoint** value will be printed.

![img](img/a9033da266d51aec79de9c24efeec81d.png)

8 MPU6050 Accelerometer and Gyroscope

![img](img/c782e6004b9ff2dd09a68f0dbe142783.png)

The MPU6050 is a six-axis motion processor that includes a 3-axis gyroscope and a 3-axis accelerometer. Two sensors integrated on a single chip that can detect static and dynamic object motion states, including angular speed, Angle and acceleration.

------

The MPU6050 is integrated with a 16-bit ADC that can simultaneously read data from six axes to measure diagonal speed and Angle, and can also infer acceleration information from the object. The MPU6050 also boasts a built-in temperature sensor used to measure the temperature of the chip, helping to monitor the temperature of the sensor during operation.

------

In addition, the MPU6050 is equipped with a fast Digital Motion Processor (DMP), which helps process raw data from the gyroscope and accelerometer to obtain the motion state of the object.

**Typical circuit diagram:**

![img](img/0a2e882d758d9d22bafe32726ca4518f.png)

|  #   | NAME | DESCRIPTION                                                  |
| :--: | :--: | :----------------------------------------------------------- |
|  1   | GND  | Negative interface (0V).                                     |
|  2   | VCC  | Positive interface (3.3V or 5V).                             |
|  3   | SDA  | I2C data line, connected to MCU, used to transmit data.      |
|  4   | SCL  | I2C clock line, connected to MCU, used to synchronize data transmission. |
|  5   | XDA  | I2C data line, connected to external extension sensors, used to transmit data. |
|  6   | XCL  | I2C clock line, connected to external extension sensors, used to synchronize data transmission. |
|  7   | AD0  | I2C Slave address. The sensor address is 0x69 at high and 0x68 at low. |
|  8   | INT  | External interrupt pin, detects the internal interrupt time of the MPU6050. |

- Operating voltage: 3.3V, 5V
- Static current: 5μA
- Rotating current: 3mA
- Maximum rotation speed: 2000°/s
- Acceleration range: ±2g, ±4g, ±8g, ±16g
- Temperature range: –10 ~ +65°C

MPU6050 can be used to measure the attitude of an object. Measurements of three angles can be provided: **roll**, **pitch** and **yaw**. It can also provide the acceleration of the object, and obtain the speed and position information of the object through calculation.

**Its three axises:**

![img](img/d4ec878ce6579c1fa90ed5b3f7bd4f36.png)

![img](img/bca124b77cd5d4b1e2555433cea63375.png)

The corresponding **Euler Angle** indicates the Angle of rotation of the object in three-dimensional space, and its coordinate axis can be adjusted arbitrarily.

Euler Angle consists of three angles, namely **Roll**, **Pitch** and **Yaw**.

|   Roll    |   Rotation Angle with x-axis as rotation axis   |
| :-------: | :---------------------------------------------: |
| **Pitch** | **Rotation Angle with y-axis as rotation axis** |
|  **Yaw**  | **Rotation Angle with z-axis as rotation axis** |

![img](img/c4f1a0de73deeefaafc83696ad56621a.png)

When acquiring Yaw, the gyroscope inside the MPU6050 is automatically calibrated to zero, which causes Yaw to drift to zero.

**Zero drift** means that the detected data will have an accidental small fluctuation. For example, the sensor value will automatically have an accidental small change. Even after a good algorithm, zero drift still exists, as it is limited by hardware. 

Solution: add a magnetometer to calibrate the MPU6050.

For more details, please refer to the MPU6050 data sheet:

[https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf](https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf)

[https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Register-Map1.pdf](https://www.invensense.com/wp-content/uploads/2015/02/MPU-6000-Register-Map1.pdf)

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code

**Find code blocks:**

![img](img/af81635991bc0ed2597f080716945a4c.png)

![img](img/6d4b455db85ed2c550ac1592ac16bd80.png)

**Build blocks:**

Initialize serial port and MPU6050.

![img](img/f115d6971f08e40bedd3a60ce1b913ab.png)

This block is used to update the data each time it is fetched.

![img](img/c432dcb1bed8ecf23d15634bc6fc76e2.png)

![img](img/de113a2dc7f4772b958a038760633838.png)

**Complete code:**

![img](img/59b490f5d8810ef434eeab9915eab5a5.png)

4. Test Result

After uploading code and powering on, Put ESP32 Easy Coding Board flatwise on the desk, press the reset button to initialize MPU6050, and wait 2 or 3 seconds. 

When the serial monitor shows values, the initialization is completed; and if values on each axis is not greater than 10, the initialization is correct; otherwise you need to re-initialize.

![img](img/f76470488f2793026eaa3a9777264b70.png)

![img](img/4b8d194edc5f4038c774def1b63c87a9.png)

9 Light Brightness

![img](img/db8f895ba85dd2552a29030fc4ab5a3b.png)

Photoresistors measure light intensity and are commonly used to detect brightness in the surrounding environment.

**Working principle:** This module is designed by the light-sensitive materials. There are two main types: photoresistor and photodiode.

- **Photoresistor:** The resistance of a photoresistor varies with the intensity of ambient light. For one photoresistor, the stronger the ambient light is, the lower the resistance will be.
- **Photodiode:** The current output of a photodiode is proportional to the intensity of the incident light. The electrical signals they produce can be used to measure light brightness.

**Applications:** Photoresistors are widely applied to various fields, including light control systems, lighting systems, camera exposure control, light monitoring, automatic adjustment of screen brightness, etc.

**Unit of brightness:** They usually measure light intensity in luminance units (such as Lux). Luminance represents the luminous flux per unit area.

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code

**Find code blocks:**

![img](img/af81635991bc0ed2597f080716945a4c.png)

![img](img/a34af46f2d6c4adcd279577d384c4140.png)

**Build blocks:**

![img](img/9b4f562e8a890d3e1dc381beda252483.png)

4. Test Result

Upload the test code and open the serial monitor. When the light intensity detected by the sensor changes, the sensor values will also change.

![img](img/d9f8b4dc97dcc96b69404cd6af8eab3d.png)

![img](img/d4dd0d09cb97e98597d05b8c7dc05f8d.png)

10 Read SD Card

![img](img/dbc96c166250e3277c3d9553eedf0ed6.png)

The SD card module is used in conjunction with the MCU on the ESP32 Easy Coding Board for reading and writing data on the SD (Secure Digital) card. This module makes it easier to use SD cards to store and access data in projects.

- **Function:** SD card module allows the ESP32 Easy Coding Board to communicate with the SD card to achieve data reading and writing. This is very useful for data logging, file storage, logging, etc.
- **Interface:** The SD card module usually connects to the ESP32 Easy Coding Board using the Serial Peripheral Interface (SPI) interface. It needs to be connected to the corresponding pin of the ESP32 Easy Coding Board, For example, MOSI (Master Out Slave In), MISO (Master In Slave Out), SCK (Serial Clock), and CS (Chip Select).
- **SD card type:** SD card modules are generally compatible with various types, including standard SD cards, SDHC cards (High Capacity), and SDXC cards (eXtended Capacity).

1. Components

| ESP32 Easy Coding Board*1           | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png)  |
| ----------------------------------- | ------------------ |
| USB type C cable *1                 | ![img](img/26110bd63d838c6377849040b83e3a08.png)  |
| SD card *1(not included in the kit) | ![img](img/4f70bcfd89ff384a12d0485c91f63c8f.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

Insert the SD card into the slot.

![img](img/76163cdf839040406681820aacee0475.png)

![img](img/80b3aa025cccd44caa354ad0d2956010.png)

3. Test Code

**Find code blocks:**

![img](img/c0552cba50bec2bb8e0c8b79016bdca2.png)

Initialize the serial monitor and SD card.

![img](img/eed2df7b094e85a16d5b6b8ab42b2c38.png)

Refresh the SD data before using.

![img](img/bd795191701ef148993854501fb3021d.png)

**Read SD card type**

![img](img/0b423ee426ccfad1731d395164cbb4dc.png)

Serial monitor outputs SD type:

![img](img/6f69553ae20d4ce1e41df5c0a16399de.png)

**Read SD card message**

![img](img/b361a714f678faf06b680a5c97fda77c.png)

![img](img/532312c650f787990abc6f1b31db8a62.png)

Serial monitor outputs messages:

![img](img/1cf023931e9089a3746e2322aa75c81c.png)

**File**:

Determine whether there is a ‘’file.txt‘’ file in SD card.

![img](img/35c090aad4f8f8e7b66be865e22ace57.png)

If there is no ‘’file.txt‘’, it create a file and input “hello,world” in a new line.

![img](img/ad4b85727d676a2577e264cfd0aaee8a.png)

After that, read the content in ‘’file.txt‘’.

![img](img/f597166b6cac865f382f52e566106a6c.png)

Read all list files in SD card, including hidden files.

![img](img/10451ce84e7e1dc26f45fcdbd71f9ab0.png)

Delete this ‘’file.txt‘’.

![img](img/74bde7aecbf49401cdf8f3e2121d9706.png)

**Complete code:**

![img](img/4a4b43efbbd304584ec05f0fde3a01fd.png)

Serial monitor outputs:

![img](img/4bee2f4a6ab0b20ab9f5107984893871.png)

11 Read ESP32 Easy Coding Board Current

![img](img/2da227a2e63416e1f6dd94baa3c9eb4f.png)

ESP32 Easy Coding Board boasts a built-in current measurement module (only measure USB power supply and PH2.0 interface power supply) to measure current by a resistive current sensor. 

Resistive current sensor is commonly used to monitor the current value by measuring the voltage drop generated by the current through the resistance. The working principle of such sensors is based on Ohm's law, which states that when a current passes through a resistor, the voltage generated at both ends of the resistor is proportional to the current.

![img](img/832bba6595b35e2c6b63b43ec42359fb.png)

1. **Current sensing:** Resistive current sensor contains a current sensing element, usually, a resistor. When current passes through this resistor, a voltage drop will be generated at both ends of the resistor, the magnitude of which is proportional to the strength of the current.
2. **Voltage output:** By measuring the voltage drop at both ends of the resistor, the sensor can provide a voltage signal that is related to current. This voltage signal can be digitally processed by devices like an analog-to-digital converters (ADC).

Resistive current sensors are widely applied to power system monitoring, power consumption measurement of electronic devices, electric vehicle current monitoring and so on.

1. Components

| ESP32 Easy Coding Board*1 | ![img](img/4f8ac5efacc04d3f15e4f804abe70fc0.png) |
| ------------------------- | ----------------- |
| USB type C cable*1        | ![img](img/26110bd63d838c6377849040b83e3a08.png) |

2. Connection

Connect the ESP32 Easy Coding Board to your computer via USB cable.

![img](img/a4dc84d7f522d094ab4964b4721e0be4.png)

3. Test Code 1

**Read current value:**

![img](img/6fe6280d99638de85029008a5b0bc120.png)

**Complete code:**

![img](img/f1e692b195a31232855914a5917c764c.png)

4. Test Result 1

After uploading test code, open the serial monitor and you will see the current value is 0. Because many modules are not working on the board, so the current is close to 0.

![img](img/5429cd95980c433e8637209a321ef913.png)

5. Test Code 2

Enable RGB dot matrix and then measure the current value.

Initialize the serial monitor and RGB dot matrix.

![img](img/11e9caa3dd539f00a8adb12b52c01dec.png)

First measure 10 RGB beads.

![img](img/0bb06d5e3ec3b1fe85c514b87d001a6e.png)

Then measure 18 RGB beads.

![img](img/8de8b3a5f13fe04dc374b54b115eb6d1.png)

Last measure 25 RGB beads.

![img](img/fb92b17a8a6e32f4dd457a6bc4275057.png)

**Complete code:**

![img](img/4f32fc1463133d03992f0ff3f71996c8.png)

6. Test Result 2

Upload test code and you will find that the more the beads are, the larger the current will be.

![img](img/b22d109c823d56aa84006181841386a0.png)

7. Test Code 3

The conversion of current to power: power (P) equals current (I) times voltage (V).

**P = IV**

- *P* is power, unit: Watt(W)
- *I* is current, unit: ampere(A)
- *V* is voltage, unit: volt(V)

This formula is suitable for DC circuits. 

For AC circuits, power calculation may require more complex formulas due to power factor.

In a circuit, power describes the conversion of electrical energy. Input current and voltage values into the above formula and you can get real-time power values. This is commonly used for energy monitoring, power system management and equipment power consumption evaluation.

The power voltage of ESP32 Easy Coding Board is 3.3V, so we only need to measure the current and multiply it by 3.3 to get the power of the Board of this time.


------

**Find code blocks:**

Create variables **P** and **I**.


![img](img/603ba0ec54833da5e008579e80773dd2.png)

![img](img/bf2925bb49b892ea50f34da98bdaebbf.png)

![img](img/138d6da2dee2b41bb9ddc40731b4cabf.png)

Assign the read current value to variable I.

![img](img/28006926353d2e311c5167f2a1fa87d6.png)

Variable **I** multiplies by 3.3 is the power of the ESP32 Easy Coding Board (the board voltage is 3.3V).

![img](img/4bd35043342c25b0b113c2a7c128641a.png)

**Complete code:**

![img](img/ba5fe3631c4aaa98011c621395270e2a.png)

8. Test Result 3

Upload code and open serial monitor to set baud rate. The more the beads are, the greater the current value and power will be.

![img](img/2ebecb69f942006aa38d48dc9d15d491.png)

12 WiFi Wireless Communication

ESP32 Easy Coding Board is built with Wi-Fi (2.4G) and Bluetooth (4.2) to easily connect to a Wi-Fi network and communicate with other devices in the network, so you can use this Board to display web pages in your browser.

![img](img/acc2f14244d38b448897ff5397b2de5d.png)

ESP32 Easy Coding Board WiFi Function:

- **Base mode** (STA / Wi-Fi Client mode): ESP32 Easy Coding Board is connected to a Wi-Fi hotspot (AP).
- **AP mode** (Soft-AP / Wi-Fi hotspot mode): Other Wi-Fi devices connect to ESP32 Easy Coding Board.
- **AP-STA mode**: ESP32 Easy Coding Board is both a Wi-Fi hotspot and a Wi-Fi device connected to another Wi-Fi.
- These modes support multiple security modes: WPA, WPA2, WEP, etc.
- Wi-Fi hotspots can be searched (active and passive scanning).
- Support hybrid mode monitoring of IEEE802.11 Wi-Fi data packets.

------

For more wifi reference, please visit: [https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_wifi.html](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_wifi.html)

Espressif Official: [https://www.espressif.com.cn/en/home](https://www.espressif.com.cn/en/home)

![img](img/b4fdfdedf9494c9535fce6a6be913113.png)

------

WiFi Web Page

Click the extension icon to add the library.

![img](img/7cb2c9917c343b06bf195888204651dc.png)

![img](img/77304610624761f9eae57e5580c3d610.png)

Load Web Page Editing PRO.

![img](img/d6b277643f8c60696259c8eb4bd9533e.png)

You will see code blocks:

![img](img/21f70beae826af2028d916eab1a3afa3.png)

Connect to a wifi and input your wifi name and passwords. After connecting, the IP address will be printed on the serial monitor. 

![img](img/d7de9119b64c5894d0c3006c1f3003b6.png)

![img](img/8e1581c2c9209e3f27b228791621293a.png)

Set up a web component and name as **temperature** in the unit of ℃.

![img](img/baa152c1b25963a0c2800f06b7571e44.png)

![img](img/b18704ff30a7b4a504086c56010e2676.png)

Add a button module and name as **button**.

![img](img/21da077c0a0ecd203ac21cc8682dcd0f.png)

![img](img/a1977b46870d355d0156b640d08fd439.png)

**Complete code:**

![img](img/20434681f6ce3f6ca772dadf9882d3be.png)

As long as connecting to Wi-Fi, you may use the Web Server Library of ESP32 Easy Coding Board to provide web page. In the example, we set up a simple web page to display a certain temperature value.

------

**Open your browser to check and visit the IP address of ESP32 Easy Coding Board. Herein, you may access to “http://[IP address of ESP32 Easy Coding Board]” to visit its website.**

**NOTE: When PC, mobile phone and ESP32 Easy Coding Board are connected to one network, this website(your own IP address of ESP32 Easy Coding Board) can be accessed via PC and mobile at the same time.**

PC:

![img](img/a6ae13afc3f26dc52a57ca05a8916a8e.png)

Mobile:

![img](img/0c04c5513169733e22b726164218bee8.png)