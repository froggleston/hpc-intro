---
title: "Why use HPC?"
teaching: 10
exercises: 0
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
        icebreaker questions: what % of research uses programming/what DRI or HPC facilities are you aware of in your institution?
        Research is increasingly computational
        Side effect of this is that researchers need to process more and more complex data and access more computing resources to do so
        undertake more advanced computations
        specialised computing power is needed
        why is a laptop not enough (give examples). comparing computational power of a laptop (e.g. this many calculations per second on a computer versus on HPC)
        case studies (pick and choose depending on audience)
        relationship between HPC and AI
        exercise ideas: researcher personas with research projects - do they need HPC?

-->

HPC stands for High-Performance Computing and refers to the use of powerful computers and programming techniques to solve computationally-intensive tasks.
Very often, several of these high-performance computers are connected together in a network and work as a unified system, forming a HPC cluster.
HPC clusters typically consist of numerous nodes (computers) connected through a high-speed network, and they are used to distribute and parallelise tasks.

The main reason that researchers use HPC clusters is that regular computers do not have enough resources to run the analysis or computation of interest.
By _resources_ here we mean memory, processors, disk space or network bandwidth.

Let's look at some specific cases in which researchers required the use of an HPC cluster.

## Case study 1: Astrophysics
HPC was instrumental in capturing the first ever image of a black hole in 2019.

[Source](https://prace-ri.eu/hpc-supports-first-black-hole-image/)

## Case study 2: Engineering
HPC is being used to model the performance of floating platforms for floating wind turbines.

[Source](https://ni-hpc.ac.uk/CaseStudies/WindTurbineModelling/#d.en.1380908)

## Case study 3: Biology
HPC was fundamental in the creation of the neural network AlphaFold, which is highly accurate in predicting the structure of proteins.

[Source](https://www.embl.org/news/science/alphafold-using-open-data-and-ai-to-discover-the-3d-protein-universe/)

## Case study 4: Cognitive science


:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

The information presented here has been copied and lightly adapted from:
- **[Working on HPC clusters using SLURM](https://cambiotraining.github.io/hpc-intro/materials/01-intro.html)**
- **[Introduction to High Performance Computing with Raspberry Pi](https://scw-aberystwyth.github.io/Introduction-to-HPC-with-RaspberryPi/01-HPC-intro/)**

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge 

## Challenge 1: Can you do it?

What is the output of this command?

```r
paste("This", "new", "lesson", "looks", "good")
```

:::::::::::::::::::::::: solution 

## Output
 
```output
[1] "This new lesson looks good"
```

:::::::::::::::::::::::::::::::::


## Challenge 2: how do you nest solutions within challenge blocks?

:::::::::::::::::::::::: solution 

You can add a line with at least three colons and a `solution` tag.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::



::::::::::::::::::::::::::::::::::::: callout

Callout sections can highlight information.

They are sometimes used to emphasise particularly important points
but are also used in some lessons to present "asides": 
content that is not central to the narrative of the lesson,
e.g. by providing the answer to a commonly-asked question.

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 

- Use `.md` files for episodes when you want static content
- Use `.Rmd` files for episodes when you need to generate output
- Run `sandpaper::check_lesson()` to identify any issues with your lesson
- Run `sandpaper::build_lesson()` to preview your lesson locally

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
