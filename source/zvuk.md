# Zvuk

![Pripojenie reproduktora](/_static/images/speaker-setup.png)

## Predprogramovaná hudba

```python
import music

music.play(music.NYAN)
```

* __music__ - kinižnica na generovanie hudby na _pine 0_
* __music.NYAN__ - prehrá melódiu _NYAN_

micro:bit už má niekoľko predprogramovaných melódií, tie nájdete v  - [dokumentácii (pozri Music)](http://microbit-micropython.readthedocs.io/en/latest/tutorials/music.html)



## Písanie vlastnej hudby

```python
import music

tune = ["C4:4", "D", "E", "C", "C", "D", "E", "C", "E", "F", "G:8",
        "E:4", "F", "G:8"]
music.play(tune)
```
* __C4:4__ - nota C zo štvrtej oktávy s dĺžkou 4

## Rolničky na micro:bite


![Noty](/_static/images/noty-1.jpg)
![Noty](/_static/images/noty-2.gif)

![Rolničky noty](/_static/images/jinglebells.gif)


```python
# Piesen Rolnicky
import music

tune = ["E:2", "E:2", "E:4", "E:2", "E:2", "E:4", "E:2", "G:2", "C:3", "D:1",
        "E:8", ]
music.play(tune)
```

__Úloha:__ Doplň celú pieseň a zmeň jej tóninu


## Zvukové efekty

```python
import music

music.pitch(400, 1000)
```

Prvým argumentom je frekvencia a druhým dĺžka prehrávania frekvencie.

Viac o tvorení zvukových efektov pomocou funkcie music.pitch() nájdeš v [dokumentácii](https://microbit-micropython.readthedocs.io/en/latest/music.html?highlight=pitch#music.pitch)

## Tvorba melódie


```python
import music

music.pitch(400, 1000)
music.pitch(600, 1000)
music.pitch(800, 1000)
```

__Úloha:__ Naprogramuj jednoduchý dvojtónový alarm ktorý sa po 5 sekundách vypne


## Tvorba melódie cez cykly


```python
import music

for freq in [400, 600, 800]:
    music.pitch(freq, 1000)
```

```python
import music

for freq in range(400, 1000, 200):
    music.pitch(freq, 1000)
```

## Obrátená melódia

```python
import music

for freq in [800, 600, 400]:
    music.pitch(freq, 1000)
```

```python
import music

for freq in range(800, 200, -200):
    music.pitch(freq, 1000)
```

## Jemnejšia melódia

Teraz zmenšíme jednotlivé skoky vo frekvenciách a aj dĺžky prehrávania jednotlivých tónov

```python
import music

while True:
    for freq in range(880, 1760, 16):
        music.pitch(freq, 6)
    for freq in range(1760, 880, -16):
        music.pitch(freq, 6)
```

__Úloha:__ Naprogramuj policajnú sirénu [(inšpiruj sa touto zvučkou)](https://www.youtube.com/watch?v=Kpxcx0E8MIU)


## Rozprávajúci micro:bit

![Speech setup](https://microbit-micropython.readthedocs.io/en/latest/_images/speech1.png)

```python
import speech

speech.say("Hello students! I am a microbit")
```


