# Installation using Docker

It is possible to install Hubzilla comfortably and conveniently as a Docker container.

## Option 1: saiwal/hubzilla-docker

The key features are:

- Fully functional Hubzilla instance with just a few commands.
- Prebuilt images available via dockerhub for amd64, arm/v7, arm64.
- Continuous Updates: The Docker image is built to allow for easy updates whenever new changes are made to the Hubzilla core or its dependencies.
- SMTP Integration: Built-in support for sending emails using ssmtp, making it easy to configure email notifications for your Hubzilla instance.

The repository for the container is located here: [saiwal/hubzilla-docker](https://github.com/saiwal/hubzilla-docker)

### Building the image from scratch

* Clone the Repository:

```bash
git clone https://github.com/skprg/hubzilla-docker.git
cd hubzilla-docker
```

* Configure Your Environment: Update the docker-compose.yml file with your SMTP and other settings.

    Build and Run the Container:

```bash
docker-compose up --build -d
```

### Using prebuilt image

* Replace the following lines in docker-compose.yml
```  
    build:
      context: .
      dockerfile: Dockerfile
```
with
```
    image: ghcr.io/skprg/hubzilla-docker:latest
```
* Run the container:
``` bash
docker compose up -d
```

Access Your Hubzilla Instance: Navigate to http://localhost (or the appropriate URL) to view your Hubzilla instance.

## Option 2: dhitchenor/hubzilla

Another dockjer deployment is provided at <https://github.com/dhitchenor/hubzilla>

Features:
* Automatic setup
* Integral addons, preinstalled
* env file for easy configuration/toggling of features

Instructions and details are available at the [repository](https://github.com/dhitchenor/hubzilla).
