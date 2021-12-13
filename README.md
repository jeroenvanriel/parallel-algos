## Docker image

Based on `pyspark-notebook` from [Jupyter Docker Stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/), also see [options for PySpark](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/specifics.html#specific-docker-image-options).

Build and tag the image using
`docker build --rm -t jupyter/my-pyspark-notebook .`

Then run it using
`docker run -p 8888:8888 -p 4040:4040 -v "$PWD":/home/jovyan/work jupyter/my-pyspark-notebook

## Helpful resources

- https://sparkbyexamples.com/pyspark-rdd/
- https://github.com/spark-examples/pyspark-examples/

