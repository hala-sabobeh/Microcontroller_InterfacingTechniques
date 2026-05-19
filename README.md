# ENCS4380 – Microcontroller Systems | Homework 2

**Student:** Hala Sabobeh  
**Course:** Microcontroller Systems (ENCS4380)  
**Platform:** Arduino Uno (ATmega328P) — register-level programming (no Arduino HAL)

---

## Overview

This homework contains 5 questions, each implemented using direct AVR register manipulation.

---

## Questions

### Q1 – Custom LCD Driver (4-bit mode)
A bare-metal LCD driver written from scratch using direct port manipulation on `PORTB` and `PORTD`. Sends commands and data to a 16×2 LCD in 4-bit mode without any library.

### Q2 – Multi-LED Blinking (Non-blocking Timers)
Controls 5 LEDs (A–E) with different blink intervals using `millis()`-based non-blocking timing. Includes a phase-offset LED and a button-triggered LED. Uses `DDRB`/`PORTB` registers directly.

### Q3 – LCD Countdown Timer
A countdown timer displayed on a 16×2 LCD, implemented using a custom `Timer` class (`Timer.cpp` / `Timer.h`). Uses the `Timers_one_for_all` library. Wokwi simulation diagram included (`diagram_Q3.json`).

### Q4 – Hardware Interrupts (INT0 / INT1)
Button-driven counter using hardware interrupts configured via `EICRA`/`EIMSK` registers and `ISR()` macros — no `attachInterrupt()`. 
- **Button 1 (D2 / INT0):** Increment counter  
- **Button 2 (D3 / INT1):** Reset counter  
- **Bonus:** Pause/resume toggle via Button 3 (A0)

### Q5 – Traffic Light Controller with Pedestrian Crossing
A state-machine-based traffic light (Red / Yellow / Green) with a pedestrian crossing mode triggered by an interrupt on INT0. Uses `avr/interrupt.h` directly, with LCD status display and a blinking pedestrian LED.

---

## File Structure
<img width="638" height="305" alt="image" src="https://github.com/user-attachments/assets/ee6b69be-82bc-4628-b459-843f71219872" />
