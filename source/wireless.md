# Bezdrôtová komunikácia

## Bezdrôtové vysielanie a prijímanie na micro:bitoch

```python
# Vysielanie
import radio

radio.on()
radio.send('sprava')
```

```python
# Prijimanie
import radio

radio.on()

while True:
    sprava = radio.receive()
    if sprava:
        print(sprava)
```

## Bezdrôtový vypínač (problémový)

```python
# Vysielanie
import radio
from microbit import *

radio.on()

while True:
    if button_a.was_pressed():
        radio.send('on')
    elif button_b.was_pressed():
        radio.send('off')
```

```python
# Prijimanie
import radio
from microbit import *

radio.on()

while True:
    sprava = radio.receive()
    if sprava == 'on':
        display.show(Image.HAPPY)
    elif sprava == 'off':
        display.show(Image.SAD)
```

## Bezdrôtový vypínač so špeciálnym protokolom

```python
# Vysielanie
import radio
from microbit import *

radio.on()

while True:
    if button_a.was_pressed():
        radio.send('adam-janka-on')
    elif button_b.was_pressed():
        radio.send('adam-janka-off')
```

```python
# Prijimanie
import radio
from microbit import *

radio.on()

while True:
    sprava = radio.receive()
    if sprava == 'adam-janka-on':
        display.show(Image.HAPPY)
    elif sprava == 'adam-janka-off':
        display.show(Image.SAD)
```


## Wireless Sniffer - Odchytávanie cudzích správ

```python
# Sniffer
import radio
from microbit import *

radio.on()

while True:
    message = radio.receive()
    if message:
        print(message)
```
