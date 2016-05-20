maestro.py
==========

This Python class supports Pololu's Maestro servo controller over USB serial.

The class includes methods to control servos (position, speed, acceleration), read servo position, and start/stop Maestro scripts.  See Pololu's on-line documentation to learn about the full capabilities of this nifty micro-controller.

## Getting Started

Pololu's Maestro Windows installer sets up the Maestro Control Center, used to configure, test and program the controller.  Be sure the Maestro is configured for "USB Dual Port" serial mode. I believe the controller is setup in this mode by default by default, so it shouldn't be necessary to use the Control Center application.

You'll need to have the 'pyserial' Python module installed to use maestro.py.

### Installing for Windows

For Windows, you'll need to first, download and install Python as administrator (Maestro has been tested so far on Python 2):
  - [Python for Windows Releases](https://www.python.org/downloads/windows/)
    - [Python 2.7.11 Installer](https://www.python.org/downloads/release/python-2711/)

Then install pyserial, be sure to run as administrator again:
  - [PySerial Latest Release](https://pypi.python.org/pypi/pyserial)
    - [PySerial 3.0.1 Windows Installer](https://pypi.python.org/packages/6b/a6/0206c0517b508a640408db26310b4666083ad8bfd612f5a4d2bc796005b9/pyserial-3.0.1.win32.exe#md5=a3dbae2ca647e90dbb262d62093302ea)

Example usage of maestro.py:

```python
import maestro
servo = maestro.Controller()
servo.setAccel(0,4)      #set servo 0 acceleration to 4
servo.setTarget(0,6000)  #set servo to move to center position
servo.close
```
