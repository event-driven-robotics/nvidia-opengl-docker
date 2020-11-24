Adds Nvidia/OpenGL support to other docker builds. 

Requires nvidia-container-toolkit: "https://github.com/NVIDIA/nvidia-docker"

-- USAGE

Build:
docker build \<PATH_TO_DOCKERFILE_DIR\> --build-arg from=\<BASEIMAGE\> -t \<BASEIMAGE\>:opengl

Run:
docker run -v /dev/:/dev --runtime=nvidia -e NVIDIA_DRIVER_CAPABILITIES=graphics \<BASEIMAGE\>:opengl
