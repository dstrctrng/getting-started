---
layout: guide
title: Getting Started
---
# Getting Started

tl;dr getting-started makes your deploys faster and easier.

getting-started project is a common configuration and script library for
access to production and integration environments.  If you access
servers to deploy applications, debug services, run
migrations/tasks, and want your workstation compatible with the ever
changing security, audit, toolchain, configuration that is Operations,
please follow the instructions in this README.

This procedure has been tested on OS X workstations.  Ubuntu workstation
support is coming.

## Cloning the getting-started repo

Initialize getting-started into your $HOME on your workstation.  Do not
clone this project in production/shared environments since its presence enables
autoconf, autoproxy, and autocache capabilities that are not necessary
once you are in production.

    git clone https://github.com/HeSYINUvSBZfxqA/getting-started ~/.getting-started

To receive updates, use the `bin/pancake` script.

    ~/.getting-started/bin/pancake update

## Test deploy

The getting-started project is deployable and is a good indicator your
computer is set up correctly.

Using rvm and ruby ree, deploy getting-started to the master
environment:

    cd ~/.getting-started
    bin/deploy master

You can also run the `hello` task remotely to verify you can run
commands remotely:

    bin/task hello master

## Configuring ssh

Append the contents of ~/.getting-started/ssh/config.example to your
~/.ssh/config to expose the hostname aliases for ssh, scp based commands
(like rsync).

## Generate documentation

This README (and more, soon) is available as a static jekyll site in in
`site/`.  To build it, use the `bin/build` command:

    bin/build site

The static site is generated in `site/_site`.  The start page is in
getting-started project root at `index.html`.  It's meant to be both
hosted on a web server and directly viewable from a folder.

## TODO

Need to cover

 * OS X packages (macports)
 * Ubuntu workstation packages
 * VirtualBox guests (dev1, dev2)
 * ssh and gpg key management
 * private gem repository
