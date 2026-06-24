# 03 - Button Interrupt And Debounce

## Goal

Convert button handling from polling to an EXTI interrupt while keeping interrupt work short and predictable.

## Hardware

- STM32 board
- Push button
- LEDs from the traffic light project
- Breadboard and jumper wires

## Concepts

- External interrupts
- NVIC configuration
- Shared state and `volatile`
- ISR callback design
- Short interrupt handlers

## Completion Standard

- Button uses an EXTI interrupt.
- Interrupt handler only records the event or sets a flag.
- Shared variables are documented.
- Debouncing works.
- README explains interrupt handling versus polling.

## Documentation To Add Later

- Interrupt pin and trigger mode
- Debounce strategy
- Debugging notes
- Demo video link
- Lessons learned

## Implementation Status

Not implemented. This directory is a documentation scaffold only.

