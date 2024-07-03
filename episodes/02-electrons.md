---
title: "Electrons"
teaching: 10
exercises: 30
---

:::::::: questions
- What are electromagnetic objects
- How are electrons treated in CMS?
- What variables are available in NanoAOD?
::::::::

:::::::: objectives
- Understand what electromagnetic objects are in CMS
- Learn electron member functions for common track-based quantities
- Learn variables for identification and isolation of electrons
- Learn variables for electron detector-related quantities
::::::::

::::::::::: prereq
## Prerequisites

We will be making some plots in the ROOT Docker container, `my_root`.

:::::::::::

## Motivation

In the middle of the workshop we will be working on the main activity, which is to attempt to replicate a [CMS physics analysis](https://link.springer.com/content/pdf/10.1007/JHEP09(2017)051.pdf) in a simplified way using modern analysis tools. The final state that we will be looking at contains electrons, muons and jets.  We are using these objects as examples to review the way in which we extract physics objects information.

The analysis requires some special variables, which we will need to identify in our Open Data NanoAOD files.

## Electromagnetic objects

We call photons and electrons **electromagnetic particles** because they leave most of their energy in the electromagnetic calorimeter (**ECAL**) so they share many common properties and functions

Many of the different hypothetical exotic particles are unstable and **can transform, or *decay*, into electrons**, photons, or both. Electrons and photons are also standard tools to measure better and understand the properties of already known particles.  For example, one way to find a Higgs Boson is by looking for signs of two photons, or four electrons in the debris of high energy collisions. Because electrons and photons are crucial in so many different scenarios, the physicists in the CMS collaboration make sure to do their best to reconstruct and identify these objects.

![](fig/brem.gif){width="50%"}

As depicted in the figure above, tracks -- from the pixel and silicon tracker systems -- as well as ECAL energy deposits are used to **identify** the passage of electrons in CMS.  Being charged, electron trajectories **curve** inside the CMS magnetic field.  Photons are similar objects but with no tracks.  Sophisticated algorithms are run in the **reconstruction** to take into account subtleties related to the identification of an electromagnetic particle.  An example is the convoluted **showering** of sub-photons and sub-electrons that can reach the ECAL due to *bremsstrahlung* and *photon conversions*.

We measure momentum and energy but also other properties of these objects that help analysts understand better their quality and origin. 

## Electron variables in NanoAOD

In the pre-exercises, you learned how to find NanoAOD datasets on the Open Data Portal. One example is the [SingleElectron dataset](https://opendata.cern.ch/record/30562). The "Dataset Semantics" section has a link to the [variable list webpage](https://opendata.cern.ch/eos/opendata/cms/dataset-semantics/NanoAOD/30562/SingleElectron_doc.html). Each "collection" of objects in the NanoAOD file is linked by a common naming scheme (ex: `Electron_*`). The individual variables are shown in a table that includes the branch name, the data type, and a brief descriptive comment.


:::::::: keypoints

- Quantities such as impact parameters and charge have common member functions.
- Physics objects in CMS are reconstructed from detector signals and are never 100% certain!
- Identification and isolation algorithms are important for reducing fake objects.

::::::::

