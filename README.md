# Marlin

My customized build of Marlin...

## Files I have changed

- `README.md`
- `platformio.ini`
- `Marlin/Configuration.h`
- `Marlin/Configuration_adv.h`
- `Marlin/_Bootscreen.h`
- `Marlin/_Statusscreen.h`

## How to build

Setup the [Marlin/PlatformIO/VS Code build process](https://marlinfw.org/docs/basics/install_platformio_vscode.html), and run the build step for `STM32F103RET6_creality` that Auto Build Marlin provides.

Next time, I might try the [Marlin/PlatformIO command-line build process](https://marlinfw.org/docs/basics/install_platformio_cli.html), and run `platformio run -e STM32F103RET6_creality`

## How to upload the new firmware

1. Format my printer's microSD card
2. Copy the `.pio/build/STM32F103RET6_creality/firmware-[date].bin` file onto my microSD card
3. Put the microSD card into the printer and turn it on.  The printer should wake up with the new firmware in about 10 seconds.

## How to connect to the computer over serial

[Fix the drivers if necessary](https://linustechtips.com/topic/1288640-driver-issues-with-my-ender-3-pro-need-some-advice/)

Close Cura or any other programs that might hog the COM connection.

```
C:\Users\Joseph\Downloads\pronterface>pronsole
Welcome to the printer console! Type "help" for a list of available commands.
offline> connect
No port specified - connecting to COM3 at 115200bps
Printer is now online
T:21> M119
SENDING:M119
Reporting endstop status
x_min: TRIGGERED
y_min: open
z_min: TRIGGERED
filament: TRIGGERED
T:21> exit
Disconnecting from printer...
Exiting program. Goodbye!

```

## License

[GPL](/LICENSE)