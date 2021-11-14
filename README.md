[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Introduction
============

Driver in MicroPython for AHT2x: humidity and temperature sensors.
The driver covers 100% of the sensor's functionality:
* Get busy status or calibrated status.
* Measurement of relative humidity and temperature.
* Automatic calibration.
* Reset function.
* Control function (with CRC8 Dallas/Maxim).

Compatible models:
* AHT20
* AHT21

Dependencies
=============

This driver has no dependency

Install
=======

Copy the file aht.py in your project folder.

Usage Example
=============

.. code-block:: micropython

    import time, machine
    import aht

    # Example SCL pin and SDA pin for WEMOS D1 mini Lite
    i2c = machine.I2C(scl=machine.Pin(5), sda=machine.Pin(4))
    sensor = aht.AHT2x(i2c, crc=True)

    # To print one of measures:
    print("Humidity: {:.2f}".format(sensor.humidity))
    print("Temperature: {:.2f}".format(sensor.temperature))


Documentation
=============

Read the code.

Contributing
============

Contributions are welcome!
