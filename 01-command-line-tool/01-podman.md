This file documents the learning about using `podman` command to interact with containers.

# Commands

1. Init machine on Mac

    ``` shell
    podman machine init

    podman machine start podman-machine-default
    ```

2. Pull **Nginx** container image

    ``` shell
    podman pull nginx:latest
    ```

3. Run container

    ``` shell
    # Expose the container port 80 through host port 8080
    podman run          \
    --detach            \
    --name nginx        \
    --publish 8080:80   \
    nginx:latest
    ```

4. Query Nginx from browser

    ``` shell
    localhost:8080
    ```

5. Stop container

    ``` shell
    podman container stop nginx
    ```