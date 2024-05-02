---
title: "First Content"
date: 2024-04-21T17:04:41Z
draft: false
---

> :bulb: **Tip:** This is a light bulb.

```math { align="left" }
$$f(x) = \int_{0}^{\infty}e^{2 \pi i x}dx$$
```

```docker {title="Dockerfile"}
FROM alpine
RUN apk update
RUN apk add --no-cache --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community hugo
RUN apk add git
EXPOSE 1313
WORKDIR /home/data
ENV HUGO_BIND=0.0.0.0 HUGO_DESTINATION=public HUGO_ENV=DEV HUGO_EDITION=extended HUGO_CACHEDIR=/tmp
ENTRYPOINT [ "hugo" ]
```

```bash {title="Run the container"}
docker run --rm -p 1313:1313 -v $(pwd):/home/data hugo server -D --gc --bind=0.0.0.0
```

Example TeX
```math { align="left" }
\[
\begin{aligned}
KL(\hat{y} || y) &= \sum_{c=1}^{M}\hat{y}_c \log{\frac{\hat{y}_c}{y_c}} \\
JS(\hat{y} || y) &= \frac{1}{2}(KL(y||\frac{y+\hat{y}}{2}) + KL(\hat{y}||\frac{y+\hat{y}}{2}))
\end{aligned}
\]
```
