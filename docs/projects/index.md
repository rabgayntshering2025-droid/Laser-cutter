# projects 

## Laser cutter

### A machine to cut your design.




A laser cutting machine is a tool that uses a very focused beam of light (a laser) to cut or engrave materials like wood and acrylic.

<img class="profile-photo" src="https://drive.google.com/thumbnail?id=1vTsu-DluIAqYmpiNH3S7Qzt4XLyVB8MT&sz=w400" alt="Profile Photo">

### How it works 

You create a design on a computer (like a drawing or logo).
Send that design to the laser machine.
The machine follows the design and uses a laser beam to:
Cut through material, or
Engrave  the surface

## What can it cut or engrave?
### -Wood
### -Acrylic (plastic)
### -Paper & cardboard

## *Example uses*

### Making signs and nameplates
### Custom gifts (engraved wood, glass)
### School projects
### Small business products (keychains, decorations)

<img class="profile-photo" src="https://drive.google.com/thumbnail?id=1vTsu-DluIAqYmpiNH3S7Qzt4XLyVB8MT&sz=w400" alt="Profile Photo">

## Vector (Cutting)

### Vector = cutting lines

The laser follows thin lines in your design
It cuts all the way through the material
Like using a blade or scissors, but with a laser

## 👉 Example:

### -Cutting out a circle from wood
### -Making shapes like keychains or letters


<img class="profile-photo" src="https://drive.google.com/thumbnail?id=1vTsu-DluIAqYmpiNH3S7Qzt4XLyVB8MT&sz=w400" alt="Profile Photo">

## Engraving 

### Engrave = surface marking

### -The laser moves back and forth (like a printer)
### -It does NOT cut through, only burns the surface
### -Creates designs, text, or images

## 👉 Example:

### -Writing a name on wood
### -Adding a photo or logo



# Quick difference>

## 	What it does.

### Vector

#### -Cuts lines
#### -Goes through
#### -Shapes, outlines

### Engrave	
#### -Burns surface
#### -Images, text, logos

	
<img class="profile-photo" src="https://drive.google.com/thumbnail?id=1vTsu-DluIAqYmpiNH3S7Qzt4XLyVB8MT&sz=w400" alt="Profile Photo">

- Basically for the LED to glow the circuit should be completed (i.e the two end ot the LED terminal should be connected to the positive and negative terminal of the power)
  - When the switch is off, the LED is disconnected from power i.e both side is connected to the negative terminal of the battery.
  - When the switch is on, the circuit is completed and the LED glows.

### Schematic.

ThinkerCad can also be used to generate schematic from the design we make.

> What is Schematic?


>   A schematic, or schematic diagram, is a representation of the elements of a system using abstract, graphic symbols rather than realistic pictures.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/schematic.png?ref_type=heads)
<p class="drive-image-caption">Figure </p>


The schematic shown above is symbolic representation of the circuit we have designed earlier. Schematic can be used to learn the symbols of the components used our design.
- The numbered symbols are:
    1. Resistor.
    2. LED
    3. Switch
    4. Battery.

# Introduction To Arduino.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/arduino-uno2.png?ref_type=heads)
<p class="drive-image-caption">Figure </p>


> What is Arduino?

>   Arduino is an open-source hardware and software company, project, and user community that designs and manufactures single-board microcontrollers and microcontroller kits for building digital devices.

To understand more about arduino, [Click Here](https://www.youtube.com/watch?v=CSx6k-zXlLE).

## Arduino in TinkerCad.

Tinkercad provides various other controllor but we would be focusing more on Arduino UNO Board.
- Arduino is available is various range of board version such as Arduino UNO, Arduino Nano, Arduino Mega etc.

To start programming arduino:
1. First add the arduino Board to the design from the component list.
2. Before that lets understand the different views, we can select in the tinkercad platform.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/top_corner.png?ref_type=heads)
<p class="drive-image-caption">Figure</p>


On the top right corner, we can select the views such as:

      1. Circuit view: Where we can make design.
      2. Schematic view: Whatever circuit is designed in the circuit view can be represented with components symbols.
      3. Component List: All the components added in the circuit will be listed in this view.
      4. Code: This will let the user write codes to perform simulation. Options for Block and text programming are available.
      5. Start Simulation: Whenever a design is ready, we can test the design by clicking the start simulation button.
      6. Send To: enables users to share their work.


### Blinking LED with Arduino.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/pin_13.png?ref_type=heads)
<p class="drive-image-caption">LED</p>


As we have learned, Arduino has Digital and analoge pins. One of the digital pin (i.e Pin 13) has a builtin LED marked red in the picture above.

- Therefore the key point to remember is that we will be using pin number 13 to controll the builtin LED.

The block program to blink an LED on and off with deslay of 1 second each is.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/block_code.png?ref_type=heads)
<p class="drive-image-caption">Block Code</p>


- First block: Will send a HIGH signal to the builtin LED pin (i.e pin number 13).
- Second block: The first block will be executed and and it will wait for one second before it executes the next block.
- Third block: Similar to first block, now it will send a LOW signal to the builtin LED pin.
- Fourth Block: Wait for one second.

This block of code will repeat multiple times, until the simulation is stopped.

Another Interesting feature of Tinkercad is that it will generate a text program, which can be directly uploaded to the real arduino board.

When ever a block program is created, it will simultaneously generate a text program.

The text program for the blinking LED is given Below:

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/text_code.png?ref_type=heads)
<p class="drive-image-caption">Text Code</p>

In text programming, by default arduino code will have a void setup method and void loop method.
The difference between the block code and text code is mostly the **void setup()** :

- The setup method is executed on once when the a system or a code is initiated.
- Most of defining and initializing parameter work is done in this method.
  - The parameter/pin defined here is the LED_BUILTIN (i.e pin number 13) and the function of that pin is to give output.
- In block code, defining and initializing work is handled by the platform.

**Void loop()**:

This method determines the kind of work and processes the arduino will consider. Once the setup method is completly executed. Then it will directly jump to the loop methode.
- If you compare the line of code here and block code above, both express the same type of instructions. Just expressed in text syntax.

### Blinking external LED.

Till here, it has been mentioned that the builtin LED is connected to pin number 13. So we will be using the same code and will only make changes to the circuit.

- To do that, we have learned that to power up a LED we need to make a complete circuit. That is connect anode of LED to positive terminal (here we can use pin 13 since all the instruction are executed on pin 13) of through a current limiting resistor and cathode must be connected to the negative terminal (Ground/GND in arduino).

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/ex_led_test.png?ref_type=heads)
<p class="drive-image-caption">Led Test</p>


### Working with Servo Motor.

What is a servo motor?
- Servo motor is a rotary actuator, which means that we can adjust the output shaft to a specific angle. And we can provide the angle through program code of other input devices.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/servo_labeled.jpg?ref_type=heads)
<p class="drive-image-caption">Servo Label</p>


1. Case
2. Mounting taps
3. Output shaft
4. Servo Horns
5. Cable
6. Connector

Servo Motor comes in with 3 pins for power and signal.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/servo_connector.png?ref_type=heads)
<p class="drive-image-caption">Figure 1: Aesthetic Centre</p>


1. Power (RED): Connects to 5V.
2. Ground (Brown): Connects to ground.
3. Signl (Orange): Connects to any of the arduino pin, which can generate pulses.

To know more about servo motors, [click here](https://www.pololu.com/blog/13/gettin-all-up-in-your-servos).

### Connecting Servo circuit.

From the components list, add:
- Micro Servo and
- Arduino Uno R3 : our microntrollor.

Servo's can only be connected with those pins which are capable to generation pulse with modulation. Those pins can be identified from the arduion board.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/PWM.png?ref_type=heads)
<p class="drive-image-caption">PWM pins</p>


Take this in mind disign your own circuit understanding the basic connection rules learned during previous circuits. Start by adding the components on your design space.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/components.png?ref_type=heads)
<p class="drive-image-caption">Components</p>

Click on the terminal of servo and connect it to the Arduino as shown in the picture below.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/servo%20_circuit.png?ref_type=heads)
<p class="drive-image-caption">Servo Circuit</p>


To change the color of the connecting wires, on the top left cornor those options are available.

### Servo program.

![Description](https://gitlab.com/anithghalley/robotics_for_students/-/raw/main/Images/robotics_images/servo_code.png?ref_type=heads)
<p class="drive-image-caption">Servo Code</p>


From the block collection, similar to the code from blinking LED, replace the **LED HIGH** block with **SERVO ROTATE** block and insert the pin number and angles.

Finally click on start simulation to view the servo simulation.
