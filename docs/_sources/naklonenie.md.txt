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

## Presné meranie naklonenia

cez get_x()

## Hra: Vajce na lyžičke



