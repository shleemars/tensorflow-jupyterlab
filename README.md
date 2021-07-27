# TensorFlow GPU Jupyterlab

## Building
```shell
docker build -f ./Dockerfile -t tf-gpu-jupyterlab .
```

## Running docker
```shell
docker run --rm --gpus all -p 8888:8888 -v $(realpath ~/notebooks):/notebooks -v $(realpath /datasets):/datasets tf-gpu-jupyterlab
```

## Running with docker-composer
Edit the docker-compose.yml to fit your configuration.

```shell
docker-compose up
```

### Run daemon
```shell
docker-compose up -d
```

### Show logs
```shell
docker-compose logs
```

### Stop daemon
```shell
docker-compose down
```
