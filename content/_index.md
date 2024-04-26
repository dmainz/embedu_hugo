+++
archetype = "home"
title = "Home"
description = "Description"
+++


Welcome to EmbeddedUniversity!

> :bulb: **Tip:** This is a light bulb.

```math { align="left" }
$$f(x) = \int_{0}^{\infty}e^{2 \pi i x}dx$$
```
| Dockerfile |
| ---------------------- |
```
FROM alpine
RUN apk update
RUN apk add --no-cache --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community hugo
RUN apk add git
EXPOSE 1313
WORKDIR /home/data
ENV HUGO_BIND=0.0.0.0 HUGO_DESTINATION=public HUGO_ENV=DEV HUGO_EDITION=extended HUGO_CACHEDIR=/tmp
ENTRYPOINT [ "hugo" ]
```

