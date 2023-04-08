

## Setup

```sh

# build
docker build . -t newproject

# run container
docker run -it -v $(pwd):/code -p 8888:8888 newproject bash
# note: -p 8888:8888 maps port 8888 to your host machine and is needed for jupyter notebooks
# note: -v $(pwd):/code mounts your current working directory (presumably your project directory) and makes any changes instantly available in the running container

# run the second command, for example, if you want to start a jupyter notebook:
jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
```


