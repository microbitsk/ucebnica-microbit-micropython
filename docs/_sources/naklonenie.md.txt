# Naklonenie


## Gestures

```python

from microbit import *

while True:
    gesture = accelerometer.current_gesture()
    if gesture == "face up":
        display.show(Image.HAPPY)
    else:
        display.show(Image.ANGRY)
```

Gestures:

* up
* down
* left
* right
* face up
* face down
* freefall
* 3g
* 6g
* 8g
* shake

__Úloha:__ Pomocou obrázkov ``Image.ARROW_N``, ``Image.ARROW_E``, ``Image.ARROW_S`` a ``Image.ARROW_W`` naprogramuj micro:bit tak, aby pri akomkoľvek naklonení smerovala šípka na obrazovke smerom hore.

```python
from microbit import display, acceletometer, sleep
import random

while True:
    if accelerometer.was_gesture("shake"):
        display.clear()
        sleep(1000)
        display.scroll(random.randint(1, 15))

```

## Presné meranie naklonenia

cez get_x()

## Hra: Vajce na lyžičke



