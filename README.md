# Dockerfile for Brightway

Based on the [Jupyter minimal notebook](https://github.com/jupyter/docker-stacks/tree/master/minimal-notebook).

## What it Gives You

* micromamba
* Python 3.11
* Jupyterlab
* brightway2 framework (see the [requirements.txt](requirements.txt) file for the details)

Docker instances are ephemeral. You will almost certainly want to mount a [data volume](https://docs.docker.com/storage/volumes/).

## Usage

To run an instance of Jupyter Lab, accessible at [localhost:8888](http://localhost:8888/):

    docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes brightway/bw2

Jupyterlab also allows you to run iPython sessions or even a terminal.

See the [Jupyter documentation](https://github.com/jupyter/docker-stacks) for more usage options.


## Installed bw dependencies

The bw2 specific dependencies correspond to the [brightway2 2.4.7](https://github.com/brightway-lca/brightway2) release. 
At build time for this image, they correspond to the following:


| Package             | Version  | Build             | Channel      |
|--------------------|----------|-------------------|--------------|
| bw2analyzer         | 0.10     | pyhd8ed1ab_0      | conda-forge  |
| bw2calc             | 1.8.2    | py311h38be061_0   | conda-forge  |
| bw2data             | 3.6.6    | pyhd8ed1ab_0      | conda-forge  |
| bw2io               | 0.8.12   | pyhd8ed1ab_0      | conda-forge  |
| bw2parameters       | 1.1.0    | pyhd8ed1ab_1      | conda-forge  |
| bw_migrations       | 0.2      | pyhd8ed1ab_1      | conda-forge  |
| ecoinvent_interface | 3.1      | pyhd8ed1ab_1      | conda-forge  |
| pypardiso           | 0.4.6    | pyhd8ed1ab_2      | conda-forge  |


## Tags

### brightway2

The [brightway2](https://github.com/brightway-lca/brightway2) docker images are currently built and
tagged based on the following different components of the image

+ brightway2 metapackage version (2.4.3)
+ python version (py310, py311, py312)
+ the python distribution (official python 3 or micromamba)



The following images are built:

| Image Name | components |
| ---------- | ---------- |
| brightway/bw2:latest | brightway 2.4.7, py311, micromamba|
| brightway/bw2:2.4.7-py311-micromamba | brightway 2.4.7, py311, micromamba|
| brightway/bw2:2.4.7-py310-micromamba | brightway 2.4.7, py310, micromamba|

