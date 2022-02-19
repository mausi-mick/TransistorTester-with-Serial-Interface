
TransistorTester on Arduino with Serial-Interface

The project based on the project "Tester V1.13: The Arduino UNO Transistor Tester“ from Pouc68000 :
       https://create.arduino.cc/projecthub/plouc68000/ardutester-v1-13-the-arduino-uno-transistor-tester-dbafb4/
I compiled the source under IDE 1.8.4 and 1.8.13  and load the program to an Arduino-NANO (clone) with old bootloader.
IAs display I used a LCD1602 (HD44780) 

It works perfect and the Pin-assignment is great.
On my Transistor-Curve-Tracer I have to find the assignement of the pins per hand and it’s sometime a problem and it needs time for changings pins, start again ....
Therefore I thought it would be a great help to copy the information from the Transitor-Tester to the Curve- Tracer and start the tracer automatically.
I need only a few data:

1. Device Type:  “1“ = DIODE, “2“=TRANSISTOR(bipolar), “3“=MOSFET, “4“=JFET, “5“=IGBT
2. Polarity:   “N“ or “P“
3. Mode:  „“E“ or „“D“ or blank:  E=enhanced, D=depletion (only for MOSFET and JFET , JFET generally “D
4: Pin1 -Assignment (BCDEGAK (and blank for DIODE (2-pole))
5: Pin2 -Assignment (BCDEGAK (and blank for DIODE (2-pole))
6: Pin3 -Assignment (BCDEGAK (and blank for DIODE (2-pole))

I send this few data per Serial (SoftSerial with 9600 baud) Interface to the Curve-Tracer.
On the end of the data I send CR (13) with Serial.println.
