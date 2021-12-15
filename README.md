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

## app

~~~bash
app:config:dump
# 备份程序设置
bin/magento app:config:dump
Shared configuration was written to config.php and system-specific configuration to env.php.
Shared configuration file (config.php) doesn't contain sensitive data for security reasons.
Sensitive data can be stored in the following environment variables:
CONFIG__DEFAULT__PAYMENT__PAYFLOWPRO__PARTNER for payment/payflowpro/partner
...
Done. Config types dumped: scopes, themes, system, i18n
~~~

~~~bash
app:config:import
# 从分享的配置文件导入appropriate相对应的数据存储
~~~

~~~bash
app:config:status
# 检查配置
bin/magento app:config:status
Config files are up to date.
~~~

## braintree

~~~bash
braintree:migrate
# 从M1的数据库迁移以保存的信用卡
bin/magento braintree:migrate

Database host/IP address:127.0.0.1
Database name:m243_dev
Database username:
Database user password:

~~~

## *cache

~~~bash
cache:clean
# 清空制定类型的缓存，不带参数就是全部
bin/magento cache:clean
Cleaned cache types:
config
layout
block_html
collections
reflection
db_ddl
compiled_config
eav
customer_notification
config_integration
config_integration_api
full_page
config_webservice
translate
vertex
~~~

~~~bash
cache:disable
# 禁用缓存
bin/magento cache:disable
Changed cache status:
                        config: 1 -> 0
                        layout: 1 -> 0
                    block_html: 1 -> 0
                   collections: 1 -> 0
                    reflection: 1 -> 0
                        db_ddl: 1 -> 0
               compiled_config: 1 -> 0
                           eav: 1 -> 0
         customer_notification: 1 -> 0
            config_integration: 1 -> 0
        config_integration_api: 1 -> 0
                     full_page: 1 -> 0
             config_webservice: 1 -> 0
                     translate: 1 -> 0
                        vertex: 1 -> 0
~~~

~~~bash
cache:enable
# 开启缓存，并清空
bin/magento cache:enable
Changed cache status:
                        config: 0 -> 1
                        layout: 0 -> 1
                    block_html: 0 -> 1
                   collections: 0 -> 1
                    reflection: 0 -> 1
                        db_ddl: 0 -> 1
                           eav: 0 -> 1
         customer_notification: 0 -> 1
            config_integration: 0 -> 1
        config_integration_api: 0 -> 1
                     full_page: 0 -> 1
             config_webservice: 0 -> 1
                     translate: 0 -> 1
                        vertex: 0 -> 1
Cleaned cache types:
config
layout
block_html
collections
reflection
db_ddl
eav
customer_notification
config_integration
config_integration_api
full_page
config_webservice
translate
vertex

~~~

~~~bash
cache:flush
# 冲刷缓存
bin/magento cache:flush
Flushed cache types:
config
layout
block_html
collections
reflection
db_ddl
compiled_config
eav
customer_notification
config_integration
config_integration_api
full_page
config_webservice
translate
vertex

~~~

>  the main difference between Cache clean and cache flush in Magento 2 is that cache:clean will wipe all the enabled items which are Magento-related, and cache:flush wipes out the cache storage.
>
> ​	-- [link](https://magecomp.com/blog/magento-2-difference-between-cache-clean-cache-flush/#Difference_Between_Magento_2_Cache_Clean_Cache_Flush)

```bash
cache:status
# 检查缓存状态
bin/magento cache:status
Current status:
                        config: 1
                        layout: 1
                    block_html: 1
                   collections: 1
                    reflection: 1
                        db_ddl: 1
               compiled_config: 1
                           eav: 1
         customer_notification: 1
            config_integration: 1
        config_integration_api: 1
                     full_page: 1
             config_webservice: 1
                     translate: 1
                        vertex: 1
```

## catalog

```bash
catalog:images:resize
# 调整产品图片
bin/magento catalog:images:resize
801/801 [============================] 100% 28 mins 128.5 MiB   | /w/s/wsh12-red_main_1.jpg
Product images resized successfully
# 耗时较久
```

```bash
catalog:product:attributes:cleanup
# 移除未使用的产品属性
bin/magento catalog:product:attributes:cleanup
Unused product attributes successfully cleaned up:
  catalog_product_entity_text
  catalog_product_entity_decimal
  catalog_product_entity_datetime
  catalog_product_entity_int
  catalog_product_entity_varchar
```

## cms

```bash
cms:wysiwyg:restrict
# 设置是强制用户HTML内容验证还是显示警告
bin/magento cms:wysiwyg:restrict
```

## config

~~~bash
config:show
# 
bin/magento config:show
# web/unsecure/base_url - http://m243.com/
# 系统所有的配置值
~~~

```bash
config:sensitive:set
# 设置敏感配置项的值
bin/magento config:sensitive:set
Configuration path for example group/section/field_name
```

```bash
config:set
# 改变系统设定，形参 "path, value"
bin/magento config:set
```

## cron

```bash
cron:install
# 为当前用户生成并安装定时任务
bin/magento cron:install
Crontab has been generated and saved
```

```bash
cron:remove
# 移除定时任务
bin/magento cron:remove
Magento cron tasks have been removed
```

```bash
cron:run
# 按照计划运行定时任务
bin/magento cron:run
Ran jobs by schedule.
# 服务器荷载
```

## customer

```bash
customer:hash:upgrade
# 按照最新的算法升级客户的hash according 散列显示
bin/magento customer:hash:upgrade
Finished
```

## *deploy

```bash
deploy:mode:show
# 显示当程序模式
bin/magento deploy:mode:show
Current application mode: developer. (Note: Environment variables may override this value.)
```

```bash
deploy:mode:set
# 设置程序模式 Available options are "developer" or "production"
bin/magento deploy:mode:set
```

## dev

```bash
dev:di:info
# 提供关于该命令的依赖注入配置的信息，形参"class"
bin/magento dev:di:info
```

```bash
dev:profiler:disable
# 关闭分析器
bin/magento dev:profiler:disable
Profiler disabled.
```

```bash
dev:profiler:enable 
# 启用分析器，每个页面的下方显示表格
bin/magento dev:profiler:enable 
Profiler enabled with html output.

bin/magento dev:profiler:enable csvfile
# 文件保存在<project_root>/var/log/profiler.csv
```

[Profiling Magento](https://devdocs.magento.com/guides/v2.4/config-guide/bootstrap/mage-profiler.html)

```bash
dev:query-log:disable
# 关闭数据库查询日志
bin/magento dev:query-log:disable
DB query logging disabled.
```

```bash
dev:query-log:enable 
# 开启数据库查询日志
bin/magento dev:query-log:enable 
DB query logging enabled.
# 文件保存在var/debug/db.log
```

```bash
dev:source-theme:deploy
# 从主题里收集并发布源文件  to create symlinks to LESS files
bin/magento dev:source-theme:deploy
# Warning: symlink() has been disabled for security reasons

```

> 与steup:static-content:deply 区别
>
> [stack-exchange](https://magento.stackexchange.com/questions/247533/cli-what-is-the-difference-between-setupstatic-contentdeploy-and-devsourc)

```bash
dev:template-hints:status
# 前台主题提示状态
bin/magento dev:template-hints:status
Template hints are disabled
```

```bash
dev:template-hints:disable
# 关闭主题提示
bin/magento dev:template-hints:disable
Template hints disabled. Refresh cache types
```

```bash
dev:template-hints:enable
# 开启主题提示
bin/magento dev:template-hints:enable
Template hints enabled.
```

```bash
dev:tests:run
# 运行测试
bin/magento dev:tests:run
# Warning: passthru() has been disabled for security reasons
```

```bash
dev:urn-catalog:generate
# 编辑器PhpStorm and Visual Studio Code，避免语法报错，URNs转成XSDs标准
bin/magento dev:urn-catalog:generate
```

> dev:urn-catalog:generate
>
> [Magento link](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-urn.html)

```bash
dev:xml:convert 
# 转换XML为XSL风格表单
bin/magento dev:xml:convert 
```

```bash

# 
bin/magento 
```

```bash

# 
bin/magento 
```

```bash

# 
bin/magento 
```

````bash

```bash

# 
bin/magento 
```
````
