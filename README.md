### Lithium Ion battery charger ( Update in progress )
#### Objective of the project: The objective of the project is to design a lithium Ion battery charger project using MSP430 series microcontrollers

![A-Brief-Introduction-to-MSP430-using-Launchpad-MSP430G2553](https://user-images.githubusercontent.com/26503600/227121366-362b866c-f650-4f66-8403-8dcf4cc90eec.jpg)


Project description: This project is done to illustrate, how to design a 3.7V Lithium ion battery charger using MSP430G2553 launchpad microcontrollers. The project is broken down into the following steps

* Study the Li battery chemistry / charging and discharging process
* Create / build project specifications
* Create the project block diagram
* Create the firmware flow for the project
* Build the project ( H/w \ S/w in phases)
* Integrate the sections
* Test
---------------------------------------------------------------------------------------------------------------------------------------------------------
#### Li battery charging and discharging concepts
A Lithium Ion battery charging consists of three stages
1. Slow charging / Pre charging stage / trickle charging: In this stage, the battery is charged at 0.1C, that is 1/10th capacity of the battery, if the battery voltage is less than 2.5 volts. For example a 500 mAh capacity battery is charged at the rate of 50 mA. 
2. Fast charge: This stage is started, once battery voltage reaches around 3 volts. In this stage, the battery is charged at 1C, i.e, at the rated current of the battery till the battery reaches to its maximum voltage of 4.2 volts.
3. Constant voltage charging: During this stage, the battery voltage is maintained at 4.1 - 4.2 volts, while the charging current falls to 0.1C of it's capacity. Once the charging current reaches around 0.1C, charging stops.

![Li charging](https://user-images.githubusercontent.com/26503600/227710560-2138c698-306c-4729-a79a-27565721297b.jpg)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
#### Project requirements
1. The system has to monitor three parameters, battery voltage, charge current and battery temperature continously.
2. The charging current has to be modulated / controlled based on PWM signal generated by the MSP controller
3. If battery voltage is less than 2.5V, the system has to be trickle charged at the rate ofd 0.1C
4. If the battery voltage is more than 3V, battery has to charge in C-V mode at the rate of 1C
5. Once battery voltage reaches 4.2 volts, and charge current drops below 10% of battery current, charging has to stop / terminate.
