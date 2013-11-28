This repository contains the profiling results of running Keshmesh on several
projects.

# Procedure

For each project we obtain the profiling results as follows.

- Repeat the steps below for each level of [object sensitivity](https://github.com/reprogrammer/keshmesh/wiki/Configuring-Keshmesh) from 1, 2, and 3.
  - Repeat the steps below **five** times.
    1. Restart Eclipse to make sure that results of previous runs of Keshmesh are not cached.
    1. Run Keshmesh through the FindBugs interface.
    1. Store the [profiling
    results](https://github.com/reprogrammer/keshmesh/wiki/Profiling-Keshmesh) of
    Keshmesh.

# Machine

- Ubuntu Release 12.04 (precise) 64-bit
- Kernel Linux 3.5.0-43-generic
- Processor: Intel Core 2 Quad CPU Q8200 @ 2.33GHz × 4 

# Java

- java version "1.6.0_45"
- Java(TM) SE Runtime Environment (build 1.6.0_45-b06)
- Java HotSpot(TM) 64-Bit Server VM (build 20.45-b01, mixed mode)

# Eclipse

- Eclipse for RCP and RAP Developers
- Version: Helios Service Release 1
- Build id: 20100917-0705
- Keshmesh v1.0.0.201311271834
- -XX:MaxPermSize=256m -Xms40m -Xmx512m

