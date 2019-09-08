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
[My Glow Video](https://photos.app.goo.gl/LDEgweeLkWETSJTz5)

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
Assign the proper pin (11)
int led = 11;           // the PWM pin the LED is attached to


**b. What is analogWrite()? How is that different than digitalWrite()?**
analogWrite allows us to variably adjust the voltage input as opposed to only High (5v or 3v) or Low (Ground)

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
