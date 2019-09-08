# IDD-Fa18-Lab1: Blink!

**A lab report by Johnway Yih. Student**

## Part A. Set Up a Breadboard
![Breadboard Setup](https://github.com/JwayYih/IDD-Fa18-Lab1/blob/master/Breadboard%20Setup.jpg)

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

Brown black brown
 
**b. What do you have to do to light your LED?**

In order to light the LED, I must complete the circuit, by pressing and holding down the switch.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

Have delay commands for the high and low state.
  digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
  
**b. What line(s) of code do you need to change to change the rate of blinking?**

Change the number in the delay. Units are in ms.

**c. What circuit element would you want to add to protect the board and external LED?**
 
 Add a resistor
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

At a delay of ~10ms, I can no longer perceive blinking

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[BlinkMyWay.ino](https://github.com/JwayYih/IDD-Fa18-Lab1/blob/master/BlinkMyWay.ino)

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[My Blink Video](https://photos.app.goo.gl/5hWD3orHpzHwkZtq7)

## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes.  The potentiometer is a acting as a voltage resistor.  As I turn the potentiometer, the resistance increases/decreases influence the amount of current going through the circuit and how bright the LED will glow. 
[Fade/Glow Video](https://photos.app.goo.gl/LDEgweeLkWETSJTz5)

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

Assign the proper pin (11)
int led = 11;           // the PWM pin the LED is attached to

**b. What is analogWrite()? How is that different than digitalWrite()?**

analogWrite allows us to variably adjust the voltage input as opposed to only High (5v or 3v) or Low (Ground)

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

![Microphone Board](https://github.com/JwayYih/IDD-Fa18-Lab1/blob/master/Microphone%20Board.jpg)

[Schematic](https://github.com/JwayYih/IDD-Fa18-Lab1/blob/master/Schematic%20Sketch.jpg)

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

Yes, there does seem to be a processor, circled in red.  The device is a microphone, so I believe some sort of audio input is being transferred down the black wire on the left, processed, and then outputted through the RGWB cables on the top right.

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

There must be some sort of microphone sensor in the neck of the device which is transferring a signal down the black wire.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

The device is powered from the 5V/Ground connect on the top right thicker black cable.  This power is drawn from a USB output port, such as a computer/laptop.  Power seems to be managed/transformed through the various resistors and capacitors on the board.  There is a switch @ SW1 which controls on/off.

**d. Is information stored in your device? Where? How?**

I don't believe information is stored on this device.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

I connected it at two locations
1) Attached where an exisiting LED already was and simply placed it in parallel.
2) Attached where I assume output signals are being sent back to the laptop.

### 3. Build your light!

**Make a video showing off your Frankenlight.**
![Franken Light](https://github.com/JwayYih/IDD-Fa18-Lab1/blob/master/Franken%20Light.jpg)

[Franken Light Video](https://photos.app.goo.gl/yomcpruqp3SwFURt8)
Connected at signal output pins? And attaching to onboard LED location

**Include any schematics or photos in your lab write-up.**
