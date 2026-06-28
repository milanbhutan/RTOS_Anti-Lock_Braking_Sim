# RTOS_Anti-Lock_Braking_Sim (In-progress)

## Project Overview
The purpose of this project is to model an anti-lock braking system using FreeRTOS and hardware peripherals. Anti-lock braking systems are present on almost every vehicle and are especially important as they provide increased driver control during dangerous hard braking events. During hard braking, variations of car weight distribution cause some wheels to be locked leading to vehicle slippage. The ABS system will mitigate this slippage by pulsing locked wheels, allowing the driver to steer during hard braking. While this project cannot perform this brake pulsing and fully demonstrate the entire ABS system we can still model the detection of wheel slip and indicate the need for ABS activation on locked up wheels using LEDs. Separate FreeRTOS tasks for ABS activation, motor slip detection, and motor control will be scheduled to ensure high priority tasks like the ABS activation can meet their deadlines.

## Parts List
- 1× Nucleo L4A6ZG (emulates ABS computer)
- 1× L298N Motor Driver 
- 2× DC Motors (emulates front wheels)
- 2× LEDs (indicates braking and ABS activation)
- 2× Push Buttons (acts as soft and hard brake)
- 2× 560Ω Resistors (current limiting for LEDs)
- 1× 5V Power Module

## Hardware Layout

<img width="1957" height="1174" alt="image" src="https://github.com/user-attachments/assets/67ab4188-1d7b-4ecb-9215-0e8136b053ca" />

The Nucleo L4A6ZG sits at the center of the circuit, handling all control logic. Two push buttons are connected to GPIO input pins PC0 and PC1 with internal pull-ups, used to trigger soft and hard braking events. PWM signals are output from PA0 and PA1 to the ENA and ENB enable pins of the L298N motor driver, which controls the speed of the two DC motors via its OUTA and OUTB channels. The L298N is powered by an external 5V power module to supply enough current for the motors. Two LEDs are connected to GPIO output pins PB0 and PB1 through 560Ω current-limiting resistors to indicate braking and ABS activation status.

## Opening in STM32CubeIDE

1. Clone this repository.
2. Open STM32CubeIDE.
3. Go to File > Import > Existing Projects into Workspace.

<img width="1197" height="998" alt="image" src="https://github.com/user-attachments/assets/fa253afd-b6cc-43aa-9e8d-884ec4943588" />

4. Select the cloned repository folder.
5. Click Finish.
6. Build the project.
7. When running the project for the first time on the STM32 board create the debug configuration by right-clicking on the project and go to, Debug As > STM32 C/C++ Application.

<img width="540" height="555" alt="image" src="https://github.com/user-attachments/assets/5888d326-1056-4f23-a04a-6cddf0212527" />


8. Click "Finish" to create your Debug file and then click on the green bug at the top of the IDE to start debugging.

<img width="747" height="137" alt="image" src="https://github.com/user-attachments/assets/47c99b63-c2a8-443f-bb63-ec1917ac4809" />


9. Click on the Resume bottom at the top of the IDE and to start running the code on the board.

<img width="453" height="94" alt="image" src="https://github.com/user-attachments/assets/d122a09c-f8b2-4a07-9e18-ac3fde8c12f3" />


