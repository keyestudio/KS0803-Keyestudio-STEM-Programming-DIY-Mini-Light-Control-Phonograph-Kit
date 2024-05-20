# ESP32 Easy Coding Board Phonograph Projects

## 1. Projects

### 1. Photoresistor: Light Detector

#### Photoresistor

![img](img/KS0028-1.jpg)

Photoresistor, also known as photoelectric sensor, is a sensor that converts optical signals into electrical ones (voltage, current, resistance, etc.) through photoelectric devices. In the circuit, there is a resistor whose resistance value depends on light intensity.

The photoresistor enters the circuit in series, and we add an appropriate voltage. When there is no light, the resistance is infinity, so the circuit is close to open. When there is light, its resistance reduces and the current increases. If the light is bright enough, it is equivalent to a short circuit.

Herein, we write code on the ESP32 Easy Coding Board to read the value of the photoresistor.

#### Principle Diagram

Light hits the photoresistor. The harder the light is, the smaller the resistance value will be, and the greater the voltage (VCC passing through the resistor) will be.

![img](img/couy21.png)

------

#### Wiring Diagram

![img](img/couj1.png)

------

#### Parameters

- Voltage: 3~5V

- Current: 0.2mA
- Power: 1mW
- Spectral peak: 540nm
- Bright resistance (10lux): 5~10KR
- Dark resistance: 0.5MR

------
#### Test Code 1

- Initialize the serial port.

  ![img](img/cou1.png)

- Read the analog value of pin 14.

  ![img](img/cou2.png)

- Complete code

  ![img](img/cou3.png)

------

#### Test Result 1

A hole is reserved on the phonograph and the photoresistor is under it, as shown below:

![img](img/cou4.png)

------

Move the tone arm above the hole, and open the serial monitor to set baud rate to 115200.

![img](img/cou5.png)

And the monitor prints:

![img](img/cou6.png)

------

If we move the tone arm away, 

![img](img/cou7.png)

the serial monitor will print analog values of the photoresistor.

![img](img/cou8.png)

------

#### Test Code 2

If no light is detected, light up RGB dot matrix; when there is light, turn off RGB dot matrix.

- Initialize the serial port and RGB dot matrix.

  ![img](img/cou9-1.png)

- Define a variable to store the detected light values.

  ![img](img/cou9.png)

  ![img](img/cou10.png)

  ![img](img/cou11.png)

- Assign the detected light value to the variable and print it.

  ![img](img/cou12.png)

- Determine whether the value is greater than 10. If yes, turn off RGB dot matrix. If not, light up RGB dot matrix.

  ![img](img/cou13.png)

- Complete code

  ![img](img/cou14.png)


#### Test Result 2

  Put the tone arm above the hole position, and the RGB dot matrix will light up.

![img](img/cou15.png)

Remove the arm and RGB dot matrix will turn off.

![img](img/cou16.png)

Put the tone arm on the turntable of the phonograph, it covers the hole so the photoresistor detects no light. Remove the arm, and light hits the photosensor. We can know whether the phonograph plays music by checking whether the photosensor detects light. Pay attention that if you put the phonograph in a completely dark environment, it will play music because the photoresistor cannot detect light.

------

### 2. Power Amplifier: Music Box

#### Power Amplifier

The power amplifier mainly consists of a potentiometer, a speaker, and an audio amplifier chip. This module amplifies the small audio signals about 8.5 times, and plays audio through its built-in speaker. Therefore, it can be used to play music or as an external amplifier for some music players.

![img](img/KS0374-4.jpg)

#### Principle Diagram

![img](img/cou17.png)

------

#### Wiring Diagram

![img](img/couj1.png)

------

#### Test Code 1

- Find **Music** Block.

  ![img](img/cou18.png)

- Set pin to IO4.

  ![img](img/cou19.png)

- Set frequency.

  ![img](img/cou20.png)

-  Complete code: 7 basic tones

  ![img](img/cou21.png)

#### Test Result 1

The amplifier will play the 7 basic tones. 

Rotate the potentiometer on the module to adjust the volume.

![img](img/cou22.png)

#### Test Code 2

![img](img/cou23.png)

------

#### Test Result 2

The module plays the set music.

------

### 3. Light Control Phonograph

#### Introduction

![img](img/cou24.png)

In this project, we try to simulate a real phonograph: when the tone arm is placed on the turntable, it plays music; When we remove it, it finishes the current music and then stops singing.

#### Test Code

- Initialize RGB dot matrix.

  ![img](img/cou25.png)

- Define a variable to store the detected light value.

  ![img](img/cou9.png)

  ![img](img/cou10.png)

  ![img](img/cou11.png)

- Assign the detected light value to the variable.

  ![img](img/cou26-1.png)

- Determine whether the value is greater than 10. If yes, turn off the RGB dot matrix and the music. If not, turn on the RGB dot matrix and play music.

  ![img](img/cou26.png)

- Complete code

  ![img](img/cou27.png)

#### Test Result

Put the tone arm above the hole position, and it starts to play music with RBG lighting up. Remove the arm, and the music and RGB dot matrix both turn off.

![img](img/cou28.png)

------

### 4. Button Control Phonograph

![img](img/cou29.png)

In this project, we control the phonograph with buttons. 

There are two button (A and B) on the board. Herein, we utilize these buttons to have a switchover of songs: press A for the previous song with a left arrow showing on the dot matrix; press B for the next song with a right arrow showing on the dot matrix.

------

#### Test Code

- Initialize the RGB dot matrix.

  ![img](img/cou25.png)

- Define a button-control block **“f_button”** to represent the codes of button.

  ![img](img/cou30.png)

  ![img](img/cou31.png)

- Show “<” when A is pressed; show “>” when B is pressed.

  ![img](img/cou32.png)

- Define two variables **”button_value”** and **”play“**.

  ![img](img/cou33.png)

  ![img](img/cou34.png)

- We have enrolled four song numbered as 0, 1, 2 and 3. Variable **”button_value”** stores the song number.

  1. To ensure button_value is within 0~3, we set button_value to 0 when it is less than 1, and set it to 3 when it is greater than 2. 

  2. When we press button A/B, we set **“play”** to 1 to play music.

  Press button A and button_value-1

  ![img](img/cou35.png)

  Press button B and button_value+1

  ![img](img/cou37.png)

  Complete button-control code:

  ![img](img/cou38.png)

- Read the value of **”button_value”** to determine which song should be played. After the song is finished, set play to 0 to have a pause.

  ![img](img/cou39.png)

-  Complete code

   ![img](img/cou40.png)

#### Test Result

Music is being played:

![img](img/cou41.png)

Pause:

![img](img/cou42.png)

The next song:

![img](img/cou43.png)

The previous song:

![img](img/cou44.png)

------

## 2. FAQ

### Q: Battery model?

A: Four AAA batteries. Please install the batteries in the correct direction rather than reverse them! For younger students, please be accompanied by your parents!

------



### Q: Errors occur when ESP32 burns code?

A: 

- Please check whether the USB port number is correct.
- Please ensure the main board model is available. 

------



### Q: Expand to external modules?

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
