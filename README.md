# Home automation door key dispenser
Something for when I forget to take my keys and lock myself out of the apartment. Portable, battery powered, system which is attached to the main door itself, right on top of the letter hole, from the inside of the apartment. The key is held hanging with a thread/rope attached and rolled to a motor shaft. Once activated, the motor should rotate the shaft and let gravity do the work. The key comes down to the letter hole and from outside we just grab it. Silly, IKR?

## Tech details

### Parts
 - ESP8266/NodeMCU
 - L298N motor driver
 - Small DC motor
 - 5V regulator
 - Battery pack (2S Li-Ion)
 - Thread/Rope
 - IR remote
 - IR receiver
 - Buzzer
 - Some 3D printer housing

### How it works
The workflow would be like, standing infront of the locked door the user should first wake up the system. Because, since this whole system is modular and battery powered we need to save the battery for as as possible. So, the system is always in deep sleep mode except the when the user wakes it up.

Waking up can be done in many different ways, such as buttons, NFC, mobile app etc. I chose IR because I just salvaged a sensor and remote from a broken led strip and most importantly I just want to.

The remote can be attached to the door, 90degrees left from the letter box so the postman does not mess it up. A 3D printed housing sticking to the door with double sided tape for the remote should be good enough. The IR sensor should be connected to the MCU and the receiving end should be exposed somehow. I have a "ancient looking keyhole" on my door and it should fit there nicely.

After waking up the system checks for a password and this password is given with the IR remote. The buzzer plays sounds of "System woke up", "Ready to take password", "Wrong password", " Correct password" etc. After that, user can put the system back to sleep or demand the key, where the key should be available through the letter hole.

### Circuit diagram
![alt text](https://github.com/ShocKwav3/home-automation-door-key-dispenser/blob/main/fritzing/door-key-dispenser_img.png)
