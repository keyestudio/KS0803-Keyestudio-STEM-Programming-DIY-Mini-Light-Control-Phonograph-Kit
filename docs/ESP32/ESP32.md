# ESP32 Easy Coding Board Phonograph Projects

## 1. Projects

1. Photoresistor: Light Detector

Photoresistor

![img](img/96c8270974492cfeccf977e05847c900.jpg)

Photoresistor, also known as photoelectric sensor, is a sensor that converts optical signals into electrical ones (voltage, current, resistance, etc.) through photoelectric devices. In the circuit, there is a resistor whose resistance value depends on light intensity.

The photoresistor enters the circuit in series, and we add an appropriate voltage. When there is no light, the resistance is infinity, so the circuit is close to open. When there is light, its resistance reduces and the current increases. If the light is bright enough, it is equivalent to a short circuit.

Herein, we write code on the ESP32 Easy Coding Board to read the value of the photoresistor.

Principle Diagram

Light hits the photoresistor. The harder the light is, the smaller the resistance value will be, and the greater the voltage (VCC passing through the resistor) will be.

![img](img/e08561c3a64ee7ac18d37f4c4302f932.png)

------

Wiring Diagram

![img](img/72deb8ab7752a63e61aa17d47aa25da1.png)

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

  ![img](img/0501ee816510ccd3a3ea9a6621d3f2f4.png)

- Read the analog value of pin 14.

  ![img](img/b2c4964dd51e15fee46f8b6d10b62062.png)

- Complete code

  ![img](img/9236048a14a0f946e6e8a1dfe6a22cb6.png)

------

Test Result 1

A hole is reserved on the phonograph and the photoresistor is under it, as shown below:

![img](img/8393d254d21c9e3b8c02902bd5b60ab9.png)

------

Move the tone arm above the hole, and open the serial monitor to set baud rate to 115200.

![img](img/53a805c8df0c01aadacc25a115e56234.png)

And the monitor prints:

![img](img/0ef95a52d914e88f35ecaf20dc3a716c.png)

------

If we move the tone arm away, 

![img](img/3ea894f3ec6bad4bfe9888c6f75bcb7b.png)

the serial monitor will print analog values of the photoresistor.

![img](img/f98cc0ede1157ff459b2cd38dcb9ecb8.png)

------

Test Code 2

If no light is detected, light up RGB dot matrix; when there is light, turn off RGB dot matrix.

- Initialize the serial port and RGB dot matrix.

  ![img](img/517015029e2f5703e30a0e62c4941994.png)

- Define a variable to store the detected light values.

  ![img](img/d482380b329f53140904ea041261eccf.png)

  ![img](img/820d4b16570241079034d2630bf57aaa.png)

  ![img](img/74e40916d59b46635710f64de425903c.png)

- Assign the detected light value to the variable and print it.

  ![img](img/2629312ca1a0c9eb5c132f01487a1018.png)

- Determine whether the value is greater than 10. If yes, turn off RGB dot matrix. If not, light up RGB dot matrix.

  ![img](img/f9c482dd7c9707c5f485b89ba9026ccc.png)

- Complete code

  ![img](img/b22b99bf33b993510655f36ae9320d7c.png)


Test Result 2

  Put the tone arm above the hole position, and the RGB dot matrix will light up.

![img](img/849b3f27bb97c1c8e1419b28591f3d3f.png)

Remove the arm and RGB dot matrix will turn off.

![img](img/e6d18fbd739610830a9775bca62d78f6.png)



------

2. Power Amplifier: Music Box

Power Amplifier

The power amplifier mainly consists of a potentiometer, a speaker, and an audio amplifier chip. This module amplifies the small audio signals about 8.5 times, and plays audio through its built-in speaker. Therefore, it can be used to play music or as an external amplifier for some music players.

![img](img/d462bd9e090272cad154dc8e041bd869.jpg)

Principle Diagram

![img](img/80765898fa3afe1f45fad42a07e1919a.png)

------

Wiring Diagram

![img](img/72deb8ab7752a63e61aa17d47aa25da1.png)

------

Test Code 1

- Find **Music** Block.

  ![img](img/0fa96cac5569edc4927999c63be519b8.png)

- Set pin to IO4.

  ![img](img/33ecfa98348b32194e92ac633b35488a.png)

- Set frequency.

  ![img](img/d6994333781d81b4694e82c5f73432a5.png)

-  Complete code: 7 basic tones

  ![img](img/30a1398b0d744e6ae8847f383241f1b9.png)

Test Result 1

The amplifier will play the 7 basic tones. 

Rotate the potentiometer on the module to adjust the volume.

![img](img/28ded1e8523e76435bd31a4b3eed0422.png)

Test Code 2

![img](img/5f870c69fe83eb84663e53be5f5cb661.png)

------

Test Result 2

The module plays the set music.

------

3. Light Control Phonograph

Introduction

![img](img/d83fdd7f1ec60e744c58c4c95c92c1ef.png)

In this project, we try to simulate a real phonograph: when the tone arm is placed on the turntable, it plays music; When we remove it, it finishes the current music and then stops singing.

Test Code

- Initialize RGB dot matrix.

  ![img](img/bc5b03b593b4cfdf0614d3694c6759e0.png)

- Define a variable to store the detected light value.

  ![img](img/d482380b329f53140904ea041261eccf.png)

  ![img](img/820d4b16570241079034d2630bf57aaa.png)

  ![img](img/74e40916d59b46635710f64de425903c.png)

- Assign the detected light value to the variable.

  ![img](img/28b8654be965f70a52c36cac4cc705c0.png)

- Determine whether the value is greater than 10. If yes, turn off the RGB dot matrix and the music. If not, turn on the RGB dot matrix and play music.

  ![img](img/94e0c4bcb23abaa281793a4c96889d40.png)

- Complete code

  ![img](img/eba8adfebe147c16eaefef0f4f9dcd89.png)

Test Result

Put the tone arm above the hole position, and it starts to play music with RBG lighting up. Remove the arm, and the music and RGB dot matrix both turn off.

![img](img/d731e3862f5630ea3979fe550f19bac8.png)

------

4. Button Control Phonograph

![img](img/e0f37d12fdf93381c761ab0f066b6583.png)

In this project, we control the phonograph with buttons. 

There are two button (A and B) on the board. Herein, we utilize these buttons to have a switchover of songs: press A for the previous song with a left arrow showing on the dot matrix; press B for the next song with a right arrow showing on the dot matrix.

------

Test Code

- Initialize the RGB dot matrix.

  ![img](img/bc5b03b593b4cfdf0614d3694c6759e0.png)

- Define a button-control block **“f_button”** to represent the codes of button.

  ![img](img/339121ae4046ac3026f28ec2cd4be999.png)

  ![img](img/2b74cc63e177b101f0490ef87716fb69.png)

- Show “<” when A is pressed; show “>” when B is pressed.

  ![img](img/03015a748e0bf0c06b1dcb48233f73cb.png)

- Define two variables **”button_value”** and **”play“**.

  ![img](img/430f5d0c7f639a802b37ac560c90abc7.png)

  ![img](img/4e07968cb152a0c7cea1bbedc8613dfc.png)

- We have enrolled four song numbered as 0, 1, 2 and 3. Variable **”button_value”** stores the song number.

  1. To ensure button_value is within 0~3, we set button_value to 0 when it is less than 1, and set it to 3 when it is greater than 2. 

  2. When we press button A/B, we set **“play”** to 1 to play music.

  Press button A and button_value-1

  ![img](img/11d63fd6c722ca8e2c79e9152023e247.png)

  Press button B and button_value+1

  ![img](img/f587a0261a552851165571909806483d.png)

  Complete button-control code:

  ![img](img/06dd1a67b353cdbd7dd015f2ca492022.png)

- Read the value of **”button_value”** to determine which song should be played. After the song is finished, set play to 0 to have a pause.

  ![img](img/fa16b283c44c691f205713a590c7f971.png)

-  Complete code

   ![img](img/ec291e08d2d1d76122d676b1f71e49ea.png)

Test Result

Music is being played:

![img](img/38ed96deb6f6fb9fcdf1c158395bf707.png)

Pause:

![img](img/4e41cd9e34a1a44223f0de557969eb23.png)

The next song:

![img](img/0f56dd025a02eb8e378ab49ba49b4c2d.png)

The previous song:

![img](img/9c7ab4bf5b4b5080e99a7f5956a3513b.png)

------

## 2. FAQ

Q: Battery model?

A: Four AAA batteries. Please install the batteries in the correct direction rather than reverse them! For younger students, please be accompanied by your parents!

------



Q: Errors occur when ESP32 burns code?

A: 

- Please check whether the USB port number is correct.
- Please ensure the main board model is available. 

------



Q: Expand to external modules?

A: It can expand to external modules. For details, please follow the ESP32 pin instructions to ensure external modules can normally work.

------



## 3. Resources

Keyestudio official:

[https://www.keyestudio.com/](https://www.keyestudio.com/)

Keyestudio wiki:

[https://wiki.keyestudio.com/Main_Page](https://www.keyestudio.com/)

Arduino official:

[https://www.arduino.cc/](https://www.keyestudio.com/)

ESP32 espressif official:

[https://www.espressif.com/](https://www.keyestudio.com/)
