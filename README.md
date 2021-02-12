# Dockerfile for Brightway

Based on the [Jupyter minimal notebook](https://github.com/jupyter/docker-stacks/tree/master/minimal-notebook).

## What it Gives You

* Miniconda
* Python 3.8
* Jupyterlab
* brightway2 framework

Docker instances are ephemeral. You will almost certainly want to mount a [data volume](https://docs.docker.com/storage/volumes/).

## Usage

To run an instance of Jupyter Lab, accessible at `localhost:10000`:

    docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes cmutel:brightway2

Jupyterlab also allows you to run iPython sessions or even a terminal.

See the [Jupyter documentation](https://github.com/jupyter/docker-stacks) for more usage options.
