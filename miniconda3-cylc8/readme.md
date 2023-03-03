Purpose
to use conda environment for Cylc
/app/requirement.txt include a list of libraires for your development

Dockerfile

```
FROM docker.io/conda/miniconda3

WORKDIR /app

COPY ./app/requirements.txt /app

VOLUME ./app

```

```bash
# Build image
docker build -t miniconda3 .

#Run the container
docker run -it miniconda3

```

```bash
# container stop
docker stop container-id

# container remove
docker rm container-id

# image remove
docker rmi miniconda3
```
