# motion-webcam-server (armv7l/amd64)

use the latest version of motion as a webcam server in a docker container

[motion's offical github](https://github.com/Motion-Project/motion)

## Usage

Edit parameters in **docker-compose.yml**. The current _image_ (**henrikdocker/motion-webcam-server**) was built for _armv7l_, _amd64_ support is in **allenyllee/motion-webcam-server**. Support for other platforms could be built (not tried) using **Dockerfile** as the [Ubuntu docker](https://hub.docker.com/_/ubuntu) image supports _amd64_, _arm32v7_, _arm64v8_, _i386_, _ppc64le_ and _s390x_. 

### Single camera
Copy **conf/motion.conf.dist** to **conf/motion.conf**.

Edit parameters in **conf/motion.conf** to suit your needs. You can disable the **/tmp/motion** redirection under _volumes_ if you are using live streaming only. 

All cameras must be forwarded using the **devices** section, don't remember to mention them in **motion.conf** as well.

### Multiple cameras 
https://motion-project.github.io/motion_config.html#configfiles