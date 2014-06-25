python-raumfeld
===============
A pythonic library for discovering and controlling Teufel Raumfeld devices.

Tested with a Raumfeld One.
Hardware donations to improve the library are welcome :smile:

Supports Python >2.7, 3.x


Installation
------------
```
pip install raumfeld
```


Quickstart
----------
```python
import raumfeld

# discovery returns a list of RaumfeldDevices
devices = raumfeld.discover(timeout=1, retries=1)
if len(devices) > 0:
    speaker = devices[0]

    speaker.mute = True     # mute
    print(speaker.volume)   # print current volume
    speaker.volume = 50     # set volume
else:
    print('No devices found.')
```
