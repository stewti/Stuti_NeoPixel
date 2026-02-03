from machine import Pin
import time
kio = Pin(15, Pin.IN, Pin.PULL_UP)
ree = neopixel.NeoPixel(Pin(13),16)

while True:
    ree_val = ree.value()
    print(ree_val)
    if ree_val == 0:
        for i in range(0,16,1):
            ree[i]=(13,189,209)
            ree.write()
            time.sleep(0.1)
            
    else:
        for i in range(0,16,1):
            ree[i]=(0,0,0)
            ree.write()
        time.sleep(0.1)
