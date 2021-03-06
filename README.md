# Iso2Flux
Version: 0.7

## Short Description

Open source software for steady state 13C flux analysis

## Description

Iso2Flux is a Python-based flux analysis software that allows to perform 13C Metabolic Flux Analysis on a sub-network of a large scale model. Iso2flux uses constraint-based modelling to compute steady state fluxes across a large metabolic network and uses such flxues to predict 13C distribution across a subser of the newtork. Then, given a set of 13C data Iso2flux can iteratively find the steady state flux distributions that are most consistent with such fluxes. 

## Key features

- Constraint-Based Modelling
- 13C Metabolic Flux Analysis

## Functionality

- Post-processing
- Statistical Analysis
- Workflows 

## Approaches

- Isotopic Labelling Analysis / 13C

## Instrument Data Types

- MS

## Screenshots


## Tool Authors

- Carles Foguet (University of Barcelona)
- Pedro de Atauri (University of Barcelona)
- Vitaly Selinvanov (University of Barcelona)
- Marta Cascante (Univesity of Barcelona)

## Container Contributors

- [Pablo Moreno](https://github.com/pcm32) 
- [Carles Foguet](https://github.com/cfoguet) 


## Website

- https://github.com/cfoguet/iso2flux


## Git Repository

- https://github.com/cfoguet/iso2flux

## Installation

Iso2flux is present on all PhenoMeNal Galaxy instances on deployed Cloud Research Environments, under the Fluxomics category in the tool bar to the left of the screen. No installation is needed hence on PhenoMeNal Cloud Research Environments.

For advanced Docker usage:

- Go to the directory where the dockerfile is.
- Create container from dockerfile:

```
docker build -t iso2flux .
```

Alternatively, pull from repo:

```
docker pull container-registry.phenomenal-h2020.eu/phnmnl/iso2flux
```


## Usage Instructions
 
On a PhenoMeNal Cloud Research Environment, go to Fluxomics tool category, and then click on iso2flux, and fill the expected input according to the detail above, then press Run. Additionally, the tool can be used as part of a workflow with Midcor, Ramid and the Escher-Fluxomics tools. On a PhenoMeNal deployed CRE you should find as well a Fluxomics Stationary workflow, which includes Iso2flux. 

Advanced usage through docker

```
docker run -it -v $PWD:/data container-registry.phenomenal-h2020.eu/phnmnl/iso2flux -e /data/tracing_data.csv -l /data/tracing_model.csv -s /data/sbml_model.xml -p parameters.csv -c constraints.csv -q 
```


## Publications
- Carles Foguet, Pedro de Atauri, Vitaly A. Selivanov, Marta Cascante. Iso2Flux: A new software for 13C fluxomics developed in the framework of PhenoMeNal
