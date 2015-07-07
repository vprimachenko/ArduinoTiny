#Arduino-Tiny
Arduino-Tiny is an open source set of ATtiny "cores" for the Arduino platform.

The Arduino platform currently supports Atmel ATmega processors. There is a need for the Arduino platform to work with physically smaller DIP package processors. The intent of this project is fulfill that need. Specifically, our goal is to
provide a core that enables Arduino users to work with the ATtiny84 (84/44/24), ATtiny85 (85/45/25), and ATtiny2313 processors.

For more information about Arduino, see the website at: http://www.arduino.cc/

#How is this different from other mirrors?
This version has tailored `boards` file to leverage new ui possibilities of `^1.6` release of Arduino IDE, namely dynamic menus, thus reducing amount of new entries in board menu, yet still providing all options.

#INSTALLATION
* Ensure the Arduino IDE is NOT running.
* Download the Arduino-Tiny archive (ZIP-file).
* Locate the Arduino Sketchbook folder.  This is the folder where the Arduino IDE stores Sketches.
* Ensure the "hardware" folder exists under the Arduino Sketchbook folder.  For example, if the Arduino Sketchbook folder is

        C:\Projects\Arduino\

  Ensure this folder exists

        C:\Projects\Arduino\hardware\

* Extract the contents of the archive into the "hardware" folder.  For example, if the Arduino Sketchbook folder is

        C:\Projects\Arduino

  After extracting, the following files / folders should exist...

        C:\Projects\Arduino\hardware\tiny\avr\license.txt
        C:\Projects\Arduino\hardware\tiny\avr\platform.txt
        C:\Projects\Arduino\hardware\tiny\avr\Prospective Boards.txt
        C:\Projects\Arduino\hardware\tiny\avr\README
        C:\Projects\Arduino\hardware\tiny\avr\bootloaders\
        C:\Projects\Arduino\hardware\tiny\avr\cores\

  The following folder should contain the source files for the Arduino-Tiny
  core...

        C:\Projects\Arduino\hardware\tiny\avr\cores\tiny\

* Create a new file named "boards.txt" in the tiny\avr directory.  Following 
  from the examples above, the file would be here...

        C:\Projects\Arduino\hardware\tiny\avr\boards.txt

* Start the Arduino IDE and ensure the new boards of interest are listed under
  the <kbd>Tools</kbd>▶<kbd>Board</kbd> menu...

        ATtiny84
        ATtiny85
        …

* Under <kbd>Tools</kbd>▶<kbd>Clock</kbd> you are presented with various setting for internal and
  external clock for each chip

        8 MHz (internal oscillator; BOD disabled)
        1 MHz (internal oscillator; BOD disabled)
        …

  to **set new clocking** on a a chip it is required to <kbd>Tools</kbd>▶<kbd>Burn Bootloader</kbd> once

You are now ready to use Arduino-Tiny!


##CREDITS
Arduino is an open source project, supported by many.

The Arduino team is composed of Massimo Banzi, David Cuartielles, Tom Igoe,
Gianluca Martino, and David A. Mellis.

Arduino uses the GNU avr-gcc toolchain, avrdude, avr-libc, and code from
Processing and Wiring.

Arduino-Tiny is based on work by David A. Mellis, René Bohne, R. Wiersma,
Alessandro Saporetti, and Brian Cook.
