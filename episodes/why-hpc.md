---
title: "Why use HPC?"
teaching: 30
exercises: 10
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are good use cases for a High-Performance Computing (HPC) cluster?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explain when using an HPC cluster is a good idea.

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

<!--

Why HPC? (aim: 30 minutes)
  icebreaker questions: what % of research uses programming/what DRI or HPC facilities are you aware of in your institution? - 
  Research is increasingly computational
  Side effect of this is that researchers need to process more and more complex data and access more computing resources to do so
  undertake more advanced computations
  specialised computing power is needed
  why is a laptop not enough (give examples). comparing computational power of a laptop (e.g. this many calculations per second on a computer versus on HPC)
  case studies (pick and choose depending on audience)
  relationship between HPC and AI
  exercise ideas: researcher personas with research projects - do they need HPC?
-->

::::::::::::::::::::::::::::::::::::: challenge 

## Icebreaker questions

What Digital Research Infrastructure facilities are you aware of in your institution?

:::::::::::::::::::::::::::::::::

Scientific research is becoming increasingly computational [(Foster, 2011)](https://doi.org/10.7208/9780226038322-002).
Think, for example, of huge text datasets that comprise the entirety of Wikipedia or Reddit, or of sensor data from structures like bridges and tunnels, containing information on vibrations, seismic activity etc.
To make this more concrete, let's look at some studies that have tried to quantify this change:
One study looking at the size of medical image datasets used for research found that the median dataset size in 2018 was up to 10 times larger compared to 2011 ([Kiryati & Landau, 2021](https://doi.org/10.3390/jimaging7080155)).
Another study looking at big data in industry and academia, reports that the data that CERN records in a year is projected to increase from 160 petabytes in 2018 to 800 petabytes in 2026 ([Clissa, Lassnig, & Rinaldi, 2023](https://doi.org/10.3389/fdata.2023.1271639)).
Or, think of the hugely complicated climate models that scientists run to predict the impacts of the climate crisis.
Processing huge datasets or running calculations of this complexity requires a lot of computing power, more than an individual laptop or work station can provide.

To get around this problem, researchers may turn to High-Performance Computing (HPC) which refers to the use of powerful computers and programming techniques to solve computationally-intensive tasks.
HPC can refer to custom-built *supercomputers* or groups of individual computers that are connected together in a network and work as a unified system, forming a *cluster*.
We call these indivisual computers of a cluster *nodes*.
To give a taste of the benefit of using HPC over a regular computer, let's look at an example:
A PhD student wants to cross-validate a statistical model 1,000 times.
Running the model once on a laptop once takes one hour, meaning that cross-validating it 1,000 times would take over a month!
However, if all of the model runs happen in parallel on 1,000 nodes of an HPC cluster, the cross-validation would be complete in one hour.
How much research can be sped up is highly dependent on how efficient the code is and how parallelisable the problem.

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

The information presented here has been copied and lightly adapted from:

- **[Working on HPC clusters using SLURM](https://cambiotraining.github.io/hpc-intro/materials/01-intro.html)**
- **[Introduction to High Performance Computing with Raspberry Pi](https://scw-aberystwyth.github.io/Introduction-to-HPC-with-RaspberryPi/01-HPC-intro/)**

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

## Case studies

Let's now look at some specific cases in which the use of an HPC cluster enabled impactful research.

### Case study 1: Physics

<!-- to include for each
1. introduction
2. how is HPC implicated?
3. why does this work matter?
4. sources
-->

Most of us will remember the first image of a black hole, which was captured in 2019.
This would not have been possible without HPC!
Scientists collected data using eight telescopes located around the world, which were then transferred to two supercomputers for processing.
The superior processing power of the two supercomputers made it possible to combine the data from all eight telescopes at high speeds.

- [Source 1](https://prace-ri.eu/hpc-supports-first-black-hole-image/)
- [Source 2](https://eventhorizontelescope.org/technology)

### Case study 2: Engineering
Researchers from Queen's University Belfast are using HPC to model the performance of offshore and coastal structures.
This work places special emphasis on the behaviour of floating wind turbines, which are used to generate renewable energy.
Wind turbines that are further away from the coast benefit from, for example, stronger and more consistent wind, but their stability can suffer from the more adverse weather.
Modelling the various factors and their interactions that can affect their stability would be impossible without HPC infrastructure.

[Source](https://ni-hpc.ac.uk/CaseStudies/WindTurbineModelling/#d.en.1380908)

### Case study 3: Biology
HPC was fundamental in the creation of the neural network AlphaFold, which is highly accurate in predicting the structure of proteins.
This is incredibly important work that enables the discovery of new drugs.

[Source](https://www.embl.org/news/science/alphafold-using-open-data-and-ai-to-discover-the-3d-protein-universe/)

### Case study 4: Archaelogy
Researchers at the University of Bradford used their local HPC cluster to recreate 3D models of degraded sites.

[Source](https://www.techmonitor.ai/technology/data/university-of-bradford-hpc?cf-view)

::::::::::::::::::::::::::::::::::::: challenge 

## What kind of resources does this researcher need?

- Analyse survey responses from 300 human participants.
- Run a climate model simulation at high spatial resolution.
- Train a Large Language Model.
- Run a simple regression on CSV data (50 MB).

:::::::::::::::::::::::: solution 

## Solution
 
- Analyse survey responses from 300 human participants.
  - Answer: laptop
- Run a climate model simulation at high spatial resolution.
  - Answer: HPC
- Train a Large Language Model.
  - Answer: HPC
- Run a simple regression on CSV data (50 MB).
  - Answer: laptop

:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: callout

High-Performance Computing and Artificial Intelligence

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 

- Research is becoming more computational and, as such, requires more powerful computers.
- HPC enables research in various disciplines.
- AI is a field that often requires HPC resources.

::::::::::::::::::::::::::::::::::::::::::::::::
