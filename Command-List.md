### Module: base

* `swdc command-list`
* `swdc console`                   Executes the symfony console for the given project
* `swdc create-project`            Creates a new Shopware 6 Installation
* `swdc debug-logs`                Please use this command to collect information for a GitHub Issue
* `swdc down`                      Stops the containers
* `swdc drop`                      Drops the database
* `swdc es-clear`                  Deletes everything from Elasticsearch server
* `swdc generate-command-list`     Generates the command list for README.md
* `swdc help`
* `swdc log`                       Shows the log of the specified container
* `swdc mysql`                     Starts the mysql client on the cli container
* `swdc mysql-watch`               Watches the mysql process list
* `swdc open`                      Opens the given shop in browser
* `swdc rsnap`                     Loads back a created snapshot
* `swdc shell-root`                Joins into the CLI container as root user
* `swdc shell`                     Joins into the CLI container as normal user
  * `--php-version PHPVERSION`     As optional parameter to specify [PHPVERSION](#phpversion)
* `swdc snap`                      Creates a new snapshot
* `swdc update-images`             Updates used docker images
* `swdc up`                        Starts the containers

### Module: classic

* `swdc apply`                     Applies a database fixture
* `swdc build`                     Reinstalls the database
  * `--without-demo-data`          As optional parameter to start without demo-data
  * `--without-config-patch`       As optional parameter to specify not patching the config with error-handling
  * `--mysql-host`                 As optional parameter to specify mysql-host
* `swdc config`                    Applies fixture to the config.php
* `swdc download-testimages`       Download and extract shopware testimages
* `swdc hooks`                     Fixes the hooks for git
* `swdc mink`
* `swdc snippets`                  Reimports all snippets
* `swdc test`                      Runs all tests
* `swdc unit`                      Runs only unit tests
* `swdc update-test`               Simulate an update

### Module: classic-composer

* `swdc build`                     Reinstalls the database
  * `--mysql-host`                 As optional parameter to specify mysql-host

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
  * `--without-demo-data`          As optional parameter to start without demo-data
  * `--without-building`           As optional parameter to start without built JS
  * `--mysql-host`                 As optional parameter to specify mysql-host
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

### Available Parameter-Values

#### PHPVERSION
* `80`
* `74`
* `72`