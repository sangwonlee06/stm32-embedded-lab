# Project Index

This index maps the roadmap PDF into a practical lab sequence. The first ten projects form the core path, projects 11 and 12 are optional advanced extensions, and project 13 is the final integrated portfolio project.

| Directory | Status | Purpose |
| --- | --- | --- |
| `00-led-blink-baseline` | Planned | Confirm board, IDE, flash/debug setup, GPIO output, and simple hardware sanity checks. |
| `01-nonblocking-traffic-light` | Planned | Rewrite the traffic light as a non-blocking finite-state machine. |
| `02-pedestrian-button-polling` | Planned | Add debounced button input and a remembered pedestrian request. |
| `03-button-interrupt-debounce` | Planned | Convert button handling from polling to EXTI interrupt with debounce. |
| `04-uart-debug-console` | Planned | Print state changes, button events, and errors to a serial terminal. |
| `05-timer-pwm-led-dimmer` | Planned | Use a timer peripheral to fade an LED using PWM. |
| `06-adc-sensor-reader` | Planned | Read a potentiometer or analog sensor and print raw and voltage values. |
| `07-i2c-sensor-oled-display` | Planned | Communicate with an I2C sensor or SSD1306 OLED display. |
| `08-spi-sdcard-data-logger` | Planned | Log timestamped sensor data to CSV on a microSD card. |
| `09-uart-command-line-interface` | Planned | Add a serial command interface for status, sensor read, and logging control. |
| `10-freertos-sensor-dashboard` | Planned | Split sensing, display, logging, and command handling into RTOS tasks. |
| `11-can-rs485-industrial-communication` | Planned | Explore multi-node embedded communication for industrial-style systems. |
| `12-bootloader-basics` | Planned | Study flash layout, vector tables, and firmware update fundamentals. |
| `13-final-environmental-data-logger` | Planned | Combine the core peripherals into a polished real-time environmental logger. |

## Definition of Done for Every Project

- Hardware list is documented.
- Wiring is documented before firmware work starts.
- Build and flash steps are recorded.
- Debugging method is recorded.
- Demo output or video link is added.
- Known limitations are written down.
- Lessons learned are captured while fresh.

