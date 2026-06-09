# RTOS_Anti-Lock_Braking_Sim (In-progress)

## Project Overview

## Parts List

1× Nucleo L4A6ZG (emulates ABS computer)
1× L298N Motor Driver 
2× DC Motors (emulates wheels)
2× LEDs (indicates braking and ABS activation)
2× Push Buttons (acts as soft and hard brake)
2× 560Ω Resistors (current limiting for LEDs)
1× 5V Power Module

## Hardware Layout

<img width="1957" height="1174" alt="image" src="https://github.com/user-attachments/assets/67ab4188-1d7b-4ecb-9215-0e8136b053ca" />

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


