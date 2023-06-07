# blockchain.info wallet service

This Image contains the wallet service for blockchain.info

## Parent image

- node:latest

## Dependencies

None

## Entrypoint & CMD

```
blockchain-wallet-service start --bind 0.0.0.0 --port 3000
```

## Functions

Hosts local API Service for blockchain.info

## Build Image

### Automated Build

Through the new build pipeline all of our Docker images are built via Gitlab CI/CD and pushed to the Gitlab Container Registry. You usually don't need to build the image on your own, just push your commits to the git. The Image will be tagged after your branch name.

After the automated build is finished you can pull the image:

```
docker pull registry.gitlab.com/pazdzewicz_docker/blockchain-wallet-service:BRANCH
```

All images also have a master tag, just replace the BRANCH with "master". The "latest" Tag is only an alias for the "master" tag.

### Manual Build

You can also build the Docker image on your local pc:

```
docker build -t "myblockchain-wallet-service:latest" .
```

### Build Options

Build Options are Arguments in the Dockerfile (`--build-arg`):

- None

### Security Check during Build

Before we release Docker Containers into the wild it is required to run the Anchore security checks over the Pipeline (this doesn't apply to manual built images). You can download the current artifacts on the Pipelines page (the download drop-down).

## Ports

- 3000

## Usage

### Generic Usage