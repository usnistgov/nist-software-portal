# NIST Software Portal

Author: ODI

Welcome to the National Institute of Standards and Technology software portal! The purpose of this software portal is to serve as a hub for open source software that is produced by Lawrence Livermore National Laboratory.

NIST produces software on a daily basis. Some of this software is used only internally, other components are licensed for use by external partners and collaborators, still other software is released, or even actively developed, in the open on software hosting platforms such as GitHub.com, Bitbucket.org, Sourceforge.net, and others.

## Prerequisites

Before you begin, make sure you have working installs of Git, Ruby, and Bundler <https://bundler.io/> You will need these tools for development.

## Getting Started

To work locally, first clone into the repository:

```
git clone https://github.com/usnistgov/software.git
```

Make sure you are in the directory you just created by running `cd software` Then you can use `docker` to build the containers (see the [Docker installation docs](https://docs.docker.com/) for step-by-step guides to setting this up):

```
docker-compose build
```

Running this will install everything in your Gemfile (including Jekyll) in your container. Finally, run the development web server with:

```
docker-compose up
```

Followed by opening <http://localhost:3000> in a web browser.

## Contact

If you have any questions or would like to request a private repository, please don't hesitate to contact [Ian Lee](mailto:devops@nist.gov).

# Release

The code of this site is released under the MIT License. For more details see the
[LICENSE](LICENSE) File.
