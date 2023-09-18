# Alex and Victor ESE 3500 Final Project

This was a final project for an Embedded Systems class built in pairs.
The code is entirely Bare Metal C for an Arduino, specifically the 328P Microprocessor.

It's main function was as a Violin-Synthesizer MIDI Controller.

The design features a neck with a location sensor (soft-membrane potentiometer) and force sensor (force-sensitive potentiometer) to take pitch and vibrato input and a joystick for pitch bend. 

There are eight dials (potentiometers) for adjusting different effects and operational modes, such as octave, volume, vibrato size, scale, transposition, chord type, and more.

All analog user input from the dials, neck, and joystick are converted to digital values, using and analog multiplexer and analog-to-digital conversion (ADC) on the 328P.

We use an LCD display screen, and I wrote custom fonts and a graphics library to display notes and sensor values.

One 328P controls the LCD screen, and the other takes the user input from the device and outputs it as MIDI commands to be interpreted by a MIDI speaker or processing software.

main.c --> Code runnning the main arduino responsible for UART MIDI and reading sensor values
DISPLAY_main.c --> Code running the secondary arduino respondible for the LCD display

All other files are libraries
