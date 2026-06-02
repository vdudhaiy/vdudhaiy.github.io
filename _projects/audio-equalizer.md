---
title: Audio Equalizer
start_date: 2023-11-01
end_date: 2023-12-15
layout: default
summary: A three-band audio equalizer (bass, mid, treble) built on a breadboard for ECE 20007, using passive filters, op-amps, a summing amplifier, and a power amplifier.
last_updated: 2026-06-02
---

# Audio Equalizer
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 20007 — Electrical Engineering Fundamentals I Lab** &nbsp;·&nbsp; Purdue University &nbsp;·&nbsp; Final Project

This project involved designing and building a **three-band audio equalizer** on a breadboard, from component selection through testing with a real audio signal. The equalizer allows independent control of bass, mid, and treble frequency bands before mixing and amplifying the output.

## Circuit design

The signal path consisted of:

1. **Three passive filters** (bass, mid, and treble) — each tuned to pass a specific frequency band while attenuating the others
2. **Op-amp stages** — one per filter output to buffer and optionally amplify each band independently
3. **Summing amplifier** — combines the three filtered signals into a single mixed output
4. **Power amplifier** — drives the final output at sufficient current to power a speaker

## What I learned

This project connected the filter theory and op-amp circuits I had studied in lecture to a real, audible result. Choosing component values to hit target cutoff frequencies, dealing with real-world component tolerances, and verifying frequency response with an oscilloscope gave me practical experience that classroom exercises alone don't provide.

## Tech stack

Analog circuit design · Passive filters · Op-amps · Breadboard prototyping · Oscilloscope verification
