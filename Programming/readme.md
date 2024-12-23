## Getting started programming
I am going to assume you will use micropython, at least while you learn about the board. I personally do not have enough experiance with embedded programing in systems languages like c to teach them. 
The first thing you will need is a python ide with a way to interface with the pico. When a micropython interpreter is running on the pico (I gave it to you with one installed), the pico will show up as a serial device to host computers. Programs can then access the pico's file system and a real time shell, called a python REPL, over the serial connection. The EASIEST way to get started is by using a program called `Thonny Python` since it has functionality for the pico baked in and is supported by raspberry pi. It is not very feature rich, but it does work. VSCode will work as well using the python and micropico extensions. In the past this has been very finicky but it is getting better since the raspberry pi organization is starting to support the afformentioned micropico extension.

<br>
Unfortunatly I do not have copies of the demo code I wrote, I will make a quick copy of the device and write some demo code after christmas, for now you can open the ones on your board and modify them :)

## For Thonny
- Install Thonny https://thonny.org/
- Go to Tools -> Options -> Interpreter
- Change the top setting from "Python 3 Local" (or similar) to "Micropython Raspberry Pi Pico" (about half way down the list). Press ok.
- Plug in the pico using the microusb port (Be sure that at least one battery has been removed to avoid feeding the 5v from the usb port to the AA batteries)
- Press the stop sign to restart thonny's backend and connect to the pico. You should see some confirmation text appear in the "Shell" section
- Go to file -> open or Press CTRL+O, select open from pico, and then open main.py.

This will open up the main.py file and allow you to edit it on the pico directly. You can press the green triangle/F5 to run the file. While you are programming you can run code directly on the pico through the REPL. (it is labeled "shell" in thonny ide). Try running the program and then typing `display.fill(st7789.BLUE)` into the repl

## For VSCode

- Open up vscode and open an empty folder to work in (File -> Open Folder)
- Install the Micropico extension
- Plug in the pico using the microusb port (Be sure that at least one battery has been removed to avoid feeding the 5v from the usb port to the AA batteries)
- Back in VS Code, Press CTRL+SHIFT+P or the search bar at the top of the screen to open the command pallete
- Type in `MicroPico: Connect` and press enter.
- When the board connects, open the command pallete again and enter `MicroPico: Download project from pico`

This should download a copy of the files from the pico into your workspace. You can edit them and then run them with the Run button marked by a play icon in the toolbar at the bottom of the screen. It will be inbetween the two buttons "Pico connected/disconnected" and "Reset." When you run a program, a termial will pop up titled vREPL. Typing python code into this will run it directly on the pico. Try running the program and then typing `display.fill(st7789.BLUE)` into the repl <br>

The two libraries (& their documentation) I am using to control the display and read the IMU can be found here.<br>
https://github.com/Lezgend/MPU6050-MicroPython <br>
https://github.com/russhughes/st7789_mpy/tree/master <br>

I will update this very soon with more information :)