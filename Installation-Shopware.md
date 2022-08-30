## Using existing project

- Create a new folder in `~/Code/` with your project name and checkout the code
- Run `swdc up` to create the app container for the new shop
- Run `swdc build [project-name]` to build the project
- Run `swdc open [project-name]` to open the Shop in browser

### Configure a custom docker build process

Swdc currently supports a custom [Dockerfile](https://docs.docker.com/engine/reference/builder/) build process, but only within the app container of a given project.

Ensuring your swdc install is currently in a `down` state (all containers are currently not running), you can now start your Dockerfile build. 

Here we will follow a tutorial for custom WSL xdebug configuration with the `nginx:php74-xdebug` app container:

1. `cd ~/Code/[project_directory]`
2. `mkdir .swdc`
3. `nano .swdc/Dockerfile`
4. Copy this [xdebug config](reference/WSL/xdebug.ini) to `.swdc/xdebug.ini`. You can use `curl -sSL [file_raw_url] > .swdc/Dockerfile`
5. Copy [this Dockerfile](reference/WSL/Dockerfile) to `.swdc/Dockerfile`: `curl -sSL [file_raw_url] > .swdc/Dockerfile`
6. Run `swdc up`. You will see your custom build commands run within the output of the `up` command

**N.B:** You can configure your Dockerfile how you like, but make sure to always specify the `FROM [image_name]` clause at the top of the Dockerfile. You can find this image name with `docker ps -a` (shows all pulled containers)

## Create new project

- Run `swdc create-project [project-name]`
- Choose Shopware Template + Version
- Run `swdc open [project-name]` to open the Shop in browser
