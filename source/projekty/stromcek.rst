Stromček s bezdrôtovým ovládaním
================================


Kód pre stromček::

    # Stromcek
    from microbit import *
    import neopixel
    import radio

    LEDS = 40

    radio.on()
    np = neopixel.NeoPixel(pin1, LEDS)

    def check_change():
        incoming = radio.receive()
        if incoming and 'change' in incoming:
            return True
        
        return False

    n = 0
    while True:
        
        while True:
            for i in range(0, LEDS):
                if ((i + n) % 3) == 0:
                    np[i] = (255, 0, 0)
                elif ((i + n) % 3) == 1:
                    np[i] = (0, 255, 0)
                else:
                    np[i] = (0, 0, 255)
            n += 1
            np.show()
            sleep(500)
            if check_change():
                break

        for i in range(0, LEDS):
            np[i] = (0, 0, 0)
        np.show()

        while True:
            if check_change():
                break
            sleep(100)



