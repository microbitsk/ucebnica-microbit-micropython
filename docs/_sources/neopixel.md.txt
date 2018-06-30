# NeoPixel

## Zasvietenie jednej LEDky

```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)
np[0] = (255, 0, 0)
np.show()

```

## Zasvietenie všetkých LEDiek


```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)
np[0] = (255, 0, 0)
np[1] = (255, 0, 0)
np[2] = (255, 0, 0)
np[3] = (255, 0, 0)
np[4] = (255, 0, 0)
np[5] = (255, 0, 0)
np[6] = (255, 0, 0)
np[7] = (255, 0, 0)
np.show()

```

## Zasvietenie všetkých LEDiek cyklom

```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)

for i in [0, 1, 2, 3, 4, 5, 6, 7]:
    np[i] = (255, 0, 0)
np.show()

```


```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)

for i in range(0, 8, 1):
    np[i] = (255, 0, 0)
np.show()

```


## Jednosmerný Knight Rider

```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)

while True:

    for i in range(0, len(np)):
        for led_id in range(0, len(np)):
            if i == led_id:
                np[led_id] = (0, 255, 0)
            else:
                np[led_id] = (0, 0, 0)
        sleep(100)
        np.show()
```

__Úloha:__ Naprogramuj NeoPixel tak, aby sa LEDka odrazila naspäť


## FadeIn and FadeOut

```python
from microbit import *
import neopixel

np = neopixel.NeoPixel(pin1, 8)

while True:

    # fade in
    for i in range(0, 256, 1):
        for led_id in range(len(np)):
            np[led_id] = (0, i, 0)
        np.show()

    # fade out
    for i in range(255, 0, -1):
        for led_id in range(len(np)):
            np[led_id] = (0, i, 0)
        np.show()

    # clear
    for i in range(len(np)):
        np[i] = (0, 0, 0)
    np.show()
```

## Náhodné generovanie farieb


```python
from microbit import *
import neopixel
from random import randint, seed

seed(5)
np = neopixel.NeoPixel(pin1, 8)

while True:

    for i in range(0, len(np)):
        red = randint(0, 255)
        green = randint(0, 255)
        blue = randint(0, 255)

        np[i] = (red, green, blue)

        np.show()
        sleep(500)
```
__Úloha:__ Pozmeň program tak, aby každú sekundu zmenil farby všetkých LED diód naraz