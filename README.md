# Stepper-motor-synchronization
![maxresdefault](https://user-images.githubusercontent.com/19898602/161409403-f4f57185-7c35-46cd-97f1-1c4af16dfbb6.jpg)

# What is Stepper-motor-synchronization

Stepper motor synchronization means we made physically, electrically & by programming a set for stepper motors which runs in perfect synch, in this system we have one master stepper motor and one slave stepper motor.

So the slave motor precisely follow the the moves of master stepper motor.
They follow each other step by step. 
For this we have to program master and slave separately, the main point here is that we achieve this
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
9. 8mm smoth rod
10. 8mm linear bearings
11. 3D printed parts.


# Circuit


Power connections

This is the basic circuit by which we can control stepper motor via a4988 stepper motor 
The driver requires a logic supply voltage (3 – 5.5 V) to be connected across the VDD and GND pins and a motor supply voltage (8 – 35 V) to be connected across VMOT and GND. These supplies should have appropriate decoupling capacitors close to the board, 

and they should be capable of delivering the expected currents (peaks up to 4 A for the motor supply).

![image](https://user-images.githubusercontent.com/19898602/161410272-54bd0224-675e-4196-9b0b-aa79163c42c5.png)


Control inputs

Each pulse to the STEP input corresponds to one microstep of the stepper motor in the direction selected by the DIR pin. Note that the STEP and DIR pins are not pulled to any particular voltage internally, so you should not leave either of these pins floating in your application. If you just want rotation in a single direction, you can tie DIR directly to VCC or GND. The chip has three different inputs for controlling its many power states: RST, SLP, and EN. For details about these power states, see the datasheet. Please note that the RST pin is floating; if you are not using the pin, you can connect it to the adjacent SLP pin on the PCB to bring it high and enable the board.

By following such basics of A44988 we designe a Custom PCB so that we not need to wire whole things again and again.

# CUSTOM PCB

![image](https://user-images.githubusercontent.com/19898602/125588570-5cc527d3-79ea-40f4-8323-70093eb0e1d6.png)


![image](https://user-images.githubusercontent.com/19898602/125588592-7213d3f4-ddb1-425a-ad33-9f070ff8d8a1.png)


L293D = 2 pieces


LM7809 = 1 piece


LM7805 = 1 piece


10.1uF electrolytic = 1 piece


1N5408 = 1 piece


1N4007 = 1 piece


led = 1 piece


resistance of at least 470 Ohm = 1 piece




Arduino Nano = 1 piece


Oled display = 1 piece


Encoder = 1 piece


A4988 controller = 2 pieces




socket 8 + 8 = 1 piece


PCB female pin header connectors


screw connectors for printed circuit boards


I have designe a PCB which is multipurpose and order it from [JLCPCB](https://jlcpcb.com/IAT ) 

I always prefer [JLCPCB.com](https://jlcpcb.com/IAT) for my PCB needs, [JLCPCB.com](https://jlcpcb.com/IAT) have best deals for their customers
$2 for 1-4 Layer PCBs, free SMT assembly monthly.

![image](https://user-images.githubusercontent.com/19898602/159014034-3c9a50c3-61c3-40d2-836d-9cadc2317d33.png)


SMT Assembly service of [JLCPCB.com](https://jlcpcb.com/IAT) is cherry on top now get your PCB fully assembled and save your time and money
Select components for your PCB from there Parts Library of 200k+ in-stock components
they are offering $27 valued New User coupons  & $24 SMT coupons every month
$8.00 setup fee, and $0.0017  per joint

Now no need to order components separately for you PCB and get free from stress of soldering them on PCB just try PCB SMT assembly service and get you PCB with components pre assembled and ready for the project


👉 Try PCBA service of [JLCPCB.com](https://jlcpcb.com/IAT) and save your time and money, get PCB ready for project, 200K+ components in library of [JLCPCB.com](https://jlcpcb.com/IAT) as well as 3rd party         parts to choose from. 
    Assembly will support 10M+ parts from Digikey, mouser
    
👉 $27 valued New User coupons 

👉 $24 SMT coupons every month


For more detials & offers please visit [JLCPCB.com](https://jlcpcb.com/IAT)


[Click here to visit JLCPCB.com](https://jlcpcb.com/IAT)



![image](https://user-images.githubusercontent.com/19898602/161410534-d1b6bd4f-492d-456e-894f-20ee5697f6ac.png)![image](https://user-images.githubusercontent.com/19898602/161410536-e4ddeea8-bdd7-4fc9-95d6-1381b63e2177.png)

First of all I take some 20 x 20 aluminium profile, and make the base of the machine out of it.
I used right angle bracket to joints the corners.


![image](https://user-images.githubusercontent.com/19898602/161410575-c2f1f0a3-5d20-45ab-97f1-2c1370d39725.png)![image](https://user-images.githubusercontent.com/19898602/161410584-f4ee8fec-2dd1-4197-8a17-defbeffc4533.png)


Then I bring 2 8mm SS smooth rod. And 4 qty of 8mm linear bearings.
2 bearings is for master and 2 bearing is for slave. Our whole stepper motor arrangement will slide back and forth on this. 


![image](https://user-images.githubusercontent.com/19898602/161410622-edaef001-283d-4ed1-8e71-b7192364ff94.png)![image](https://user-images.githubusercontent.com/19898602/161410625-b63463a8-01af-4bff-ba3e-bffd092be23c.png)

Here I have Nema 17 stepper motors the reason of using such motor because stepper motors are very precise many times not any feedback system required to controlling steps. 

Specifitaction of motor
Step Angle: 1.8 °
Current: 1.2 A/Phase
Holding Torque: 5.6 kg-cm
Detent torque: 2.8 N.cm (Maximum)
Lead Wires: 4
Shaft diameter: 5 mm(D-type)

![image](https://user-images.githubusercontent.com/19898602/161410680-771916cf-5bbe-472b-9dcd-b0723b3f4879.png)![image](https://user-images.githubusercontent.com/19898602/161410687-186d8171-9563-4af5-8e5d-cc3ad51a9d37.png)

Now the back side of stepper motors control the linear motion of stepper motor.
I have placed GT2 pulley to the shaft of both stepper motors.
And I placed a GT2 timing belt along the length of track of the profile.
And I engage the timing belt with the GT2 pulley of stepper motor with the help of 2 dummy pulleys.
So when shaft of motor rotate the whole whole system will slide accordingly.


# Master Arduino Code

```

#include <Arduino.h>
#include "BasicStepperDriver.h"
#include "MultiDriver.h"
#include "SyncDriver.h"

#define MOTOR_STEPS 200
#define MOTOR_X_RPM 200
#define MOTOR_Y_RPM 200

#define DIR_X 14
#define STEP_X 15

#define DIR_Y 16
#define STEP_Y 17

int L = 970;
#define MICROSTEPS 16


BasicStepperDriver stepperX(MOTOR_STEPS, DIR_X, STEP_X);
BasicStepperDriver stepperY(MOTOR_STEPS, DIR_Y, STEP_Y);


 //MultiDriver controller(stepperX, stepperY);

SyncDriver controller(stepperX, stepperY);

void setup() {
    
    stepperX.begin(MOTOR_X_RPM, MICROSTEPS);
    stepperY.begin(MOTOR_Y_RPM, MICROSTEPS);

delay(3000);
    
   controller.rotate(3600, -3600);
    controller.rotate(3600, -3600);
    controller.rotate(3600, -3600); 
 controller.rotate(2600, -2600);
    
}

void loop() {

    
    
}

```


# Slave Arduino code

```

#include <Arduino.h>
#include "BasicStepperDriver.h"
#include "MultiDriver.h"
#include "SyncDriver.h"

#define MOTOR_STEPS 200
#define MOTOR_X_RPM 200
#define MOTOR_Y_RPM 200

#define DIR_X 14
#define STEP_X 15

#define DIR_Y 16
#define STEP_Y 17

int L = 960;
int H = 1925;
#define MICROSTEPS 16


BasicStepperDriver stepperX(MOTOR_STEPS, DIR_X, STEP_X);
BasicStepperDriver stepperY(MOTOR_STEPS, DIR_Y, STEP_Y);


// MultiDriver controller(stepperX, stepperY);

SyncDriver controller(stepperX, stepperY);

void setup() {
    
    stepperX.begin(MOTOR_X_RPM, MICROSTEPS);
    stepperY.begin(MOTOR_Y_RPM, MICROSTEPS);

delay(2000);
    
    controller.rotate(0, -H);
   delay(3000);
   controller.rotate(0, H);

    controller.rotate(-H,0 );
   delay(3000);
   controller.rotate(H,0 );

   
   controller.rotate(-L, -L);
    delay(1000);
   // controller.rotate(L, L);
   //delay(1000);

    controller.rotate(-L/2, L/2);
    delay(1000);
    controller.rotate(L, -L);
    delay(1000);

   controller.rotate(-L/2, L/2);
    delay(1000);

   controller.rotate(L, L);
   delay(1000);
    
}

void loop() {

   
    
}

void first(){

   controller.rotate(-L, -L);
    delay(1000);
   // controller.rotate(L, L);
   //delay(1000);

    controller.rotate(-L/2, L/2);
    delay(1000);
    controller.rotate(L, -L);
    delay(1000);

   controller.rotate(-L/2, L/2);
    delay(1000);

   controller.rotate(L, L);
   delay(1000);
}

```

![MVI_0008_2_2](https://user-images.githubusercontent.com/19898602/161410915-4b3b8530-4f5b-4f0c-9d62-962202f3098a.gif)

