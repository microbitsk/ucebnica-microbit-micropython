# Tlačidlá

## Vypísanie počtu stlačení

```python
from microbit import *

sleep(10000)
display.scroll(str(button_a.get_presses()))
```

## Zmena obrázku tlačidlami

```python
from microbit import *

while True:
    if button_a.is_pressed():
        display.show(Image.HAPPY)
    else:
        display.clear()

```

__Úloha 1:__ Pozmeň kód tak, aby sa pri stlačení tlačidla B zobrazil obrázok ``Image.SAD``

__Úloha 2:__ Pozmeň kód tak, aby sa pri stlačení oboch tlačidiel naraz zobrazil obrázok ``Image.CONFUSED``

