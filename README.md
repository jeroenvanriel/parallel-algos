## Docker image

Based on `pyspark-notebook` from [Jupyter Docker Stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/), also see [options for PySpark](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/specifics.html#specific-docker-image-options).

Build and tag the image using
`docker build --rm -t jupyter/my-pyspark-notebook .`

Then run it using
`docker run -p 8888:8888 -p 4040:4040 -v "$PWD":/home/jovyan/work jupyter/my-pyspark-notebook

The [Web UI](https://spark.apache.org/docs/3.0.0-preview/web-ui.html) is running on port 4040 by default, but each new spark context that is created is put onto an incrementing port. Therefore, it may be helpful to map some more ports from the start by using `-p 4040-4050:4040-4050` when starting the container.

## Helpful resources

- https://sparkbyexamples.com/pyspark-rdd/
- https://github.com/spark-examples/pyspark-examples/
- https://spark.apache.org/docs/latest/rdd-programming-guide.html

