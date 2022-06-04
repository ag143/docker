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
