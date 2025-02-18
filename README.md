#AUTOMATIC_TRAFFIC_LIGHT_CONTROL
 Traffic Light Control System Using MIcrocontroller(Arduino UNO).
 This project uses an Arduino to control three LEDs connected to pins 10, 11, and 12. The code sets up a cycle where:

    LED connected to pin 10 is turned ON for 5 seconds
    LED connected to pin 11 is turned ON for 2 seconds
    LED connected to pin 12 is turned ON for 5 seconds
    The cycle repeats continuously.

Setup Function (setup()):

 The setup() function runs once when the Arduino is powered on or reset. It configures the pin modes for the three digital pins that control the LEDs. This ensures that the Arduino knows which pins will be used for output.
 
 pinMode(pin, mode) is used to configure the pin mode. The OUTPUT mode is set for each pin (10, 11, and 12), which means these pins will supply power to the connected LEDs.

Loop Function (loop()):

 The loop() function contains the core of the program. It continuously runs after the setup() function has executed. This is where the LEDs are turned ON and OFF in a specified sequence with delays in between.
 
 digitalWrite(pin, value): This function controls the state of a specific pin. The argument HIGH turns the pin on (supplies voltage), while LOW turns the pin off (removes voltage).
 
 delay(ms): The delay() function pauses the program for the specified number of milliseconds. For example, delay(5000) causes a 5-second pause.
 
LED Sequence Breakdown:
 
    Step 1: Pin 10 is turned ON for 5 seconds, while Pin 11 and Pin 12 are turned OFF.
    Step 2: Pin 11 is turned ON for 2 seconds, while Pin 10 and Pin 12 are turned OFF.
    Step 3: Pin 12 is turned ON for 5 seconds, while Pin 10 and Pin 11 are turned OFF.
    Step 4: Pin 11 is turned ON again for 2 seconds, while Pin 10 and Pin 12 are turned OFF.
    Step 5: This cycle will continue indefinitely.

Hardware Setup:

    Required Components:
        1 Arduino board (e.g., Arduino Uno)
        3 LEDs (Red, Yellow, Green)
        3 220Ω Resistors (for current limiting)
        Breadboard and jumper wires
        Power supply (Arduino is powered via USB or external adapter)

    Circuit Diagram:
        Connect each LED to pins 10, 11, and 12 of the Arduino.
        Place a 220Ω resistor between each LED's anode (longer leg) and the corresponding pin.
        Connect the cathodes (shorter leg) of the LEDs to the ground (GND) pin on the Arduino.

LED Setup:

    RED LED at Pin 10:
        Anode (long leg) → Pin 10
        Cathode (short leg) → GND through a 220Ω resistor

    YELLOW LED at Pin 11:
        Anode → Pin 11
        Cathode → GND through a 220Ω resistor

    GREEN LED at Pin 12:
        Anode → Pin 12
        Cathode → GND through a 220Ω resistor

Working Principle of Circuit:

 When the Arduino is powered, it will execute the setup() function and then start the loop(). The LEDs will light up in sequence, following the timing defined in the program:

    Pin 10’s LED lights up first for 5 seconds.
    Then, Pin 11’s LED lights up for 2 seconds.
    Then, Pin 12’s LED lights up for 5 seconds.
    Finally, the cycle repeats.
