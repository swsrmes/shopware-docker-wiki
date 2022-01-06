Here is a quick guide to Setup PhpStorm Docker Support

- Go to **Settings** -> **PHP**
- Edit **CLI Interpreter**
- Add a new Interpreter with +
- Choose Docker and then Docker-Compose
- Configure it
    - The configuration file is `/tmp/swdc-docker-compose.yml`
    - Choose as service `cli`
    - Add to environment variables `COMPOSE_PROJECT_NAME=shopware-docker`
- Save it

Now set the new interpeter as default for this repository and anything should work like local development
