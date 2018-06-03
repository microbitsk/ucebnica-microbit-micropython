# MOVE: mini robot

[Návod na ovládanie motorov](http://robotsandphysicalcomputing.blogspot.com/2017/08/kitronik-move-mini-buggy-python-control.html)

[Návod na ovládanie LED diód](http://robotsandphysicalcomputing.blogspot.com/2017/08/kitronik-move-mini-buggy-python-control_7.html)

```python
# Kod pre Robota
from microbit import *
import radio

radio.on()

while True:
    try:
        msg = radio.receive()
    except Exception:
        continue
    if msg is None:
        pin1.write_analog(0)
        pin2.write_analog(0)
    else:
        if msg == "F":
            display.show(Image.ARROW_N)
            pin1.write_analog(1)
            pin2.write_analog(180)
        elif msg == "L":
            display.show(Image.ARROW_E)
            pin1.write_analog(180)
            pin2.write_analog(180)
        elif msg == "R":
            display.show(Image.ARROW_W)
            pin1.write_analog(1)
            pin2.write_analog(1)
    sleep(10)
    display.clear()
```

```python
# Ovladac
from microbit import *
import radio

radio.on()

while True:
    if accelerometer.get_y() < -500:
        radio.send("F")
        display.show(Image.ARROW_N)
    elif accelerometer.get_x() > 500:
        radio.send("R")
        display.show(Image.ARROW_E)
    elif accelerometer.get_x() < -500:
        radio.send("L")
        display.show(Image.ARROW_W)
    sleep(10)
```