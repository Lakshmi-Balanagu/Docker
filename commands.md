1. To start a new container with a different command:
       $docker run <options> <image_name> <new_command>
2.The docker history command is used to show the history of an image, including the layers that make up the image, and details about each layer.
  This can be useful to understand how an image was built, what commands were executed during its creation, and how much disk space each layer consumes.
      $docker history <image_name>
      IMAGE ID: The unique identifier for each layer of the image.
      CREATED: The time when each layer was created.
      CREATED BY: The command that was run to create that layer.
      SIZE: The size of each layer.
      COMMENT: Any additional comments related to the layer, if available (often blank).
3.To copy a file from the host machine to a running container, you can use the docker cp command.
  This command allows you to copy files and directories between the host and a container, or vice versa.
      $docker cp <source_path> <container_name_or_id>:<destination_path>
4.The docker exec command is commonly used to start an interactive shell inside a running container using bash or /bin/bash. This allows you to make changes, edit files, install packages, etc.
      $docker exec -it <container_name_or_id> /bin/bash
5.To create a new Docker image from a running or stopped container, you can use the docker commit command. This command takes the current state of a container and saves it as a new image. The image will include all changes made to the container's filesystem since it was started.
      $docker commit <container_name_or_id> <new_image_name>:<tag>
