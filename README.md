Alpine GNU C library (glibc) Docker image
=========================================

This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make [glibc](https://www.gnu.org/software/libc/) work side by
side with musl libc (default in Apline Linux). glibc packages for Alpine Linux are prepared by
[Andy Shinn](https://github.com/andyshinn) and the releases are published in
[andyshinn/alpine-pkg-glibc](https://github.com/andyshinn/alpine-pkg-glibc) github repo.

Usage Example
-------------

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM cosmomill/alpine-glibc

COPY ./my_app /usr/local/bin/my_app
```

```sh
$ docker build -t my_app .
```
