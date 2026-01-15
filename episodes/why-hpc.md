---
title: "Why use HPC?"
teaching: 20
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
Think, for example, of huge text datasets that comprise the entirety of Wikipedia or Reddit, or of sensor data coming from structures like bridges and tunnels and contain information on structural vibrations, seismic activity etc.
Or, think of the hugely complicated climate models that scientists run to predict the impacts of the climate crisis or of the training required for Machine Learning models.
Processing huge datasets or running calculations of this complexity requires a lot of computing power, more than an individual laptop or work station can provide.

To get around this problem, researchers may turn to High-Performance Computing (HPC) which provides more resources to run the analysis or computation of interest.
By _resources_ here we mean memory, processors, disk space, network bandwidth, or a combination of any of them.
To give a taste of the difference between HPC and regular computers, an HPC cluster can be 1 million times faster than the fastest laptop, [according to IBM](https://www.ibm.com/think/topics/supercomputing). (note: this is dependent on code efficiency and how parallelisable the problem is)
Another example, from the EPCC, is the cross-validation of a statistics model:
if running the model once takes one hour, cross-validating it 1,000 times on a laptop would take over a month!
If all of the model runs happen in parallel on an HPC cluster, the crossvalidation would be complete in one hour.

> ABM as methodological tool necessitates running the simulation many times, and by many, I mean eight hundred thousand times, and that is possible with a laptop… if one plans to be doing their Ph.D. for 500 years.
> Supercomputing is bigger, faster, better without any qualitative change in terms of the research.

Iza Romanowska, Assistant Professor at Aarhus University

[Source](https://interactivehpc.dk/?p=1358)

## Case studies

Let's now look at some specific cases in which the use of an HPC cluster enabled impactful research.

### Case study 1: Astrophysics

<!-- to include for each
1. introduction
2. how is HPC implicated?
3. what does this work matter?
4. sources
-->

Most of us will remember the first image of a black hole, which was captured in 2019.
This would not have been possible without HPC!
Scientists collected data using eight telescopes located around the world, which were then transferred to two supercomputers for processing.
Advances in chip technology made it possible to measure the radiation emitted from the black hole at different frequencies, increasing sensitivity and quality of the data captured.
Then, the superior processing power of the two supercomputers made it possible to combine the data from all eight telescopes at high speeds.

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

What is the output of this command?

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
