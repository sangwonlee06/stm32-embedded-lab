# 09 - UART Command-Line Interface

## Goal

Control firmware through serial commands such as status, sensor read, log start, and log stop.

## Hardware

- STM32 board
- UART connection
- Existing sensor/logger hardware
- Serial terminal on the computer

## Concepts

- UART receive
- Interrupt-based receive
- Ring buffer
- Command parser
- Firmware interface design

## Completion Standard

- Commands can be typed from the computer.
- STM32 responds over UART.
- Parser handles invalid commands.
- System does not freeze while waiting for input.
- README documents supported commands.

## Documentation To Add Later

- Command list
- Serial settings
- Parser behavior
- Error handling examples
- Demo video link
- Lessons learned

## Implementation Status

Not implemented. This directory is a documentation scaffold only.

