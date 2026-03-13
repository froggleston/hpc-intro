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
  - interactive (or login) nodes are used to access the cluster
  - compute node are used to run jobs. There are numerous compute nodes in a cluster.
  - storage, where files are stored. The nodes used for storage may have more RAM than the compute nodes.
- a switch, which connects the login, compute, and storage nodes to allow them to act as a seamless unit. These are usually InfiniBand or other high-speed Ethernet to meet the low-latency, high-bandwidth requirements of HPC clusters.

<!-- is this stupid xD -->
- cables connecting the different nodes

![Schematic of an HPC cluster, from the [Yale Center for Research Computing.](https://docs.ycrc.yale.edu/clusters-at-yale/)](files/clusters.png)

The components listed until now are all hardware.
A very important piece of software when working on an HPC cluster is the _job scheduler_.
A job scheduler is essential because the resources of an HPC cluster are finite and the demand on those resources is usually very high.
When submitting a job, users have to specify how many resources (RAM and GPUs) they require and how long they expect their job to take.
The scheduler uses this information to prioritise jobs and make as efficient use of the resources as possible.
One of the most commonly used job schedulers is Slurm.
There will be more information on Slurm in the following episode.

## Different types of HPC

<!-- if only embarassingly parallel, rethink how sections work -->

We've talked about the different hardware components of an HPC cluster that determine the system's computing power, bandwidth and memory storage.
These can be configured in bespoke ways to suit the type of problem at hand.
For example, some problems require a lot of storage space but little CPU, while others may require the opposite.

### Embarassingly parallel

Some scientific problems require running the same programme multiple times, but with different parameters.
Each run of the programme is completely independent from the rest, i.e. its run does not rely on the outcome of any other run.
In this case, all runs can happen in parallel on separate CPUs and everything is combined at the very end.
This would be an example of an "embarassingly parallel" task.

This relates to the concept of *high-throughput computing*, which not only runs multiple jobs in parallel and independently, but does so on *ordinary computers*.
This means that the nodes used in these systems are not specialised, but very similar to what you would use in your own laptop.

For embarassingly parallel tasks, priority is on a large number of CPUs, with a high-speed low-latency interconnect being less important.

<!--
### Shared memory parallelism

A different kind of scientific question might rely on the analysis of very large datasets.
Here, CPUs are able to work on tasks independently, but they all need access to the same dataset.

For this kind of tasks, all CPUs need to be part of the same node and have access to the same RAM.
-->
### Message Parsing Interface (MPI) parallelism

Sometimes, jobs can be parallelised to an extent but cannot be run completely independently of each other, but need to exchange information.
Generally this is the case because the different chunks of the task that needs to be completed can only be in a certain order.

In those cases, a high-speed low-latency interconnect is much more important compared to an embarassingly parallel task.

<!--
    constraints: memory, processors, discs. how do platforms differ? different kinds of HPC task require different resources (e.g. a lot of memory but little CPU vs lots of bandwidth)
    lots of computers that are similar to what your laptop but specialised
    specialist hardware matters because there are different types of computation which can rely heavily on the connection between the nodes. this gets us to high throughput vs high performance.
-->

::::::::::::::::::::::::::::::::::::: challenge 

## Will it embarassingly parallel

What is the output of this command?

```r
paste("This", "new", "lesson", "looks", "good")
```

:::::::::::::::::::::::: solution 

## Solution
 
```output
[1] "This new lesson looks good"
```

:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

## Visible HPC

<!--

Importance of visible HPC - the importance of the thing being there
this is representative of the real world

    pictures of big computers 😄
    point to small big computer in the room
    point to the different computers that are networked to each other (point to the cables)
    a core difference of HPC is that the nodes are connected with specialist hardware sometimes
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

## Challenge 2: how do you nest solutions within challenge blocks?

:::::::::::::::::::::::: solution 

You can add a line with at least three colons and a `solution` tag.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 



::::::::::::::::::::::::::::::::::::::::::::::::

