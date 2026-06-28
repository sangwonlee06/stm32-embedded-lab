# 01 - Non-Blocking Traffic Light

This lab drives three LEDs as a simple street light without using `HAL_Delay()`.

- `PA1` = red
- `PA2` = yellow
- `PA3` = green

The point of the exercise is straightforward: keep the main loop running, check time with `HAL_GetTick()`, and move to the next light when the current state's time is up.

## What the code is doing

The program keeps track of two things:

- the current light state
- when that state started

```c
typedef enum
{
  TRAFFIC_RED,
  TRAFFIC_YELLOW,
  TRAFFIC_GREEN
} TrafficState;

static TrafficState traffic_state = TRAFFIC_RED;
static uint32_t state_started_ms = 0;
```

Inside the main loop, it reads the current tick count and checks whether the current state has been active long enough.

```c
uint32_t now = HAL_GetTick();

if (traffic_state == TRAFFIC_RED) {
  HAL_GPIO_WritePin(GPIOA, GPIO_PIN_1, GPIO_PIN_SET);
  HAL_GPIO_WritePin(GPIOA, GPIO_PIN_2, GPIO_PIN_RESET);
  HAL_GPIO_WritePin(GPIOA, GPIO_PIN_3, GPIO_PIN_RESET);

  if ((now - state_started_ms) >= 3000U) {
    traffic_state = TRAFFIC_YELLOW;
    state_started_ms = now;
  }
}
```

The yellow and green sections work the same way. Each state writes all three outputs, then updates `traffic_state` and `state_started_ms` when it is time to move on.

## Sequence

The current timing is:

- red for 3 seconds
- yellow for 1 second
- green for 3 seconds

Then it loops back to red.

## Why this is non-blocking

There is no delay call stopping the CPU. The loop keeps running, so other work can still happen while the light is waiting for the next transition.

That is the main difference from a blocking version: time passes in the background, and the code only reacts when the elapsed time reaches the threshold.
