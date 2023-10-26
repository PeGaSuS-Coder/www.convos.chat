---
title: Convos loves Docker
author: Jan Henning Thorsen
---

We now have an official [Docker](https://github.com/convos-chat/convos/pkgs/container/convos)
file for Convos! The image is based on [Alpine 3.5](https://alpinelinux.org/),
making it very small and easy to install. You can get up and running with
these commands:

    # Build
    docker build --no-cache --rm -t convos-chat/convos .
    # Run
    docker run -it --rm -p 8080:3000 -v /var/convos/data:/data convos-chat/convos

<!--more-->

`8080` is the port where you want Convos to be exposed and `/var/convos/data`
is where you want to store settings and logs on the host machine.

We have plans for other ways to install/run Convos. Have a look at issue
[#285](https://github.com/convos-chat/convos/issues/285) for more details. We
welcome any help and input on making official Convos packages and easy
"install buttons".
