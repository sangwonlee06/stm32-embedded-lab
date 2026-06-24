# 13 - Final Environmental Data Logger

## Goal

Combine the smaller projects into one polished STM32 real-time environmental data logger.

## Features

- Environmental sensor over I2C
- OLED display over I2C
- microSD logging over SPI
- UART command console
- FreeRTOS tasks for sensing, display, logging, and command processing
- Button input using interrupt and debounce
- LED status indicators

## Suggested Architecture

- Sensor task reads temperature, humidity, and pressure once per second.
- Display task shows latest values on the OLED.
- Logger task saves values to the SD card on a fixed interval.
- Command task receives UART commands.
- Button interrupt toggles logging on or off.
- Status LED indicates normal, paused, and error states.

## Completion Standard

- GPIO, interrupts, UART, I2C, SPI, and FreeRTOS are all represented.
- Sensor data flows through documented task boundaries.
- Logging can be started and stopped.
- Error states are visible through UART and LEDs.
- README includes architecture, wiring, commands, sample output, limitations, and lessons learned.

## Documentation To Add Later

- System architecture diagram
- Wiring diagram
- UART command reference
- Example CSV output
- Demo video link
- Portfolio write-up

## Implementation Status

Not implemented. This capstone directory is a documentation scaffold only.

