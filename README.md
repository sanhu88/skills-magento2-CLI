# skills-magento2-CLI
CLI of Magento version 2.4.3 notes

#  bin/magento list

The list command lists all commands:

~~~BASH
 php bin/magento list
 
 php bin/magento list --format=xml 	# XML格式
 php bin/magento list --raw		    # raw格式，整句命令，方便复制使用
~~~

结果

~~~bash
Magento CLI 2.4.3-p1

Usage:
  command [options] [arguments]

Options:
  -h, --help            Display this help message
  -q, --quiet           Do not output any message
  -V, --version         Display this application version
      --ansi            Force ANSI output
      --no-ansi         Disable ANSI output
  -n, --no-interaction  Do not ask any interactive question
  -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

Available commands:
  help                                                 Display help for a command
  list                                                 List commands
 admin
  admin:user:create                                    Creates an administrator
  admin:user:unlock                                    Unlock Admin Account
 app
  app:config:dump                                      Create dump of application
  app:config:import                                    Import data from shared configuration files to appropriate data storage
  app:config:status                                    Checks if config propagation requires update
 braintree
  braintree:migrate                                    Migrate stored cards from a Magento 1 database
 cache
  cache:clean                                          Cleans cache type(s)
  cache:disable                                        Disables cache type(s)
  cache:enable                                         Enables cache type(s)
  cache:flush                                          Flushes cache storage used by cache type(s)
  cache:status                                         Checks cache status
 catalog
  catalog:images:resize                                Creates resized product images
  catalog:product:attributes:cleanup                   Removes unused product attributes.
 cms
  cms:wysiwyg:restrict                                 Set whether to enforce user HTML content validation or show a warning instead
 config
  config:sensitive:set                                 Set sensitive configuration values
  config:set                                           Change system configuration
  config:show                                          Shows configuration value for given path. If path is not specified, all saved values will be shown
 cron
  cron:install                                         Generates and installs crontab for current user
  cron:remove                                          Removes tasks from crontab
  cron:run                                             Runs jobs by schedule
 customer
  customer:hash:upgrade                                Upgrade customer's hash according to the latest algorithm
 deploy
  deploy:mode:set                                      Set application mode.
  deploy:mode:show                                     Displays current application mode.
 dev
  dev:di:info                                          Provides information on Dependency Injection configuration for the Command.
  dev:profiler:disable                                 Disable the profiler.
  dev:profiler:enable                                  Enable the profiler.
  dev:query-log:disable                                Disable DB query logging
  dev:query-log:enable                                 Enable DB query logging
  dev:source-theme:deploy                              Collects and publishes source files for theme.
  dev:template-hints:disable                           Disable frontend template hints. A cache flush might be required.
  dev:template-hints:enable                            Enable frontend template hints. A cache flush might be required.
  dev:template-hints:status                            Show frontend template hints status.
  dev:tests:run                                        Runs tests
  dev:urn-catalog:generate                             Generates the catalog of URNs to *.xsd mappings for the IDE to highlight xml.
  dev:xml:convert                                      Converts XML file using XSL style sheets
 dotdigital
  dotdigital:connector:automap                         Auto-map data fields
  dotdigital:connector:enable                          Add Dotdigital API credentials and enable the connector
  dotdigital:migrate                                   Migrate data into email_ tables to sync with Engagement Cloud
  dotdigital:sync                                      Run syncs to populate email_ tables before importing to Engagement Cloud
  dotdigital:task                                      Run dotdigital module tasks on demand
 downloadable
  downloadable:domains:add                             Add domains to the downloadable domains whitelist
  downloadable:domains:remove                          Remove domains from the downloadable domains whitelist
  downloadable:domains:show                            Display downloadable domains whitelist
 encryption
  encryption:payment-data:update                       Re-encrypts encrypted credit card data with latest encryption cipher.
 i18n
  i18n:collect-phrases                                 Discovers phrases in the codebase
  i18n:pack                                            Saves language package
  i18n:uninstall                                       Uninstalls language packages
 indexer
  indexer:info                                         Shows allowed Indexers
  indexer:reindex                                      Reindexes Data
  indexer:reset                                        Resets indexer status to invalid
  indexer:set-dimensions-mode                          Set Indexer Dimensions Mode
  indexer:set-mode                                     Sets index mode type
  indexer:show-dimensions-mode                         Shows Indexer Dimension Mode
  indexer:show-mode                                    Shows Index Mode
  indexer:status                                       Shows status of Indexer
 info
  info:adminuri                                        Displays the Magento Admin URI
  info:backups:list                                    Prints list of available backup files
  info:currency:list                                   Displays the list of available currencies
  info:dependencies:show-framework                     Shows number of dependencies on Magento framework
  info:dependencies:show-modules                       Shows number of dependencies between modules
  info:dependencies:show-modules-circular              Shows number of circular dependencies between modules
  info:language:list                                   Displays the list of available language locales
  info:timezone:list                                   Displays the list of available timezones
 inventory
  inventory:reservation:create-compensations           Create reservations by provided compensation arguments
  inventory:reservation:list-inconsistencies           Show all orders and products with salable quantity inconsistencies
 inventory-geonames
  inventory-geonames:import                            Download and import geo names for source selection algorithm
 maintenance
  maintenance:allow-ips                                Sets maintenance mode exempt IPs
  maintenance:disable                                  Disables maintenance mode
  maintenance:enable                                   Enables maintenance mode
  maintenance:status                                   Displays maintenance mode status
 media-content
  media-content:sync                                   Synchronize content with assets
 media-gallery
  media-gallery:sync                                   Synchronize media storage and media assets in the database
 module
  module:config:status                                 Checks the modules configuration in the 'app/etc/config.php' file and reports if they are up to date or not
  module:disable                                       Disables specified modules
  module:enable                                        Enables specified modules
  module:status                                        Displays status of modules
  module:uninstall                                     Uninstalls modules installed by composer
 newrelic
  newrelic:create:deploy-marker                        Check the deploy queue for entries and create an appropriate deploy marker.
 queue
  queue:consumers:list                                 List of MessageQueue consumers
  queue:consumers:start                                Start MessageQueue consumer
 remote-storage
  remote-storage:sync                                  Synchronize media files with remote storage.
 sampledata
  sampledata:deploy                                    Deploy sample data modules for composer-based Magento installations
  sampledata:remove                                    Remove all sample data packages from composer.json
  sampledata:reset                                     Reset all sample data modules for re-installation
 security
  security:recaptcha:disable-for-user-forgot-password  Disable reCAPTCHA for admin user forgot password form
  security:recaptcha:disable-for-user-login            Disable reCAPTCHA for admin user login form
 setup
  setup:backup                                         Takes backup of Magento Application code base, media and database
  setup:config:set                                     Creates or modifies the deployment configuration
  setup:db-data:upgrade                                Installs and upgrades data in the DB
  setup:db-declaration:generate-patch                  Generate patch and put it in specific folder.
  setup:db-declaration:generate-whitelist              Generate whitelist of tables and columns that are allowed to be edited by declaration installer
  setup:db-schema:upgrade                              Installs and upgrades the DB schema
  setup:db:status                                      Checks if DB schema or data requires upgrade
  setup:di:compile                                     Generates DI configuration and all missing classes that can be auto-generated
  setup:install                                        Installs the Magento application
  setup:performance:generate-fixtures                  Generates fixtures
  setup:rollback                                       Rolls back Magento Application codebase, media and database
  setup:static-content:deploy                          Deploys static view files
  setup:store-config:set                               Installs the store configuration. Deprecated since 2.2.0. Use config:set instead
  setup:uninstall                                      Uninstalls the Magento application
  setup:upgrade                                        Upgrades the Magento application, DB data, and schema
 store
  store:list                                           Displays the list of stores
  store:website:list                                   Displays the list of websites
 theme
  theme:uninstall                                      Uninstalls theme
 varnish
  varnish:vcl:generate                                 Generates Varnish VCL and echos it to the command line
 vertex
  vertex:tax:warm-wsdl-cache                           Execute WSDL Cache Warming
 yotpo
  yotpo:reset                                          Reset Yotpo sync flags &/or configurations
  yotpo:sync                                           Sync Yotpo manually (reviews module)
  yotpo:update-metadata                                Manually send platform metadata to Yotpo
~~~



~~~bash
# php bin/magento list --raw
help                                                  Display help for a command
list                                                  List commands
admin:user:create                                     Creates an administrator
admin:user:unlock                                     Unlock Admin Account
app:config:dump                                       Create dump of application
app:config:import                                     Import data from shared configuration files to appropriate data storage
app:config:status                                     Checks if config propagation requires update
braintree:migrate                                     Migrate stored cards from a Magento 1 database
cache:clean                                           Cleans cache type(s)
cache:disable                                         Disables cache type(s)
cache:enable                                          Enables cache type(s)
cache:flush                                           Flushes cache storage used by cache type(s)
cache:status                                          Checks cache status
catalog:images:resize                                 Creates resized product images
catalog:product:attributes:cleanup                    Removes unused product attributes.
cms:wysiwyg:restrict                                  Set whether to enforce user HTML content validation or show a warning instead
config:sensitive:set                                  Set sensitive configuration values
config:set                                            Change system configuration
config:show                                           Shows configuration value for given path. If path is not specified, all saved values will be shown
cron:install                                          Generates and installs crontab for current user
cron:remove                                           Removes tasks from crontab
cron:run                                              Runs jobs by schedule
customer:hash:upgrade                                 Upgrade customer's hash according to the latest algorithm
deploy:mode:set                                       Set application mode.
deploy:mode:show                                      Displays current application mode.
dev:di:info                                           Provides information on Dependency Injection configuration for the Command.
dev:profiler:disable                                  Disable the profiler.
dev:profiler:enable                                   Enable the profiler.
dev:query-log:disable                                 Disable DB query logging
dev:query-log:enable                                  Enable DB query logging
dev:source-theme:deploy                               Collects and publishes source files for theme.
dev:template-hints:disable                            Disable frontend template hints. A cache flush might be required.
dev:template-hints:enable                             Enable frontend template hints. A cache flush might be required.
dev:template-hints:status                             Show frontend template hints status.
dev:tests:run                                         Runs tests
dev:urn-catalog:generate                              Generates the catalog of URNs to *.xsd mappings for the IDE to highlight xml.
dev:xml:convert                                       Converts XML file using XSL style sheets
dotdigital:connector:automap                          Auto-map data fields
dotdigital:connector:enable                           Add Dotdigital API credentials and enable the connector
dotdigital:migrate                                    Migrate data into email_ tables to sync with Engagement Cloud
dotdigital:sync                                       Run syncs to populate email_ tables before importing to Engagement Cloud
dotdigital:task                                       Run dotdigital module tasks on demand
downloadable:domains:add                              Add domains to the downloadable domains whitelist
downloadable:domains:remove                           Remove domains from the downloadable domains whitelist
downloadable:domains:show                             Display downloadable domains whitelist
encryption:payment-data:update                        Re-encrypts encrypted credit card data with latest encryption cipher.
i18n:collect-phrases                                  Discovers phrases in the codebase
i18n:pack                                             Saves language package
i18n:uninstall                                        Uninstalls language packages
indexer:info                                          Shows allowed Indexers
indexer:reindex                                       Reindexes Data
indexer:reset                                         Resets indexer status to invalid
indexer:set-dimensions-mode                           Set Indexer Dimensions Mode
indexer:set-mode                                      Sets index mode type
indexer:show-dimensions-mode                          Shows Indexer Dimension Mode
indexer:show-mode                                     Shows Index Mode
indexer:status                                        Shows status of Indexer
info:adminuri                                         Displays the Magento Admin URI
info:backups:list                                     Prints list of available backup files
info:currency:list                                    Displays the list of available currencies
info:dependencies:show-framework                      Shows number of dependencies on Magento framework
info:dependencies:show-modules                        Shows number of dependencies between modules
info:dependencies:show-modules-circular               Shows number of circular dependencies between modules
info:language:list                                    Displays the list of available language locales
info:timezone:list                                    Displays the list of available timezones
inventory:reservation:create-compensations            Create reservations by provided compensation arguments
inventory:reservation:list-inconsistencies            Show all orders and products with salable quantity inconsistencies
inventory-geonames:import                             Download and import geo names for source selection algorithm
maintenance:allow-ips                                 Sets maintenance mode exempt IPs
maintenance:disable                                   Disables maintenance mode
maintenance:enable                                    Enables maintenance mode
maintenance:status                                    Displays maintenance mode status
media-content:sync                                    Synchronize content with assets
media-gallery:sync                                    Synchronize media storage and media assets in the database
module:config:status                                  Checks the modules configuration in the 'app/etc/config.php' file and reports if they are up to date or not
module:disable                                        Disables specified modules
module:enable                                         Enables specified modules
module:status                                         Displays status of modules
module:uninstall                                      Uninstalls modules installed by composer
newrelic:create:deploy-marker                         Check the deploy queue for entries and create an appropriate deploy marker.
queue:consumers:list                                  List of MessageQueue consumers
queue:consumers:start                                 Start MessageQueue consumer
remote-storage:sync                                   Synchronize media files with remote storage.
sampledata:deploy                                     Deploy sample data modules for composer-based Magento installations
sampledata:remove                                     Remove all sample data packages from composer.json
sampledata:reset                                      Reset all sample data modules for re-installation
security:recaptcha:disable-for-user-forgot-password   Disable reCAPTCHA for admin user forgot password form
security:recaptcha:disable-for-user-login             Disable reCAPTCHA for admin user login form
setup:backup                                          Takes backup of Magento Application code base, media and database
setup:config:set                                      Creates or modifies the deployment configuration
setup:db-data:upgrade                                 Installs and upgrades data in the DB
setup:db-declaration:generate-patch                   Generate patch and put it in specific folder.
setup:db-declaration:generate-whitelist               Generate whitelist of tables and columns that are allowed to be edited by declaration installer
setup:db-schema:upgrade                               Installs and upgrades the DB schema
setup:db:status                                       Checks if DB schema or data requires upgrade
setup:di:compile                                      Generates DI configuration and all missing classes that can be auto-generated
setup:install                                         Installs the Magento application
setup:performance:generate-fixtures                   Generates fixtures
setup:rollback                                        Rolls back Magento Application codebase, media and database
setup:static-content:deploy                           Deploys static view files
setup:store-config:set                                Installs the store configuration. Deprecated since 2.2.0. Use config:set instead
setup:uninstall                                       Uninstalls the Magento application
setup:upgrade                                         Upgrades the Magento application, DB data, and schema
store:list                                            Displays the list of stores
store:website:list                                    Displays the list of websites
theme:uninstall                                       Uninstalls theme
varnish:vcl:generate                                  Generates Varnish VCL and echos it to the command line
vertex:tax:warm-wsdl-cache                            Execute WSDL Cache Warming
yotpo:reset                                           Reset Yotpo sync flags &/or configurations
yotpo:sync                                            Sync Yotpo manually (reviews module)
yotpo:update-metadata                                 Manually send platform metadata to Yotpo

~~~

## admin

~~~bash
admin:user:create
# 创建一个管理员账户
bin/magento admin:user:create
Admin user: Burt
Admin password:
Admin email: xxx@qq.com
Admin first name: Burt
Admin last name:  xxx

~~~

~~~bash
admin:user:unlock
# 解锁账户，后面要加用户名参数
bin/magento admin:user:unlock Burt
The user account "Burt" was not locked or could not be unlocked
~~~

