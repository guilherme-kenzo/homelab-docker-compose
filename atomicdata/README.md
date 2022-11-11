# Atomic Data

Directly from the [projects docs](https://docs.atomicdata.dev/atomic-data-overview.html): 

> Atomic Data is a modular specification for sharing, modifying and modeling graph data. It combines the ease of use of JSON, the connectivity of RDF (linked data) and the reliability of type-safety.

For my pratical uses it consists of a data server with flexible schemas and interesting APIs and a [notion-like](https://notion.so/) web client. The project is in its early days, but it seems to be promissing.

The server must be built from scratch and the dockerfile is pulled directly from the projects repo - which is a submodule in this repository. It takes a while on a slow machine. Grab a coffee and wait. 

Run this service through the `run_compose.sh` script (at least when first building the image), which ensures that the DOCKER_BUILDKIT=1 and COMPOSE_DOCKER_CLI_BUILD=1 flags are set.

## To future me

This is still a work in progress. I had some trouble finding the configuration/env options and files, but found that running `./atomic-server-bin setup-env` inside the the atomicserver container generates a helpful sample env file. However, I could not get the web interface to work - index just gave me an authentication error.

## TO DO

- [ ] Check if there are any related bugs in the projects github.
