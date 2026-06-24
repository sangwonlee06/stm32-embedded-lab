# 10 - FreeRTOS Sensor Dashboard

## Goal

Build a multitasking firmware system with separate sensor, display, logger, and command tasks.

## Hardware

- STM32 board
- I2C sensor
- Optional OLED display
- Optional microSD card module
- UART connection
- Button and status LEDs

## Concepts

- Tasks
- Priorities
- Queues
- Semaphores
- Mutexes
- Race conditions
- Stack size

## Completion Standard

- FreeRTOS runs multiple tasks.
- Sensor data moves through a queue.
- Shared UART access is protected.
- No task blocks the whole system.
- README explains task responsibilities.

## Documentation To Add Later

- Task list and priorities
- Queue and mutex plan
- Timing diagram
- Demo video link
- Lessons learned

## Implementation Status

Not implemented. This directory is a documentation scaffold only.

