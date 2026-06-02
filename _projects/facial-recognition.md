---
title: Facial Recognition System
start_date: 2023-03-01
end_date: 2023-04-30
layout: default
summary: A group final project for ENGR 10301 (Introduction to Engineering in Practice) that uses a webcam to identify faces in a captured image and label them against a known reference set.
last_updated: 2026-06-02
---

# Facial Recognition System
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ENGR 10301 — Introduction to Engineering in Practice** &nbsp;·&nbsp; Purdue University &nbsp;·&nbsp; Group Final Project

This was the final group project for ENGR 10301, Purdue's introductory engineering course. The project was completed on **Google Colab** and used the computer's webcam to capture an image and identify faces within it by comparing them against a set of reference photos uploaded to the notebook.

## How it works

1. A reference set of labelled face images is uploaded to the Colab environment
2. The system captures an image using the computer's webcam
3. Each detected face in the captured image is compared against the reference set using a facial recognition library
4. **Identified faces** are highlighted with a **green bounding box** and labelled with the person's name
5. **Unrecognized faces** are highlighted with a **red bounding box** and labelled "Unknown"

## What I learned

This project was my first experience applying Python to a real-world problem. Working on a team, splitting up tasks, and integrating each person's contribution into a single working notebook introduced me to collaborative coding practices early in my engineering education.

## Tech stack

Python · Google Colab · Face recognition library · Webcam capture · NumPy
