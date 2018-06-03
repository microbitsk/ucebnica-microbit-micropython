# Digitálny vstup

```python
from microbit import *

while True:
    if pin2.read_digital():
        display.show(Image.HAPPY)
    else:
        display.show(Image.SAD)
```

![Micro:bit pinout](http://microbit-micropython.readthedocs.io/en/latest/_images/pinout.png)
