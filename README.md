# STM32 Embedded Systems Lab

Documentation-first project lab based on `Embedded_Systems_Developer_Project_Roadmap.pdf`.

This repository is a scaffold for learning embedded firmware on STM32. It intentionally contains no firmware implementation yet. Each project directory has planning documents, completion standards, wiring notes, and demo documentation placeholders so implementation can be added later one project at a time.

## Goal

Build a junior embedded systems portfolio that demonstrates:

- C programming for microcontrollers
- GPIO, interrupts, timers, PWM, ADC, UART, I2C, SPI, and FreeRTOS
- Debugging with ST-Link, breakpoints, watch variables, UART logs, and a logic analyzer
- Clean documentation with wiring notes, demo links, known limitations, and lessons learned

## Lab Rules

- Do not add firmware code until you are actively working on a project.
- Keep each project independently documented.
- Every project README should explain the goal, hardware used, wiring, embedded concepts, build and flash steps, sample output, known limitations, and lessons learned.
- Prefer small, polished demos over large unfinished systems.
- Commit documentation and project setup separately from implementation work.

## Project Ladder

| Order | Project | Main Skills | Portfolio Value |
| --- | --- | --- | --- |
| 00 | LED blink baseline | GPIO output, toolchain setup | Establishes the known-good board setup |
| 01 | Non-blocking traffic light | State machines, non-blocking timing | Converts LED demos into firmware architecture |
| 02 | Pedestrian button polling | GPIO input, pull-ups, debounce, event flags | Shows real-world input handling |
| 03 | Button interrupt and debounce | EXTI, NVIC, volatile, ISR rules | Shows interrupt understanding |
| 04 | UART debug console | Serial output, logs, printf redirection | Shows debugging discipline |
| 05 | Timer PWM LED dimmer | Timers, prescaler, period, duty cycle | Shows hardware timer use |
| 06 | ADC sensor reader | Analog input, voltage scaling, sampling | Shows sensor input basics |
| 07 | I2C sensor or OLED display | I2C, addresses, registers, drivers | Demonstrates a useful beginner peripheral |
| 08 | SPI SD card data logger | SPI, chip select, FatFS, CSV logging | Looks like a real product feature |
| 09 | UART command-line interface | RX interrupt, ring buffer, parser | Shows firmware interface design |
| 10 | FreeRTOS sensor dashboard | Tasks, queues, mutexes, priorities | Strong junior-level project |
| 11 | CAN or RS-485 communication | Industrial bus, multi-node design | Useful for robotics, automotive, and industrial roles |
| 12 | Bootloader basics | Flash, vector table, memory layout | Advanced portfolio differentiator |
| 13 | Final environmental data logger | Integrated peripherals and RTOS | A complete portfolio capstone |

## Repository Structure

```text
stm32-embedded-lab/
  docs/
  assets/
  00-led-blink-baseline/
  01-nonblocking-traffic-light/
  02-pedestrian-button-polling/
  03-button-interrupt-debounce/
  04-uart-debug-console/
  05-timer-pwm-led-dimmer/
  06-adc-sensor-reader/
  07-i2c-sensor-oled-display/
  08-spi-sdcard-data-logger/
  09-uart-command-line-interface/
  10-freertos-sensor-dashboard/
  11-can-rs485-industrial-communication/
  12-bootloader-basics/
  13-final-environmental-data-logger/
```

Each project contains:

- `README.md` - project plan and completion checklist
- `docs/wiring.md` - wiring notes placeholder
- `docs/demo.md` - demo capture and output placeholder
- `src/README.md` - reminder that implementation is intentionally absent

## Suggested Hardware

Minimum useful kit:

- STM32 Nucleo-F446RE or an existing STM32 Discovery board
- Breadboard, jumper wires, LEDs, and 220 ohm or 330 ohm resistors
- Push buttons and potentiometer
- BME280 or SHT31 sensor
- SSD1306 OLED display
- microSD card module
- Cheap logic analyzer
- Multimeter

Optional later:

- Second STM32 board
- CAN transceiver modules
- RS-485 modules
- Small DC motor and motor driver
- Encoder
- Servo motor

## Exact Next Action

Start with `01-nonblocking-traffic-light` after confirming the LED blink baseline works. The first polished portfolio milestone is:

- no blocking delay calls
- tick-based timing
- enum-style state model
- separate update and hardware-control responsibilities
- red, yellow, and green LEDs
- README documentation
- demo video link

