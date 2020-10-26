<a href="https://hub.docker.com/r/codercom/enterprise-base">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-base?label=codercom%2Fenterprise-base)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-multieditor">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-multieditor?label=codercom%2Fenterprise-multieditor)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-webstorm">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-webstorm?label=codercom%2Fenterprise-webstorm)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-vnc">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-vnc?label=codercom%2Fenterprise-vnc)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-pycharm">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-pycharm?label=codercom%2Fenterprise-pycharm)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-node">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-node?label=codercom%2Fenterprise-node)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-jupyter">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-jupyter?label=codercom%2Fenterprise-jupyter)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-java">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-java?label=codercom%2Fenterprise-java)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-intellij">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-intellij?label=codercom%2Fenterprise-intellij)</a>
<a href="https://hub.docker.com/r/codercom/enterprise-goland">![Docker Pulls](https://img.shields.io/docker/pulls/codercom/enterprise-goland?label=codercom%2Fenterprise-goland)</a>

# Enterprise Example Images

These docs contain examples and guides for how to setup your images to utilize
the Multi Editor Support built into Coder Enterprise.

Each directory in [`images/`](./images) contains examples for how to setup your images
with different IDEs.

See our [documentation at our Enterprise Hub](https://enterprise.coder.com/docs/multi-editor) for additional information
about supported editors and known issues.

## Image Minimums

All of the images provided in this repo include the following utilities to ensure they work well
with all of Coder Enterprise's features, and to provide a solid out-of-the-box developer experience:

* git
* bash
* curl & wget
* htop
* man
* vim
* sudo
* python3 & pip3
* gcc & gcc-c++ & make

## Images on Docker Hub

Each of these images is also published to Docker Hub under the `codercom/enterprise-[name]`
repository. For example, `intellij` is available at https://hub.docker.com/r/codercom/enterprise-intellij.
The tag is taken from the file extension of the Dockerfile. For example, `intellij/Dockerfile.ubuntu`
is under the `ubuntu` tag.

## Adding a New Image

To add a new image, create a new folder in `images/` with the name of the image, and create
at least one `Dockerfile` for it, using an extension as the tag. For instance, an Ubuntu-based
version of your image would be in `Dockerfile.ubuntu`.

New images should extend from existing images whenever possible, e.g.
```Dockerfile
FROM codercom/enterprise-base:ubuntu

# Rest of your image...
```
