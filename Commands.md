The commands in SWDC are separated by modules. The modules define the context of the given project. 

Most commands are used in the following way `swdc command project`, swdc tries to detect the given project type and scopes to the corresponding modules. 

Like when the target project is Shopware 5 Git installation, to include base + classic or on Shopware 6, base + platform. 


### Module: base

| Command                                  | Description                                                       |
| ---------------------------------------- | ----------------------------------------------------------------- |
| `swdc command-list` |  | 
| `swdc completion` |  | 
| `swdc configure` | Opens the configuration .env file with your favourite editor | 
| `swdc console` | Executes the symfony console for the given project | 
| `swdc create-project` | Creates a new Shopware 6 Installation | 
| `swdc debug-logs` | Please use this command to collect informations for a Github Issue | 
| `swdc down` | Stops the containers | 
| `swdc drop` | Drops the database | 
| `swdc es-clear` | Deletes everything from elasticsearch server | 
| `swdc generate-command-list` | Generates the command list for README.md | 
| `swdc help` | Lists all commands | 
| `swdc log` | Shows the log of the specified container | 
| `swdc mysql-exec-watch` | Executes a every second MySQL command and shows the result | 
| `swdc mysql-watch` | Watches the mysql process list | 
| `swdc mysql` | Starts the mysql client on the cli container | 
| `swdc open` | Opens the given shop in browser | 
| `swdc pshell` | Opens a shell in the specific project | 
| `swdc redis-clear` | Clears all redis databases | 
| `swdc redis-cli` | Opens the Redis-CLI | 
| `swdc rsnap` | Loads back a created snapshot | 
| `swdc shell-root` | Joins into the cli container as root user | 
| `swdc shell` | Joins into the cli container as normal user | 
| `swdc snap` | Creates a new snapshot | 
| `swdc tool-cache-clear` | Clears the tool cache | 
| `swdc up` | Starts the containers | 
| `swdc update-images` | Updates used docker images | 
| `swdc varnish-clear` | Bans all varnish cache | 
### Module: classic

| Command                                  | Description                                                       |
| ---------------------------------------- | ----------------------------------------------------------------- |
| `swdc apply <project-name>` | Applies a database fixture | 
| `swdc build <project-name>` | Reinstalls the database | 
| `swdc config <project-name>` | Applies fixture to the config.php | 
| `swdc download-testimages <project-name>` | Download and extract shopware testimages | 
| `swdc hooks <project-name>` | Fixes the hooks for git | 
| `swdc mink <project-name>` | Starts the Browser tests | 
| `swdc snippets <project-name>` | Reimports all snippets | 
| `swdc test <project-name>` | Runs all tests | 
| `swdc unit <project-name>` | Runs only unit tests | 
| `swdc update-test <project-name>` | Simulate a update | 
### Module: platform

| Command                                  | Description                                                       |
| ---------------------------------------- | ----------------------------------------------------------------- |
| `swdc admin-build <project-name>` | Builds the administration and executes assets install | 
| `swdc admin-init <project-name>` | Installs required npm modules | 
| `swdc admin-jest <project-name>` | Runs the Jest tests | 
| `swdc admin-watch <project-name>` | Start the admin watcher at admin-<project>.dev.localhost | 
| `swdc build-with-old-demo-data <project-name>` | Builds Shopware 6 with Shopware 5 Demo-Data. Requires min 6.3.5.0 | 
| `swdc build <project-name>` | Reinstalls the database | 
| `swdc check <project-name>` | Checks code for ci issues | 
| `swdc config-add <project-name>` | Adds a config to config/packages | 
| `swdc config-remove <project-name>` | Removes a config from config/packages | 
| `swdc config-set <project-name>` | Sets a config for config/packages | 
| `swdc queue-clear <project-name>` | Clears the enqueue queue in Shopware 6 | 
| `swdc run <project-name>` | Runs specified command in CLI. f.e. swdc run myfolder npm install --prefix custom/plugins/MyPlugin/src/Resources | 
| `swdc storefront-build <project-name>` | Builds the storefront | 
| `swdc storefront-init <project-name>` | Installs required npm modules | 
| `swdc storefront-watch <project-name>` | Recompile the storefront when changes in its resources are detected | 
| `swdc test <project-name>` | Runs all unit tests | 
| `swdc update <project-name>` | Updates Shopware 6 | 
| `swdc worker-logs <project-name>` | Tail the logs of the workers | 
| `swdc worker <project-name>` | Run the worker | 
| `swdc admin-watch <project-name>` | Start the admin watcher at admin-<project>.dev.localhost | 
| `swdc e2e <project-name>` | Starts the Cypress instance. Use "Storefront" as parameter when you want open that package | 
| `swdc feature <project-name>` | Creates a file to enable Feature flags | 
| `swdc init-test-db <project-name>` | Initializes the test database | 
| `swdc locust <project-name>` | Starts the locust service | 
| `swdc npm-remove <project-name>` | Deletes all node_modules folders | 
| `swdc storefront-hot <project-name>` | Starts the Storefront Watcher | 
| `swdc storefront-watch <project-name>` | Start the storefront watcher at storefront-<project>.dev.localhost | 
| `swdc test <project-name>` | Run the test suite | 
| `swdc update <project-name>` | Updates Shopware 6 | 

### Module: platform-b2b

| Command                                  | Description                                                       |
| ---------------------------------------- | ----------------------------------------------------------------- |
| `swdc b2b-add-migration <project-name>` |  | 
| `swdc b2b-init <project-name>` |  | 
| `swdc b2b-storefront-build <project-name>` |  | 
