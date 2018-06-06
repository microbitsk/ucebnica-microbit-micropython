# Banánové piano

Teraz zameň ``read_digital`` za ``is_touched``.
Namiesto kábliku použi na prepojenie kúsky alobalu a ruky.
Vyskúšaj to aj cez banán, jablko či pomaranč.

![Micro:bit pinout](/_static/images/banana-keyboard.JPG)
```python
from microbit import *
import music

tune = ["C4:4", "D", "E", "C", "C", "D", "E", "C", "E", "F", "G:8",
        "E:4", "F", "G:8"]
i = 0

while True:
    if pin2.is_touched():
        music.play(tune[i])
        i += 1
        if i == len(tune):
            i = 0
```
Toto naše piano vieme rozšíriť ešte aj o svetlo - pri každom stlačení klávesu náhodne zmeníme všetky farby na LED pásiku.


__Pozri Mu editor cez pip vs cez Exe na touch sensor__