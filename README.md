# docker 

## Setup
https://docs.docker.com/desktop/windows/install/

## dockerfile
A Dockerfile is simply a text-based script of instructions that is used to create a container image

Refer the repository 
https://github.com/ag143/docker-getting-started/tree/master/app

### sample docker file
https://github.com/ag143/docker-getting-started/blob/master/app/dockerfile



> docker build -t getting-started .

# Start an app container
docker run -dp 3000:3000 getting-started

After a few seconds, open your web browser to http://localhost:3000. You should see our app

# how to write dockerfile
https://docs.docker.com/engine/reference/builder/#usage

<<<<<<< HEAD
https://docs.docker.com/language/nodejs/build-images/
=======
> Instructions
<pre>
ADD
COPY
ENV
EXPOSE
FROM
LABEL
STOPSIGNAL
USER
VOLUME
WORKDIR
ONBUILD (when combined with one of the supported instructions above)

above instructions supports environment variables

ENV abc=hello
ENV abc=bye def=$abc
ENV ghi=$abc

The FROM instruction initializes a new build stage and sets the Base Image for subsequent instructions.

##### how org works


ARG  CODE_VERSION=latest
FROM base:${CODE_VERSION}
CMD  /code/run-app

ARG VERSION=latest
FROM busybox:$VERSION
ARG VERSION
RUN echo $VERSION > image_version



RUN
RUN has 2 forms:

RUN <command> (shell form, the command is run in a shell, which by default is /bin/sh -c on Linux or cmd /S /C on Windows)
RUN ["executable", "param1", "param2"] (exec form)
The RUN instruction will execute any commands in a new layer on top of the current image and commit the results.


RUN /bin/bash -c 'source $HOME/.bashrc; \
echo $HOME'

RUN /bin/bash -c 'source $HOME/.bashrc; echo $HOME'

RUN ["/bin/bash", "-c", "echo hello"]



The CMD instruction has three forms:

CMD ["executable","param1","param2"] (exec form, this is the preferred form)
CMD ["param1","param2"] (as default parameters to ENTRYPOINT)
CMD command param1 param2 (shell form)
There can only be one CMD instruction in a Dockerfile. If you list more than one CMD then only the last CMD will take effect.

The main purpose of a CMD is to provide defaults for an executing container. These defaults can include an executable, or they can omit the executable, in which case you must specify an ENTRYPOINT instruction as well.

LABEL
LABEL <key>=<value> <key>=<value> <key>=<value> ...
The LABEL instruction adds metadata to an image. A LABEL is a key-value pair. 

EXPOSE
EXPOSE <port> [<port>/<protocol>...]
The EXPOSE instruction informs Docker that the container listens on the specified network ports at runtime. You can specify whether the port listens on TCP or UDP, and the default is TCP if the protocol is not specified.


To expose on both TCP and UDP, include two lines:

EXPOSE 80/tcp
EXPOSE 80/udp

The ADD instruction copies new files, directories or remote file URLs from <src> and adds them to the filesystem of the image at the path <dest>.

COPY
COPY has two forms:

COPY [--chown=<user>:<group>] <src>... <dest>
COPY [--chown=<user>:<group>] ["<src>",... "<dest>"]


ENTRYPOINT
ENTRYPOINT has two forms:

The exec form, which is the preferred form:

ENTRYPOINT ["executable", "param1", "param2"]
The shell form:

ENTRYPOINT command param1 param2
An ENTRYPOINT allows you to configure a container that will run as an executable.

For example, the following starts nginx with its default content, listening on port 80:

 docker run -i -t --rm -p 80:80 nginx
 
 FROM ubuntu
ENTRYPOINT ["top", "-b"]
CMD ["-c"]

>>>>>>> 28487656f177838646606c7cccd21a6960d21f31

https://docs.docker.com/language/python/build-images/

<<<<<<< HEAD
https://docs.docker.com/language/java/build-images/

https://docs.docker.com/language/golang/build-images/
=======
 </pre>
>>>>>>> 28487656f177838646606c7cccd21a6960d21f31





## References

- https://github.com/marketplace/actions/build-and-push-docker-images
- https://linuxhit.com/how-to-create-docker-images-with-github-actions/
- https://stackoverflow.com/questions/68500021/build-image-and-push-to-docker-hub-using-github-action
- https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#scheduled-events
- https://github.com/marketplace/actions/build-and-push-docker-images
- https://medium.com/platformer-blog/lets-publish-a-docker-image-to-docker-hub-using-a-github-action-f0b17e5cceb3
- https://faun.pub/how-to-push-docker-image-using-github-actions-694397c4f557
- https://www.prestonlamb.com/blog/creating-a-docker-image-with-github-actions
- https://docs.docker.com/ci-cd/github-actions/
- https://event-driven.io/en/how_to_buid_and_push_docker_image_with_github_actions/
- https://github.com/marketplace/actions/build-and-push-docker-images
