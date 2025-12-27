---
role: Undergraduate Student Researcher
employer: Purdue University
location: West Lafayette, IN
start_date: 2024-08-25
layout: default
summary: I am a member of the AI Omics research team with Dr. W. Andy Tao at Purdue University currently working on developing a statistical analysis application for proteomics research for reserachers at the Tao Research Group.
last_updated: 2025-12-27
---

# Undergraduate Student Researcher
{% if page.start_date %} {{ page.start_date | date: "%b %-d, %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %-d, %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

I am involved in [Vertically Integrated Projects (VIP)](https://engineering.purdue.edu/VIP), a program that provides the opportunity to undergraduate students to take part in research for academic credit. Through this program, I have been a member of the AI Omics team under the [Tao Research Group](https://www.protaomics.org/). 

The Tao Research Group's primary objective is to conduct research in the field of proteomics by analysing mass spectrometer data for early onset signs of diseases like Alzheimer's and Parkinson’s. 

The project that I am working on aims to reduce human error, improve interpretability, and standardize proteomics workflows across research environments. We have developed a deployable, user-friendly application that automates key stages of preprocessing and statistical analysis while preserving flexibility for different experimental designs. The application consists of a React-based frontend, a Django-based backend, and statistical/ML functions implemented in Python. A central part of the design process involves iterative feedback from biochemists, whose input is guiding workflow refinement, interface improvements, and feature prioritization. 

I’ve delivered some research talks and poster presentations on this project at the Undergraduate Research Expo held at Purdue each semester, and this exposure to the research world has motivated me to pursue higher education. 

<hr style="border: 1px solid #ccc; margin: 3rem 0;">

## Photo Highlights
<div style="display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center;">
  <figure style="width: 48%; text-align: center;">
    <img src="{{ '/assets/images/vip/poster_presentation.jpg' | relative_url }}" alt="Poster Presentation" style="width: 100%; height: auto;">
    <figcaption>Research Poster presentation at the Fall 2024 Undergraduate Research Expo at Purdue</figcaption>
  </figure>
  <figure style="width: 48%; text-align: center;">
    <img src="{{ '/assets/images/vip/research_talk.jpeg' | relative_url }}" alt="Research Talk" style="width: 100%; height: auto;">
    <figcaption>Delivering a Research Talk about our project during the Fall 2025 Undergraduate Research Expo at Purdue .
    </figcaption>
  </figure>
</div>