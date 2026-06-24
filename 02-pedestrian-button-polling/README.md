# 02 - Pedestrian Button With Polling

## Goal

Add a push button to the traffic light. When pressed during green, remember the pedestrian request, transition to yellow, then red, and hold red longer.

## Hardware

- STM32 board
- Red, yellow, and green LEDs
- Push button
- Resistors as needed
- Breadboard and jumper wires

## Concepts

- GPIO input
- Internal pull-up or pull-down configuration
- Software debouncing
- Event flags
- State machine expansion

## Completion Standard

- Button press is detected.
- Button bounce does not cause repeated triggers.
- Traffic light remembers the request.
- System remains non-blocking.
- README explains the debounce approach.

## Documentation To Add Later

- Button wiring and pull configuration
- Debounce timing notes
- Demo video link
- Known limitations
- Lessons learned

## Implementation Status

Not implemented. This directory is a documentation scaffold only.

