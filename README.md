RF CONTROLLED HOME APPLICATION
Summary of the project


This circuit utilizes the RF module (Tx/Rx) for making a wireless remote, which could be used to drive an output from a distant place. RF module, as the name suggests, uses radio frequency to send signals. These signals are transmitted at a particular frequency and a baud rate. A receiver can receive these signals only if it is configured for that frequency. A four channel encoder/decoder pair has also been used in this system. The input signals, at the transmitter side, are taken through four switches while the outputs are monitored on a set of four LEDs corresponding to each input switch. The circuit can be used for designing Remote Appliance Control system. The outputs from the receiver can drive corresponding relays connected to any household appliance.

Step 1: GATHER ALL PARTS (REQURIED PARTS)

GATHER ALL PARTS (REQURIED PARTS)
Tx-Rx module-500x500.jpg
sold1.JPG
RESISTORS
1)39K--1

2)180K--1

3)560 OHMS--1

4)1 K--1

5)730K--1

CAPACITORS

1)100MFD /16V--1

2) 100UF--1

TRANSISTORS

1)BC558---1

2)SL100---1

SWITCHES

8-PIN DIP SWITCHES OR ON-OFF SWITCHES--1

RELAY 5V--1

ON-OFF SWITCHES --1

RF MODULES RX-434A, TX-434A

IC'S

HT 12D---1

HT 12E--1

CD4017 4B--1

7805--1

SOLDIERING GUN,LEAD ,FLUX

WIRES

CUTTER

BATTERIES SNAP

9V BATTERIES

PCB

Step 2: CIRCUIT DIAGRAM RECEIVER

CIRCUIT DIAGRAM RECEIVER 
RF Based Wireless Remote using RX-TX MODULES (434MHz.)

Description

This radio frequency (RF) transmission system employs Amplitude Shift Keying (ASK) with transmitter/receiver (Tx/Rx) pair operating at 434 MHz. The transmitter module takes serial input and transmits these signals through RF. The transmitted signals are received by the receiver module placed away from the source of transmission. The system allows one way communication between two nodes, namely, transmission and reception. The RF module has been used in conjunction with a set of four channel encoder/decoder ICs. Here HT12E & HT12D have been used as encoder and decoder respectively. The encoder converts the parallel inputs (from the remote switches) into serial set of signals. These signals are serially transferred through RF to the reception point. The decoder is used after the RF receiver to decode the serial format and retrieve the original signals as outputs. These outputs can be observed on corresponding LEDs.

Encoder IC (HT12E) receives parallel data in the form of address bits and control bits. The control signals from remote switches along with 8 address bits constitute a set of 12 parallel signals. The encoder HT12E encodes these parallel signals into serial bits. Transmission is enabled by providing ground to pin14 which is active low. The control signals are given at pins 10-13 of HT12E. The serial data is fed to the RF transmitter through pin17 of HT12E

Transmitter, upon receiving serial data from encoder IC (HT12E), transmits it wirelessly to the RF receiver. The receiver, upon receiving these signals, sends them to the decoder IC (HT12D) through pin2. The serial data is received at the data pin (DIN, pin14) of HT12D. The decoder then retrieves the original parallel format from the received serial data.

When no signal is received at data pin of HT12D, it remains in standby mode and consumes very less current (less than 1μA) for a voltage of 5V. When signal is received by receiver, it is given to DIN pin (pin14) of HT12D. On reception of signal, oscillator of HT12D gets activated. IC HT12D then decodes the serial data and checks the address bits three times. If these bits match with the local address pins (pins 1-8) of HT12D, then it puts the data bits on its data pins (pins 10-13) and makes the VT pin high. An LED is connected to VT pin (pin17) of the decoder. This LED works as an indicator to indicate a valid transmission. The corresponding output is thus generated at the data pins of decoder IC. A signal is sent by lowering any or all the pins 10-13 of HT12E and corresponding signal is received at receiver’s end (at HT12D). Address bits are configured by using the by using the first 8 pins of both encoder and decoder ICs. To send a particular signal, address bits must be same at encoder and decoder ICs. By configuring the address bits properly, a single RF transmitter can also be used to control different RF receivers of same frequency.


To summarize, on each transmission, 12 bits of data is transmitted consisting of 8 address bits and 4 data bits. The signal is received at receiver’s end which is then fed into decoder IC. If address bits get matched, decoder converts it into parallel data and the corresponding data bits get lowered which could be then used to drive the LEDs. The outputs from this system can either be used in negative logic or NOT gates (like 74LS04) can be incorporated at data pins.

Step 3: CIRCUIT DIAGRAM TRANSMITTING

CIRCUIT DIAGRAM  TRANSMITTING  
IMG_20141008_093038.jpg
The TWS-434 and RWS-434 are extremely small, and are excellent for applications requiring shortrange
RF remote controls. The transmitter module is only 1/3 the size of a standard postage stamp, and can easily be placed inside a small plastic enclosure. TWS-434: The transmitter output is up to 8mW at 433.92MHz with a range of approximately 400 foot (open area) outdoors. Indoors, the range is approximately 200 foot, and will go through most walls.....

The TWS-434 transmitter accepts digital inputs, can operate from 1.5 to 12 Volts-DC, and makes building
a miniature hand-held RF transmitter very easy. The TWS-434 is approximately the size of a standard postage stamp

RWS-434: The receiver also operates at 433.92MHz, and has a sensitivity of 3uV. The RWS-434
receiver operates from 4.5 to 5.5 volts-DC, and has both linear and digital outputs

Note: For maximum range, the recommended antenna should be approximately 35cm long. To convert
from centimeters to inches -- multiply by 0.3937. For 35cm, the length in inches will be approximately 35cm x 0.3937 = 13.7795 inches long. We tested these modules using a 14", solid, 24 gauge hobby type wire, and reached a range of over 400 foot. Your results may vary depending on your surroundings
