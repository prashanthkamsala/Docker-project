### first learn the python ecosystem on Docker

❯ cd /Desktop/vishwasdemo1/docker/fast-api

❯ sh docker_build.sh

### now to learn about the jupterlab ecosystem lets 


❯ cd ..
❯ cd jupyterlab
❯ ls
Dockerfile       docker_build.sh  requirements.txt
❯ sh docker_build.sh


### run docker compose

❯ sh run_compose.sh


### fast API deployed Models

http://0.0.0.0:8000/predict_salary/?employee_age=28



docker run -it -p 8080:8888 -v $PWD:/tmp -w /tmp tensorflow/tensorflow

----------
________                               _______________
___  __/__________________________________  ____/__  /________      __
__  /  _  _ \_  __ \_  ___/  __ \_  ___/_  /_   __  /_  __ \_ | /| / /
_  /   /  __/  / / /(__  )/ /_/ /  /   _  __/   _  / / /_/ /_ |/ |/ /
/_/    \___//_/ /_//____/ \____//_/    /_/      /_/  \____/____/|__/


WARNING: You are running this container as root, which can cause new files in
mounted volumes to be created as the root user on your host machine.

To avoid this, run the container by specifying your user's userid:

$ docker run -u $(id -u):$(id -g) args...


--------

jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
