# What does your fork add over the original?

A lot actually. I have inverted some axes to better fit my requirements. I have also added an "enable" touch pin which makes the mouse move only when touched(since the hold button did not satisfy my requirements). Pin Info and pics will vary(will slowly add as project progresses), if I forget to edit later on, open an issue.

For now, the buttons all remain the same, except you need to run a jumper pin from GPIO4(in order to move the mouse) to ... well, anywhere. You touch it/hold it and mouse moves. I recommend strapping it to a piece of aluminium foil. 

    SCL (ESP32 GPIO22) MPU6050 SCL PIN
    SDA (ESP32 GPIO21) MPU6050 SDA PIN
    T0(GPIO4)(TOUCH MOUSE ENABLE PIN)
    GPIO19 (LEFT CLICK)(it's flipped on mine for some reason, GPIO 18 being left click and vice versa)
    GPIO18 (RIGHT CLICK)
    GPIO05 (HOLD KEY)
    GPIO17 (SCROLL DOWN)
    GPIO16 (SCROLL UP)
    
    
    
Schematic: 


![Schematic_AirGlove_2023-02-05](https://user-images.githubusercontent.com/84176052/216811419-fb68ccfc-73c3-4fa6-b2e3-7f4ae1456572.png)

PCB: 

https://github.com/sounddrill31/Air-Glove-PCB


Limitations: You can't use mouse and click at the same time(the original repo can. This is likely due to the touch pin "Enabling" the mouse).


Fun fact: the original repo developer has the same esp 32 as me(the ai-thinker nodemcu-32s)

Credits: 
rm10078's BLE_mouse_esp32_with_mpu6050

T-vK's ESP32-BLE-Mouse

EasyEDA, amazing software

Bonus tip: Get a cheap tp4056 module, a single or multi 18650 battery slot and an 18650 battery(also a latching switch, if you're into that.) instead of the 9V battery.


Everything below is unchanged. 

# 🐁 Bluetooth mouse control by gyro (MPU6050)

In this project i make a mouse useing esp32 and MPU6050 sensor.<br> 
It have all standard mouse features.
For more information read all documents carefully.
<br>
![App Screenshot](https://github.com/rm10078/BLE_mouse_esp32_with_mpu6050/blob/main/image/Bluetooth%20Delivery.png?raw=true)




## 🖱 Features

* Bluetooth connectivity
* Left Click
* Right Click
* Scroll Up
* Scroll Down
* Hold Button

## ⌨ Hold button work
When Your press the hold button the mouse arrow stop moveing. This button is to adjust the mouse arrow position.
<br>

![App Screenshot](https://github.com/rm10078/BLE_mouse_esp32_with_mpu6050/blob/main/image/left%20click.png?raw=true)

## Documentation

* [ESP32 DATASHEET](https://espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf)
* [ MPU6050 DATASHEET ](https://invensense.tdk.com/wp-content/uploads/2015/02/MPU-6000-Register-Map1.pdf)
* [BLE MOUSE LIBRARY](https://github.com/T-vK/ESP32-BLE-Mouse)

## Component List
* ESP32 1X
* MPU6050 1X
* PUSH BUTTON 5X
* SWITCH 1X
* WIRE
* VERO BOARD / BREADBOARD 1X
* 9V BATTERY 1x

## Circuit Diagram
![App Screenshot](https://github.com/rm10078/BLE_mouse_esp32_with_mpu6050/blob/main/image/diagram.png?raw=true)

## Pin information
* SCL (ESP32 GPIO22) MPU6050 SCL PIN
* SDA  (ESP32 GPIO21) MPU6050 SDA PIN
* GPIO19    (LEFT CLICK)
* GPIO18    (RIGHT CLICK)
* GPIO05    (HOLD KEY)
* GPIO17    (SCROLL DOWN)
* GPIO16    (SCROLL UP)

## ⚠ Warning
Try to use 9v battery.(Best 5v).Not attach battery direct to the 3.3v line.
Don't need to attach pullup resistor in button.I pullup all button on program. 
Be careful about battery polarity.

## Change configuration

### Change Mouse sensitivity & speed
* For x-axis Change (int SensitivityX = 700;) this veriable value.
* For Y-axis Change (int SensitivityZ = 800;) this veriable value.
* For scroll speed Change (int s_speed=100;) this variable value.

## Code link

- [code](https://github.com/rm10078/BLE_mouse_esp32_with_mpu6050/blob/main/air_mouse_esp32/air_mouse_esp32.ino)



## 🚀 About Me
I am a diploma engineer. Currently i am pursuing Bachelor in technology.
I am a 3nd year Applied Electronics and Instrumentation engineering student.
Thank you.

