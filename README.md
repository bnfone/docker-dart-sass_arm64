## docker-dart-sass_arm64

sass/dart-sass docker image for web development purposes on **arm64 architecture** *(like Apple Silicon)*. Runs sass --watch on provided volumes.

# How to use this image
To use this image in web development run this docker command:
```
docker run -v $PWD/sass:/sass/ -v $PWD/css:/css/ -it bnfone/docker-dart-sass:latest
```
Assuming we have ./sass folder with source files and ./css folder with desired generated CSS files.

Expected output:
```
Compiled sass/main.sass to css/main.css.
Sass is watching for changes. Press Ctrl-C to stop.
```

In our project main folder we can then run some other image to server our web. For example the https://hub.docker.com/r/jekyll/jekyll/.

# Building

```sh
docker build -t dart-sass:arm64 . --no-cache --platform linux/arm64
```


This image is based on debian:buster-slim.

Command run by the image:
```
/opt/dart-sass/sass --watch /sass:/css
```

---

### Credits

Credit to [Michal Klempa](https://github.com/michalklempa) for his [docker-dart-sass](https://github.com/michalklempa/docker-dart-sass) Repo.

