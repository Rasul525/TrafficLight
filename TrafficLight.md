# TrafficLight
from pyfirmata import Arduino
import time
MyDevice = Arduino('COM4')


GreenLed = MyDevice.digital[13]
YellowLed = MyDevice.digital[12]
RedLed = MyDevice.digital[11]


while True:
    RedLed.write(1)
    time.sleep(5)
    RedLed.write(0)
    YellowLed.write(1)
    time.sleep(2)
    YellowLed.write(0)
    GreenLed.write(1)
    time.sleep(5)
    GreenLed.write(0)
