*********************
Blokové programovanie
*********************

`Online Blockly Editor <https://makecode.microbit.org/?lang=sk_SK>`_ je online editor pre programovanie micro:bitu cez grafický programovací jazyk. Pri tomto spôsobe programovania nie je potrebná inštalácia softvéru na počítač či administrátorské práva, stačí prístup na internet a internetový prehliadač.


.. raw:: html

	<pre><code class="blocks">basic.showString(&quot;Hello world&quot;)
	</code></pre>


.. raw:: html

	<pre><code class="blocks">basic.forever(() =&gt; {
	    basic.showLeds(`
	        . # . # .
	        # . # . #
	        # . . . #
	        . # . # .
	        # . # . .
	        `)
	    basic.showLeds(`
	        . # . # .
	        # # # # #
	        # # # # #
	        . # # # .
	        . . # . .
	        `)
	})
	</code></pre>


Základné
--------

Zobraziť reťazec - vypíše text na obrazovke

Zobraziť LED - zobrazí obrázok na obrazovke

Vstup
-----

V tejto časti sa nachádzajú bloky, ktoré spustia kód pri nejakej udalosti - napríklad pri stlačení tlačidla, naklonení dosky alebo zatrasení.

Hudba
-----

Microbit dokáže generovať aj zvuk, a to konkrétne na kolíku 0. Preto k nemu pripojíme jeden káblik mikrofónu (dátový) a druhý (zem) pripojíme k ``GND``. Skúste si spustiť melódiu ``svadba``. 

Radio
-----

Micro:bit obsahuje aj vbudovaný komunikačný modul, a teda vedia medzi sebou navzájom komunikovať.

Pre používanie rádia je potrebné definovať skupinu (anglicky ``Group``) - `viac podrobností tu <https://support.microbit.org/support/solutions/articles/19000030849-how-to-use-radio-group-codes-with-the-javascript-blocks-editor>`_

Cykly, Logiku, Premenné, Matematika
-----------------------------------

Tak ako v Scratch, aj Blockly obsahuje základné príkazy a konštrukcie. Zaujímavým môže byť *vybrať náhodne od 0 po n*, ktorý generuje náhodné čísla.

