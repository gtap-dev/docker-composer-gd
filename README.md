Similar to the [Official Composer image](https://hub.docker.com/_/composer), but with the PHP `gd` extension installed.

[DockerHub page](https://hub.docker.com/r/gotoandplay/composer-gd)

To build an image:

* `cd 2.0.13-php7.4`
* `docker build . -t gotoandplay/composer-gd:2.0.13-php7.4`

To run a command on the image:

* `docker run --rm gotoandplay/composer-gd:2.0.13-php7.4 composer -V`

To test install in a local dir:

* `docker run --rm -v full-path-to-local-dir:/test -w /test gotoandplay/composer-gd:2.0.13-php7.4 composer install`

To push the built image to DockerHub:

* `docker push gotoandplay/composer-gd:2.0.13-php7.4`
