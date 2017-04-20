# pseudogene / contiguator

[![Docker Pulls](https://img.shields.io/docker/pulls/pseudogene/contiguator.svg)](https://hub.docker.com/r/pseudogene/contiguator/)
[![Layers](https://images.microbadger.com/badges/image/pseudogene/contiguator.svg)](https://microbadger.com/images/pseudogene/contiguator)

## Short Description
A bacterial genomes finishing tool for structural insights on draft genomes - Now in a Docker

## Disclamer

CONTIGuator is no longer actively maintained (except for small bugfixes and requests)! Contiguator's authors strongly suggest to use [Medusa](http://combo.dbe.unifi.it/medusa) instead

## Full Description
Supported tags and respective Dockerfile links

 * `2.7.5`, `latest` ([`Dockerfile`](https://github.com/pseudogene/contiguator/blob/master/Dockerfile))

For more information about this image and its history, please see the relevant manifest file. This image is updated via pull requests to the `contiguator` [GitHub repo](https://github.com/pseudogene/contiguator/).

### What is STACKS?

[CONTIGuator](http://contiguator.sourceforge.net/) is a bacterial genomes finishing tool for structural insights on draft genomes. CONTIGuator is developed by [Florence computational biology group](http://www.unifi.it/dbefcb/).

> http://contiguator.sourceforge.net/
> 
> https://github.com/combogenomics/CONTIGuator

### How to use this image.

For CONTIGuator run through the command line interface (CLI) allowing the deployment on Cloud, Cluster and docker Swamp.

By default the path is `/data`, to import and export the result of your analyse you need to link the folder we your data are to the docker `/data` folder by user `-v <USERFOLDER>:/data`.

```
$ docker run -it --rm -v /export:/data pseudogene/contiguator:latest \
       python /usr/local/bin/CONTIGuator.py -c "/data/contig.fasta" -r "/data/reference.fasta" -o "/data/output"
```

### Rebuild it yourself

```
git clone https://github.com/pseudogene/contiguators.git
cd contiguator
docker build --rm=true -t contiguator:latest -t contiguator:2.7.5 .
cd ..
```

### Colophon

Please see the [Docker](https://docs.docker.com/engine/installation/) installation documentation for details on how to upgrade your Docker daemon.

#### User Feedback Documentation

Be sure to familiarise yourself with the repository's [README.md](https://github.com/pseudogene/contiguator/blob/master/README.md) file before attempting a pull request.

#### Issues

If you have any problems with or questions about this docker image, please contact us through a [GitHub issue](https://github.com/pseudogene/contiguator/issues).
Any issue related to CONTIGuator itself must be done directly with [CONTIGuator developers](http://contiguator.sourceforge.net/) or via the [CONTIGuator-user mailing list](https://groups.google.com/forum/?fromgroups#!forum/contiguator).


#### Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/pseudogene/contiguator/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
