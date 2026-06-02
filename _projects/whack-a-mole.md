---
title: Whack-A-Mole on STM32
start_date: 2024-09-01
end_date: 2024-11-30
layout: default
summary: A fully-featured Whack-A-Mole game in C on an STM32 microcontroller, using a 32x32 LED matrix, keypad, OLED display, and I2C EEPROM for persistent high scores — built for ECE 362.
last_updated: 2026-06-02
---

# Whack-A-Mole on STM32
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 362 — Microprocessors and Interfacing Systems** &nbsp;·&nbsp; Purdue University

A fully-functioning Whack-A-Mole game implemented in **C** on an **STM32 microcontroller**, driving a 32×32 LED matrix, keypad, OLED display, and persistent storage over I2C — all from scratch at the register level.

## Hardware used

| Component | Interface | Purpose |
|---|---|---|
| 32×32 LED matrix | GPIO (bitbanging) | Mole display with color |
| Keypad | GPIO | Username & level input, whack detection |
| OLED display | SPI | Live score display |
| Speaker | SPI | Sound effects |
| I2C EEPROM | I2C | Persistent high score storage |

## Features

- **60-second timed game** driven by hardware timers
- Startup screen for **username input** and **difficulty level selection** via keypad
- Moles appear at **random LED matrix positions** with varying colors, implemented via GPIO bitbanging
- Each correct whack registered via **hardware interrupts** for accurate real-time detection
- **Difficulty levels** control mole appearance/disappearance speed using timer adjustments
- **Sound effects** — distinct tones for hits and a "Game Over" melody, output over SPI
- **Top 3 high scores** saved persistently across power cycles using I2C EEPROM

## What I learned

Working at the register level in C — without an RTOS or hardware abstraction layer — gave me hands-on experience with GPIO, SPI, I2C, hardware timers, and interrupt-driven design. Debugging embedded systems without a runtime debugger (using LED blink patterns and careful register inspection) sharpened my low-level systems intuition considerably.

## Tech stack

C · STM32 · GPIO · SPI · I2C · EEPROM · Hardware timers · Interrupts
