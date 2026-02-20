---
title: 'What is HPC?'
teaching: 40
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- How does a basic HPC cluster work?
- What does an HPC cluster look like?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- List the components of a basic HPC system.

::::::::::::::::::::::::::::::::::::::::::::::::

## HPC clusters 101

The previous episode already established that HPC clusters are made up of computers, which we call nodes, which are connected through a, typically high-speed, network.
Let's now dig into the different components of an HPC cluster and see how they work together.
HPC clusters will generally require the following basic components:

- nodes. There are different types of with specialised uses:
  - a login node is what the user uses to access the cluster
  - a compute node is what the user uses to run jobs. There are numerous compute nodes in a cluster.
  - storage, where files are stored. The nodes used for storage typically have more RAM than the compute nodes.
- a switch, which connects the login, compute, and storage nodes to allow them to act as a seamless unit. These are usually InfiniBand or other high-speed Ethernet to meet the low-latency, high-bandwidth requirements of HPC clusters.

<!-- is this stupid xD -->
- cables connecting the different nodes

![Schematic of an HPC cluster, from the [Yale Center for Research Computing.](https://docs.ycrc.yale.edu/clusters-at-yale/)](files/clusters.png)

The components listed until now are all hardware.
A very important piece of software when working on an HPC cluster is the _job scheduler_.
A job scheduler is essential because the resources of an HPC cluster are finite and the demand on those resources is usually very high.
When submitting a job, users have to specify how many resources (RAM and GPUs) they require and how long they expect their job to take.
The scheduler uses this information to prioritise jobs and make as efficient use of the resources as possible.
One of the most commonly used job schedulers is SLURM.
There will be more information on SLURM in the following episode.

## Different types of HPC

<!--
    constraints: memory, processors, discs. how do platforms differ? different kinds of HPC task require different resources (e.g. a lot of memory but little CPU vs lots of bandwidth)
    lots of computers that are similar to what your laptop but specialised
-->

## Visible HPC

<!--

Importance of visible HPC - the importance of the thing being there
this is representative of the real world

    pictures of big computers 😄
    point to small big computer in the room
    point to the different computers that are networked to each other (point to the cables)
    a core difference of HPC is that the nodes are connected with specialist hardware sometimes. this matters because there are different types of computation which can rely heavily on the connection between the nodes. this gets us to high throughput vs high performance. embarassingly parallel?
    exercise: example problems and ask if it's embarassingly parallel. are we able to give people enough information? could also be a discussion in a small group. props? knitting metaphor or addition

difference to a real HPC cluster
19 inch format in use for our cluster, which is standard. 12u (12 units in size) one server is one U etc.
a standard rack is 48u. if you put four of ours you get a dataserver

4 pis - 1U. Ours is a lot shallower than the real thing.

we can't have some of the real stuff - like hyperconnective cable because expensive and don't work with Pis

big switch is what you'd get in a datacenter rack! the switch is underperforming in our setup

the design is realistic - visual connection

-->



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

## Figures

You can include figures generated from R Markdown:

```{r pyramid, fig.alt = "pie chart illusion of a pyramid", fig.cap = "Sun arise each and every morning"}
pie(
  c(Sky = 78, "Sunny side of pyramid" = 17, "Shady side of pyramid" = 5), 
  init.angle = 315, 
  col = c("deepskyblue", "yellow", "yellow3"), 
  border = FALSE
)
```
Or you can use pandoc markdown for static figures with the following syntax:

`![optional caption that appears below the figure](figure url){alt='alt text for
accessibility purposes'}`

![You belong in The Carpentries!](https://raw.githubusercontent.com/carpentries/logo/master/Badge_Carpentries.svg){alt='Blue Carpentries hex person logo with no text.'}

## Math

One of our episodes contains $\LaTeX$ equations when describing how to create
dynamic reports with {knitr}, so we now use mathjax to describe this:

`$\alpha = \dfrac{1}{(1 - \beta)^2}$` becomes: $\alpha = \dfrac{1}{(1 - \beta)^2}$

Cool, right?

::::::::::::::::::::::::::::::::::::: keypoints 

- Use `.md` files for episodes when you want static content
- Use `.Rmd` files for episodes when you need to generate output
- Run `sandpaper::check_lesson()` to identify any issues with your lesson
- Run `sandpaper::build_lesson()` to preview your lesson locally

::::::::::::::::::::::::::::::::::::::::::::::::

