# AKT
a Toolchain, used on the Arduino Giga R1 Wifi

## Basic-usage

### AKT-class
AKT...

.AKT_Setup(): Initalizes the Libary, with such things like Serial, and the Onboard LED(green).

.DEBUG_INFO(): prints over Serial some debug-information and calles a Funktion which checks if float is 4 and double 8 bytes long is.

.WLAN_INFO(): prints information about the Wifi-connection.

.blinkLED(): if called in the loop, blinks the onboard LED, definde by the LED_builtin macro with an interval of 500ms.

.SP(String): prints a string via Serial, so you don't have to always use Serial.print("This is a String");.

### KC-class
KC...

.initcommandMap(): initalizes the commandmapping, but is already called in the setup.

.execute(String): executes a command, and returns the return of that command as a String.

## Advanced-usage

### Files

FILE_com...

.fileList(): list al files on the USB-Stick.

.fileRead(Name): Reads a file.

.fileWrite(Name,content): Writes to a file.

.fileDelet(Name): Delets a file

### Funcs
Funcs is a collection of Functions that have a specific usage, for example:

FUNCS.testFloatDoublePercision();

Test rather float and double are 4 or 8 bytes and prints the result to Serial.

or another example: FPU_Enable

FUNCS.FPU_Enable

enables the Hardware FPU, by executing some ASM(short for Asembly), because otherways the Giga would callculate float and double with Software.

### Serial-IN
Serial in is a Class used to read from the Serial-port and print out the return.

SERIN...

.read(): reads on the port until a "\n" and saves it to "recievedMessage", wich can be printet out with:

.getReceivedMessage().

.readSerialData is the core reader, wich is just internal
