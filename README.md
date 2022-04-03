# Stepper-motor-synchronization
![maxresdefault](https://user-images.githubusercontent.com/19898602/161409403-f4f57185-7c35-46cd-97f1-1c4af16dfbb6.jpg)

# What is Stepper-motor-synchronization

Stepper motor synchronization means we made physically, electrically & by programming we made a set for stepper motors which runs in perfect synch, in this system we have one master stepper motor and one slave stepper motor.

So the slave motor precisely follow the the moves of master stepper motor.
They follow each other step by step. 
For this we have to program master and slave separately, the main this is that we achieve this
Complex motion by using only Arduino and custom PCB, not fancy PLC or controller needed.
To achieve such precision we need our system also to be accurate for this Custom PCBs from [JLCPCB.com](https://jlcpcb.com/IAT) really helps us.


# Component used

1. Arduino Nano
2. Custom PCB
3. NEMA 17 Stepper motor
4. A4988 Stepper driver
5. 20 x 20 alu. profile
6. Right angle bracket
7. GT2 belt
8. GT2 pulley
9. 3D printed parts.


# Circuit


Power connections

This is the basic circuit by which we can control stepper motor via a4988 stepper motor 
The driver requires a logic supply voltage (3 – 5.5 V) to be connected across the VDD and GND pins and a motor supply voltage (8 – 35 V) to be connected across VMOT and GND. These supplies should have appropriate decoupling capacitors close to the board, 

and they should be capable of delivering the expected currents (peaks up to 4 A for the motor supply).

![image](https://user-images.githubusercontent.com/19898602/161410272-54bd0224-675e-4196-9b0b-aa79163c42c5.png)


Control inputs

Each pulse to the STEP input corresponds to one microstep of the stepper motor in the direction selected by the DIR pin. Note that the STEP and DIR pins are not pulled to any particular voltage internally, so you should not leave either of these pins floating in your application. If you just want rotation in a single direction, you can tie DIR directly to VCC or GND. The chip has three different inputs for controlling its many power states: RST, SLP, and EN. For details about these power states, see the datasheet. Please note that the RST pin is floating; if you are not using the pin, you can connect it to the adjacent SLP pin on the PCB to bring it high and enable the board.

By following such basics of A44988 we designe a Custom PCB so that we not need to wire whole things again and again.

# Build the PCB

![FTQFHXZKLBNXU2X](https://user-images.githubusercontent.com/19898602/123725479-bd305280-d8ab-11eb-8709-c680e91e1300.jpg)
![MVI_0001_2 mp4 00_06_55_14 Still001](https://user-images.githubusercontent.com/19898602/123725534-d5a06d00-d8ab-11eb-9645-d2a05880e79a.jpg)
![MVI_0001_2 mp4 00_07_11_00 Still002](https://user-images.githubusercontent.com/19898602/123725542-d933f400-d8ab-11eb-9a7f-d88351d6a952.jpg)

I designe this multipurpose PCB Those who ever worked with arduino they know the pain of connecting multiple components to the arduino for there projects. so here is the answer for you all.

Not only 2 or 3 you can connect 11 components at same time & on board 5V & 9V regulator,

cross polarity protection, power indication LED,

motor power selection provision (5V or 9V or 12V) manual provision for stepper motor microstepping setting.

Wide range of input supply (9V to 24V). This is my multipurpose PCB works with Arduino Nano, I have designed it in a way that you can run 2 Stepper motors, 2 DC motors, 2 Servo motors at same time and this is not it you can even connect BT module, rotary encoder, I2C device, potentiometer at same time.

This PCB is very much helpful in building any project and no need to worry about messy wire connections.

![image](https://user-images.githubusercontent.com/19898602/123725769-50698800-d8ac-11eb-83b0-fbdab6a23ec1.png)
![image](https://user-images.githubusercontent.com/19898602/123725784-5a8b8680-d8ac-11eb-9a51-bb9042d974ec.png)


He we first see the overview of PCB means what is this PCB capable of and which components you can connect to the PCB.

# List of the Components you can connect to the PCB

> 2 DC motor ( 9V to 24V DC)

> 2 Potentiometer

> 2 Servo motors ( 5V to 9V DC)

> 1 Serial device (BT module, HMI, Communication module, RX, TX)

> 1 Encoder (2 interrupt pin & 1 PB pin)

> 1 I2C device (SCL/SDA Device, display, MPU6050 etc)

> 2 Stepper motors


# Special features of PCB

> Wide range of power input 9V to 24V DC

> Cross polarity protection

> DC motor voltage selection 9V or 12 V DC

> Servo motor voltage selection 5V or 9V DC

> Manual microstepping setting for stepper motor

> Power indication LED

> L298N IC for heavier DC motor

> ON board 5V and 9V regulator no need to arrange different power sources

> Header pins and screw terminals for easy connections




I have designe this PCB and order it from [JLCPCB.com](https://jlcpcb.com/IAT)

I always prefer [JLCPCB.com](https://jlcpcb.com/IAT) for my PCB needs, [JLCPCB.com](https://jlcpcb.com/IAT) have best deals for their customers
$2 for 1-4 Layer PCBs, free SMT assembly monthly.


If new user signup today from this link [JLCPCB](https://jlcpcb.com/IAT ) you will get 27$ coupon from [JLCPCB](https://jlcpcb.com/IAT ).


[Click here to visit JLCPCB.com](https://jlcpcb.com/IAT)





