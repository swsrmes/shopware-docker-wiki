### Module: base

* `swdc command-list`
* `swdc console`                   Executes the symfony console for the given project
* `swdc create-project`            Creates a new Shopware 6 Installation
* `swdc debug-logs`                Please use this command to collect informations for a Github Issue
* `swdc down`                      Stops the containers
* `swdc drop`                      Drops the database
* `swdc es-clear`                  Deletes everything from elasticsearch server
* `swdc generate-command-list`     Generates the command list for README.md
* `swdc help`
* `swdc log`                       Shows the log of the specified container
* `swdc mysql`                     Starts the mysql client on the cli container
* `swdc mysql-watch`               Watches the mysql process list
* `swdc open`                      Opens the given shop in browser
* `swdc rsnap`                     Loads back a created snapshot
* `swdc shell-root`                Joins into the cli container as root user
* `swdc shell`                     Joins into the cli container as normal user
* `swdc snap`                      Creates a new snapshot
* `swdc update-images`             Updates used docker images
* `swdc up`                        Starts the containers

### Module: classic

* `swdc apply`                     Applies a database fixture
* `swdc build`                     Reinstalls the database
* `swdc config`                    Applies fixture to the config.php
* `swdc download-testimages`       Download and extract shopware testimages
* `swdc hooks`                     Fixes the hooks for git
* `swdc mink`
* `swdc snippets`                  Reimports all snippets
* `swdc test`                      Runs all tests
* `swdc unit`                      Runs only unit tests
* `swdc update-test`               Simulate a update

### Module: classic-composer

* `swdc build`                     Reinstalls the database

### Module: defaults

* `swdc base-up`

### Module: local

* `swdc configure`                 Opens the configuration .env file with your favourite editor

### Module: platform

* `swdc admin-build`               Builds the administration and executes assets install
* `swdc admin-init`                Installs required npm modules
* `swdc admin-jest`
* `swdc admin-watch`               Start the admin watcher at port 8181
* `swdc build`                     Reinstalls the database
* `swdc check`                     Checks code for ci issues
* `swdc storefront-build`          Builds the storefront
* `swdc storefront-init`           Installs required npm modules
* `swdc storefront-watch`          Recompile the storefront when changes in its resources are detected
* `swdc test`                      Runs all unit tests
* `swdc worker`                    Run the worker

### Module: platform-local

* `swdc e2e`
* `swdc init-test-db`              Initializes the test database
* `swdc storefront-hot`            Starts the Storefront Watcher
* `swdc test`                      Run the test suite

### Module: platform-prod

* `swdc build`