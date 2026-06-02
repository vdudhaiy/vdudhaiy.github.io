---
title: 555 Timer Light Detector
start_date: 2023-11-01
end_date: 2023-11-30
layout: default
summary: A mini-project for ECE 20007 demonstrating the 555 timer in monostable and astable modes, with a practical light detector application built using an LDR and LED.
last_updated: 2026-06-02
---

# 555 Timer Light Detector
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 20007 — Electrical Engineering Fundamentals I Lab** &nbsp;·&nbsp; Purdue University &nbsp;·&nbsp; Mini-Project 2

This mini-project focused on the **555 timer IC** — one of the most widely used integrated circuits ever made. The objective was to demonstrate its operation in both of its primary modes and then apply it to a practical real-world circuit.

## Modes demonstrated

**Monostable mode** — The 555 timer produces a single output pulse of a fixed duration in response to a trigger input. Useful for debouncing, one-shot timers, and pulse generation.

**Astable mode** — The 555 timer oscillates continuously, producing a square wave at a frequency determined by the RC components. Useful for clocks, LED flashers, and tone generation.

## Real-world application: Light Detector

The practical application demonstrated was a **light detector** built with:
- **LDR (Light-Dependent Resistor)** — its resistance changes with ambient light level
- **555 timer** in astable mode — the LDR is wired into the RC timing network, so its resistance directly controls the oscillation frequency
- **LED** — flashes at a rate that varies with light intensity, visually indicating the detected light level

In bright light, the LDR's resistance drops, increasing the oscillation frequency and making the LED flash faster. In darkness, the LDR's high resistance slows the oscillation.

## What I learned

Working with the 555 timer made abstract concepts like RC time constants and threshold-triggered circuits tangible. The light detector demonstrated how a simple, passive sensor (the LDR) can be integrated into a timer circuit to create a light-responsive system without any digital logic.

## Tech stack

555 timer IC · LDR · LED · RC circuits · Breadboard prototyping
