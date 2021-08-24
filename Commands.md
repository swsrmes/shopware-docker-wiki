The commands in SWDC are separated by modules. The modules define the context of the given project. 

Most commands are used in the following way `swdc command project`, swdc tries to detect the given project type and scopes to the corresponding modules. 

Like when the target project is Shopware 5 Git installation, to include base + classic or on Shopware 6, base + platform. 


### Module: base - Always available commands

| Command                                  | Description                                                       |
| ---------------------------------------- | ----------------------------------------------------------------- |
| swdc up                                  | Starts the containers                                             |
| swdc down                                | Stops the containers                                              |
| swdc configure                           | Opens the swdc configuration file                                 |
| swdc help                                |                                                                   |
| swdc create-project <project>            | Creates a new Shopware 6 Installation                             |
| swdc log <project>                       | Shows the log of the specified container                          |
| swdc console <project> <symfony-command> | Executes the symfony console for the given project                |
| swdc debug-logs                          | Please use this command to collect information for a GitHub Issue |
| swdc drop <name>                         | Drops the database                                                |
| swdc es-clear                            | Deletes everything from Elasticsearch server                      |
| swdc mysql                               | Starts the mysql client on the cli container                      |
| swdc mysql-watch                         | Watches the mysql process list                                    |
| swdc open <project>                      | Opens the given shop in browser                                   |
| swdc snap <project> [name]               | Creates a new database snapshot                                   |
| swdc rsnap <project> [name]              | Loads back a created database snapshot                            |
| swdc redis-clear                         | Clears all redis databases                                        |
| swdc shell-root                          | Joins into the CLI container as root user                         |
| swdc shell --php-version 80 | Joins into the CLI container as normal user                     |
| swdc update-images                       | Updates used docker images                                        |

### Module: classic - Shopware 5

| Command                            | Description                                                                  |
| ---------------------------------- | ---------------------------------------------------------------------------- |
| swdc apply <project>               | Applies a database fixture                                                   |
| swdc build <project>               | Reinstalls the database                                                      |
| --without-demo-data                | As optional parameter to start without demo-data                             |
| --without-config-patch             | As optional parameter to specify not patching the config with error-handling |
| --mysql-host                       | As optional parameter to specify mysql-host                                  |
| swdc config <project> <config>     | Applies fixture to the config.php                                            |
| swdc download-testimages <project> | Download and extract shopware testimages                                     |
| swdc hooks <project>               | Fixes the hooks for git                                                      |
| swdc mink <project>                |                                                                              |
| swdc snippets <project>            | Reimports all snippets                                                       |
| swdc test <project>                | Runs all tests                                                               |
| swdc unit <project>                | Runs only unit tests                                                         |
| swdc update-test <project>         | Simulate an update                                                           |

### Module: platform - Shopware 6

| Command                         | Description                                                         |
| ------------------------------- | ------------------------------------------------------------------- |
| swdc admin-build <project>      | Builds the administration and executes assets install               |
| swdc admin-init <project>       | Installs required npm modules                                       |
| swdc admin-jest <project>       |                                                                     |
| swdc admin-watch <project>      | Start the admin watcher at port 8181                                |
| swdc build <project>            | Reinstalls the database                                             |
| --without-demo-data             | As optional parameter to start without demo-data                    |
| --without-building              | As optional parameter to start without built JS                     |
| --mysql-host                    | As optional parameter to specify mysql-host                         |
| swdc check <project>            | Checks code for contribution issues                                 |
| swdc storefront-build <project> | Builds the storefront                                               |
| swdc storefront-init <project>  | Installs required npm modules                                       |
| swdc storefront-watch <project> | Recompile the storefront when changes in its resources are detected |
| swdc test <project>             | Runs all unit tests                                                 |
| swdc worker <project>           | Run the worker                                                      |
| swdc e2e <project>              |                                                                     |
| swdc init-test-db <project>     | Initializes the test database                                       |
