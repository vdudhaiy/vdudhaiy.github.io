---
role: Undergraduate Student Researcher
employer: Purdue University
location: West Lafayette, IN
start_date: 2024-08-25
end_date: 2026-05-08
layout: default
summary: Member of the AI Omics research team with Dr. W. Andy Tao and Dr. Marco Hadisurya at Purdue, building a web application to process and analyse mass spectrometer data for proteomics research.
last_updated: 2026-06-02
---

# Undergraduate Student Researcher
{% if page.start_date %} {{ page.start_date | date: "%b %-d, %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %-d, %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

I was a member of the AI Omics research team with [Dr. W. Andy Tao](https://www.protaomics.org/) and Dr. Marco Hadisurya at Purdue University, participating through the [Vertically Integrated Projects (VIP)](https://engineering.purdue.edu/VIP) program.

The team's primary research objective was the **development of non-invasive diagnostic methods** for cancer and neurodegeneration diseases (such as Alzheimer's and Parkinson's), leveraging proteomics data from mass spectrometers. The work drew on diverse skills including statistics, data science, data visualization, and machine learning for data mining.

## My contribution

As an undergraduate researcher, I designed and built a **prototype web application** that automates key stages of mass spectrometer data preprocessing and statistical analysis. The application was designed to reduce human error during downstream data analysis tasks while remaining flexible enough for different experimental designs.

The stack consisted of:
- **React** — frontend interface for researchers to upload data and interact with results
- **Django** — backend API handling data processing and workflow orchestration
- **Python** — statistical and ML processing functions

A central part of the design process was iterative feedback from biochemists, whose input shaped workflow refinement, interface improvements, and feature prioritization throughout the project.

## The VIP program

The Vertically Integrated Projects program gave me the opportunity to contribute to real research as an undergraduate while also providing professional development opportunities in research communication. I delivered **poster presentations** and **research talks** at the Undergraduate Research Expo at Purdue during both Fall 2024 and Fall 2025, which deepened my appreciation for the research process and motivated me to pursue higher education.

<hr style="border: 1px solid #ccc; margin: 3rem 0;">

## Photo Highlights
<div style="display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center;">
  <figure style="width: 48%; text-align: center;">
    <img src="{{ '/assets/images/vip/poster_presentation.jpg' | relative_url }}" alt="Poster Presentation" style="width: 100%; height: auto;">
    <figcaption>Research Poster presentation at the Fall 2024 Undergraduate Research Expo at Purdue</figcaption>
  </figure>
  <figure style="width: 48%; text-align: center;">
    <img src="{{ '/assets/images/vip/research_talk.jpeg' | relative_url }}" alt="Research Talk" style="width: 100%; height: auto;">
    <figcaption>Delivering a Research Talk about our project during the Fall 2025 Undergraduate Research Expo at Purdue</figcaption>
  </figure>
</div>
