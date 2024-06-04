## To build a Docker image using the Dockerfile you've created

    >> docker build --tag <docker_image_name> .
    Ex: docker build --tag python-django .
 

    i) `docker build`: Tells Docker to build a new image.

   ii) `--tag python-django`: Tags the image with the name python-django. This makes it easier to refer to the image later.

  iii) `.`: Specifies the build context, which is the current directory. Docker will look for the Dockerfile in this directory.






## To start a Docker container from the python-django image you built, and it maps a port from the container to your host machine. Here's a breakdown of what each part of the command does:

    >> docker run --publish 8000:8000 <docker_image_name>
    >> docker run --publish 8000:8000 python-django

    i) `docker run`: This command is used to run a container from a Docker image.

    ii) `--publish 8000:8000` or `-p 8000:8000`: This option maps port 8000 on your host machine (the first number) to port 8000 in the container (the second number). This allows you to access services running inside the container on port 8000 from your host machine.

    iii) `python-django`: This is the name of the Docker image you want to run.