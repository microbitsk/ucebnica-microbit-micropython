****
Úvod
****

Python
======

Python je veľmi populárny a všestranný programovací jazyk odporúčaný pre vyučovanie základov programovania. Práve preto postupne nahrádza iné programovacie jazyky na hodinách informatiky. Vo veľkom Python využívajú aj v Google, Dropbox, Európskej organizácii jadrového výskumu CERN, sociálnych sieťach Facebook, Pinterest a Instagram, či pri vyučovaní na prestížnej vysokej škole MIT.

Autorom jazyka Python je Guido van Rossum (prvá verzia je z 1989). V súčasnosti jazyk Python vyvíja a spravuje komunita, zastrešovaná medzinárodnou organizáciou Python Software Foundation (skratka PSF). Samotný jazyk je open-source.

Python je interpretovaný jazyk, a preto sa po dopísaní kódu ho neskompilujeme (ako napríklad C či Pascal) ale spustíme ho v interpreteri. Ten náš kód za chodu číta a prekladá na strojové inštukcie pre procesor. Preto je potrebné, aby sme na spustenie Python kódu mali na počítači nainštalovaný Python interpreter. (ako si vysvetlíme o schvíľu)

Odporúčame používať najnovšiu verziu Python3 (v súčasnosti je to Python3.6). Python2 je staršia verzia Pythonu a už nie je vhodné v nej programovať.

V čom sa Python líši snáď najviac od iných programovacích jazykov je práve komunika. Tá je tvorená profesionálmi, začiatočníkmi, učiteľmi i víkendovými programátormi a tak je veľmi rôznorodá. Po celom svete sa pravidelne organizujú konferencie PyCon (čiže PYthon CONference). Na Slovensku je táto konferencia organizovaná raz ročne občianskym združením SPy (Slovak Python User Group).

MicroPython
===========

MicroPython je upravená verzia Pythonu, ktorá beží aj na menej výkonných zariadeniach. Vďaka tomu vieme v MicroPythone programovať mikroelektroniku a interagovať s okolitým svetom pomocou LED diód, senzorov, bzučiakov, motorčekov, atď. Takéto zariadenia sú zároveň rádovo lacnejšie ako počítače pre klasický Python. Obrovskou výhodou je fakt, že syntax je pre obe verzie jazyka rovnaká, a tak sa učiteľom aj žiakom stačí naučiť iba jeden jazyk.

Tak ako na spustenie Python kódu na počítači potrebuje nainštalovaný interpreter, tak aj pre MicroPython kód musíme na mikroprocesom najprv nainsťalovať MicroPython interpreter. To stačí spraviť raz a následne mu budeme už len posielať naše zdrojové kódy na preklad. Raz za čas sa ale oplatí MicroPython na zariadení preinštalovať na novšiu verziu, aby sme mali vždy čo najviac funkčný interpreter.

MicroPython interpreter vymyslel Damien George v roku 2013 pre vývojovú dosku pyboard (s mikroprocesorom STM32). V súčasnosti existuje viacero verzií MicoPythonu pre rôzne mikroprocesory. My budeme používať verziu pre micro:bit.

Čo je to micro:bit?
===================
Malá edukačná doska vhodná pre využitie vrámci hodín informatiky na základných a stredných školách. Vďaka konektorom (tzv. pinom) je možné ňou programovať hardvér.

Čo a ako viem pripojiť na micro:bit?
====================================


V akých jazykoch môžem micro:bit programovať?
=============================================

Je možné programovať ho v MicroPythone, C, JavaScripte a cez Blockly (podobné Scratch).

* [Mu Editor (Offline pre Python)](https://codewith.mu/)
* [Online Blockly Editor (SK)](https://makecode.microbit.org/?lang=sk_SK) - dá sa zvoliť český jazyk
* [Online MicroPython Editor (EN)](http://python.microbit.org/)
