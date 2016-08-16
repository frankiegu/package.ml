# Jupyter Notebook; Anaconda3 4.1.1

To build:

```
docker build -t fluxcapacitor/utils-jupyter-notebook:4.1.1 .
```

To run on a local port (and have the container run in the background, detached), use the following command:

```shell
docker run -d -p <desired-port-here>:8888 fluxcapacitor/utils-jupyter-notebook:4.1.1
```

If you'd like to have the Jupyter Notebook's external port be determined automatically, you can exclude passing `<desired-port-here>`. Then you can look up the notebook's port with `docker port`:

```shell
docker run --name my-notebook -d -p 8888 fluxcapacitor/utils-jupyter-notebook:4.1.1

docker port my-notebook
8888/tcp -> 0.0.0.0:32768   # 32768 is the port in this case
```
