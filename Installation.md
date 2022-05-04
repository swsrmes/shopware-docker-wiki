## Requirements:
- Linux or Windows. macOS is currently not supported due [VirtioFS issue](https://github.com/docker/for-mac/issues/6243)
- Docker
- Docker Compose (Follow https://docs.docker.com/compose/install/ to install an updated version)
- The Linux User UID is `1000`. (Run `id -u` to check)
- The Linux user needs to be in the docker group
    - Command: `sudo usermod -aG docker $USER`
    - Logout and Login again
- Following packages were installed: `dialog` and `jq`
    - Ubuntu/Debian: `sudo apt install dialog jq`
    - Arch: `sudo pacman -S dialog jq`

## Linux Install

- Clone the shopware-docker repository to your local machine:
    - `git clone https://github.com/shyim/shopware-docker.git ~/Documents/shopware-docker`
- Create a symlink to your PATH `sudo ln -s /home/$USER/Documents/shopware-docker/bin/swdc /usr/local/bin/swdc`
- Optional on Bash: Add the following to your `~/.bashrc` to have autocompletion:
    - `source ~/Documents/shopware-docker/completion.sh`
- Start the containers `swdc up`

# Windows Install

See [Guide](https://shyim.me/blog/shopware-development-environment-windows/)
