
# Mastering tools and techniques for data analysis

This is a [CINECA](http://www.cineca.it/) [course](http://www.hpc.cineca.it/content/training-events-list-2016).

A read-only version of our notebooks can be accessed with [nbviewer](http://nbviewer.jupyter.org/github/cineca-scai/lectures/tree/datanalytics/material/)
free service reading the GitHub repository.

## Prerequisites

* docker 1.9+

To install docker on a unix terminal, you can:

```
# Install docker
curl -sSL https://get.docker.com/ | sh
```

For Mac and Windows user the best way to get Docker tools working,
is using their new [toolbox](https://www.docker.com/toolbox).

## How to use lectures interactively

On a terminal, launch the docker image:

```
docker run -d \
    --name notebook \
    -e LECTURE_BRANCH=datanalytics \
    -e LECTURE_PATH=material \
    -h notebook
    -v cineca_spark_volume:/data/lectures \
    -p 80:8888 \
    cineca/nbsparkling

## Other operations:

# To freeze the container
docker stop notebook
# To remove the frozen container
docker rm notebook
```

### Access the web jupyter notebooks pages

Visit with your browser the jupyter running server at:

[http://localhost](http://localhost).

<small>Note: if you use docker on Mac or Windows, instead of *localhost* you
should find the virtual machine IP where Docker is running.
This is usually possible with commands like `boot2docker ip` or `docker-machine ip`.</small>
