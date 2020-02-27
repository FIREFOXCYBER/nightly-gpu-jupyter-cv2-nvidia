docker run -it \
--env=LOCAL_USER_ID="\$(id -u)" \
-v ~/ex:/ex:rw \
-v /tmp/.X11-unix:/tmp/.X11-unix:ro \
-e DISPLAY=:0 \
-p 8888:8888/udp \
--env="QT_X11_NO_MITSHM=1" \
--gpus all \
--name={Name} {ImageID}
