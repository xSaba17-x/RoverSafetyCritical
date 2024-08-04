# RoverSafetyCritical
The code was developed in C using STM32CubeIDE. The aim is to use two MCUs, STM32F401RE, to control the rover. The two MCUs are used to ensure redundancy and diversity. To achieve this, communication between them is necessary. The features developed are:
1) Collecting input using SPI communication with a PS2 controller.
2) Activating an emergency brake if the ultrasonic sensors detect an obstacle.
3) If the Slave MCU fails, the Master puts the rover into a degraded mode, in which the maximum speed is reduced.
4) If the Master MCU fails, the Slave stops the rover.
5) Since there is communication between the master and slave, there is the possibility that communication may fail for various reasons while both MCUs are still operational. To ensure a deterministic decision, when one MCU believes the other is non-functional, the operational MCU will cut off the power to the other using a relay.

Other minor features are developed, try to find them :)
