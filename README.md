## Docker image

Build and tag the image using
`docker build --rm -t jupyter/my-pyspark-notebook .`

Then run it using
`docker run -p 8888:8888 -p 4040:4040 -v "$PWD":/home/jovyan/work jupyter/my-pyspark-notebook

