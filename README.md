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
dotdigital
# 类似ERP 云端软件，$400/mo
```

```bash
downloadable
# 非重点业务范围 skip
```

## encryption

```bash
encryption:payment-data:update
# 使用最新加密方法重新加密信用卡数据
bin/magento encryption:payment-data:update
```

## i18n

```bash
i18n:uninstall
# 卸载语言包，形参 语言包名称
bin/magento i18n:uninstall
```

```bash
i18n:pack
# 保存语言包，两个形参
bin/magento i18n:pack
Usage:
  i18n:pack [options] [--] <source> <locale>

Arguments:
  source                  Path to source dictionary file with translations
  locale                  Target locale for dictionary, for example "de_DE"
```

```bash
i18n:collect-phrases
# 在代码库探索短语，一个词典形参
bin/magento i18n:collect-phrases
```

## *indexer

[Magento link](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html)

```bash
indexer:status
# 表格形式展示索引状态，展示结果包含indexer:info 
bin/magento indexer:status
```

```bash
indexer:info 
# 对应关系ID 和Title
bin/magento indexer:info 
design_config_grid                       Design Config Grid
customer_grid                            Customer Grid
catalog_category_product                 Category Products
catalog_product_category                 Product Categories
catalogrule_rule                         Catalog Rule Product
catalog_product_attribute                Product EAV
inventory                                Inventory
catalogrule_product                      Catalog Product Rule
cataloginventory_stock                   Stock
catalog_product_price                    Product Price
catalogsearch_fulltext                   Catalog Search
```

```bash
indexer:show-mode
# 显示索引模式
bin/magento indexer:show-mode
Design Config Grid:                                Update on Save
Customer Grid:                                     Update on Save
Category Products:                                 Update on Save
Product Categories:                                Update on Save
Catalog Rule Product:                              Update on Save
Product EAV:                                       Update on Save
Inventory:                                         Update on Save
Catalog Product Rule:                              Update on Save
Stock:                                             Update on Save
Product Price:                                     Update on Save
Catalog Search:                                    Update on Save
```

```bash
indexer:set-mode
# 设定索引模式，两个形参 mode are 'realtime' or 'schedule'和index ID
bin/magento indexer:set-mode
```

```bash
indexer:show-dimensions-mode
# catalog_product_price 的mode
bin/magento indexer:show-dimensions-mode
Product Price:                                     none
```

```bash
indexer:set-dimensions-mode
# 修改 catalog_product_price 的mode，两个形参，一个catalog_product_price，第二个选项。
# 主要用来价格排序
bin/magento indexer:set-dimensions-mode
Usage:
  indexer:set-dimensions-mode [<indexer> [<mode>]]

Arguments:
  indexer               Indexer name [catalog_product_price]
  mode                  Indexer dimension modes
                        catalog_product_price          none,website,customer_group,website_and_customer_group
```

```bash
indexer:reindex
# 从新创建索引
bin/magento indexer:reindex
```

```bash
indexer:reset
# 重置索引，把索引设置为无效状态
bin/magento indexer:reset
Design Config Grid indexer has been invalidated.
Customer Grid indexer has been invalidated.
Category Products indexer has been invalidated.
Product Categories indexer has been invalidated.
Catalog Rule Product indexer has been invalidated.
Product EAV indexer has been invalidated.
Inventory indexer has been invalidated.
Catalog Product Rule indexer has been invalidated.
Stock indexer has been invalidated.
Product Price indexer has been invalidated.
Catalog Search indexer has been invalidated.
```

## info

```bash
info:adminuri
# 后台admin URI
bin/magento info:adminuri
Admin URI: /admin_ipzz2r
```

```bash
info:language:list
# 语言列表和code 表格
bin/magento info:language:list
# zh_Hans_CN
# en_US
```

```bash
info:timezone:list
# 时区列表和code 表格
bin/magento info:timezone:list
# Asia/Shanghai 
# Pacific Standard Time (America/Los_Angeles) America/Los_Angeles
```

```bash
info:backups:list
# 可用的备份文件
bin/magento info:backups:list
No backup files found.
```

```bash
info:currency:list 
# 货币列表和code 表格
bin/magento info:currency:list 
```

```bash
info:dependencies:show-framework 
# 根目录framework-dependencies.csv 依赖Magento框架的数量
bin/magento info:dependencies:show-framework 
```

```bash
info:dependencies:show-modules
# 根目录modules-dependencies.csv 模块之间的依赖关系
bin/magento info:dependencies:show-modules
```

```bash
info:dependencies:show-modules-circular
# 根目录modules-circular-dependencies.csv 循环依赖关系
bin/magento info:dependencies:show-modules-circular
```

## inventory

```bash
inventory:reservation:create-compensations
# Create reservations by provided compensation arguments
# 通过提供的补偿论据创建保留？
bin/magento inventory:reservation:create-compensations
```

```bash
inventory:reservation:list-inconsistencies
# 显示所有产品可售数量不一致
bin/magento inventory:reservation:list-inconsistencies
Order 000000001:
  - Product WS03-XS-Red should be compensated by -1.000000 for stock 1
Order 000000002:
  - Product WS08-XS-Blue should be compensated by -1.000000 for stock 1
```

```bash
inventory-geonames:import
# 下载并导入地理名称，用于来源选择算法？
bin/magento inventory-geonames:import
```

## maintenance

```bash
maintenance:status
# 维护状态
bin/magento maintenance:status
Status: maintenance mode is not active
List of exempt IP-addresses: none
```

```bash
maintenance:allow-ips
# 添加 清除允许IP
bin/magento maintenance:allow-ips
```

```bash
maintenance:enable 
# 开启维护状态
bin/magento maintenance:enable 
```

```bash
maintenance:disable
# 关闭维护状态
bin/magento maintenance:disable
```

## media

```bash
media-content:sync
# Synchronize content with assets 同步内容与资源
bin/magento media-content:sync
Synchronizing content with assets...
Completed content synchronization.
```

```bash
media-gallery:sync
# 在数据库中同步媒体存储和媒体资源
bin/magento media-gallery:sync
Synchronizing assets information from media storage to database...
Completed assets synchronization.
```

## *module

```bash
module:status
# 模块状态
bin/magento module:status
List of enabled modules:
...
List of disabled modules:
...
```

```bash
module:config:status
# 检查app/etc/config.php模块设置
bin/magento module:config:status
The modules configuration is up to date.
```

```bash
module:disable 
# 禁用模块，形参
bin/magento module:disable 
bin/magento module:disable --clear-static-content
```

```bash
module:enable
# 开启模块，形参
bin/magento module:enable
```

```bash
module:uninstall 
# 卸载模块，形参
bin/magento module:uninstall 
Arguments:
  module                                         Name of the module

Options:
  -r, --remove-data                              Remove data installed by module(s)
      --backup-code                              Take code and configuration files backup (excluding temporary files)
      --backup-media                             Take media backup
      --backup-db                                Take complete database backup
      --non-composer                             All modules, that will be past here will be non composer based
  -c, --clear-static-content                     Clear generated static view files. Necessary, if the module(s) have static view files
      --magento-init-params=MAGENTO-INIT-PARAMS  Add to any command to customize Magento initialization parameters
                                                 For example: "MAGE_MODE=developer&MAGE_DIRS[base][path]=/var/www/example.com&MAGE_DIRS[cache][path]=/var/tmp/cache"
```

```bash
newrelic:create:deploy-marker 
# Check the deploy queue for entries and create an appropriate deploy marker.
# 检查部署队列中的条目，并创建一个适当的部署标记。
bin/magento newrelic:create:deploy-marker 
## New Relic是一种软件分析服务，可帮助您分析和改进应用程序交互
```

## queue

```bash
queue:consumers:list
# 列出MessageQueue 消费者
bin/magento queue:consumers:list
product_action_attribute.update
product_action_attribute.website.update
media.storage.catalog.image.resize
exportProcessor
inventory.source.items.cleanup
inventory.mass.update
inventory.reservations.cleanup
inventory.reservations.update
inventory.reservations.updateSalabilityStatus
inventory.indexer.sourceItem
inventory.indexer.stock
media.content.synchronization
media.gallery.renditions.update
media.gallery.synchronization
codegeneratorProcessor
sales.rule.update.coupon.usage
async.operations.all
```

```bash
queue:consumers:start
# 形参 consumer
bin/magento queue:consumers:start
Help:
  This command starts MessageQueue consumer by its name.

  To start consumer which will process all queued messages and terminate execution:

      bin/magento queue:consumers:start someConsumer

  To specify the number of messages which should be processed by consumer before its termination:

      bin/magento queue:consumers:start someConsumer --max-messages=50

  To specify the number of messages per batch for the batch consumer:

      bin/magento queue:consumers:start someConsumer --batch-size=500

  To specify the preferred area:

      bin/magento queue:consumers:start someConsumer --area-code='adminhtml'

  To do not run multiple copies of one consumer simultaneously:

      bin/magento queue:consumers:start someConsumer --single-thread'

  To save PID enter path (This option is deprecated, use --single-thread instead):

      bin/magento queue:consumers:start someConsumer --pid-file-path='/var/someConsumer.pid'

```

```bash
remote-storage:sync
# Synchronize media files with remote storage.
bin/magento remote-storage:sync
```

## sampledata

```bash
sampledata:remove
# 从composer.json移除 sample数据文件包
bin/magento sampledata:remove
```

```bash
sampledata:reset
# 重置所有数据包为再次安装做准备
bin/magento sampledata:reset
```

```bash
sampledata:deploy
# 部署sample数据模组
bin/magento sampledata:deploy
```

## security

```bash
security:recaptcha:disable-for-user-forgot-password
# 关闭admin找回密码的验证码
bin/magento security:recaptcha:disable-for-user-forgot-password
```

```bash
security:recaptcha:disable-for-user-login 
# 关闭admin登陆的验证码
bin/magento security:recaptcha:disable-for-user-login 
```

## *setup

```bash
setup:static-content:deploy
# 部署静态view 文件
bin/magento setup:static-content:deploy -f
Deploy using quick strategy
frontend/Magento/blank/en_US            2265/2265           ============================ 100%   < 1 sec
adminhtml/Magento/backend/en_US         2915/2915           ============================ 100%   1 sec
frontend/Magento/luma/en_US             2281/2281           ============================ 100%   1 sec
Execution time: 6.6236588954926
```

```bash
setup:di:compile
# 生成DI配置，missing的类可以自动生成
bin/magento setup:di:compile
Compilation was started.
Plugin list generation... 9/9 [============================] 100% 1 min 438.0 MiB
Generated code and dependency injection configuration successfully.
```

```bash
setup:upgrade
# 升级Magento 程序application 数据库数据，结构schema
bin/magento setup:upgrade
Cache types config flushed successfully
Cache cleared successfully
File system cleanup:
...
Updating modules:
Cache cleared successfully
Schema creation/updates:
...
Schema post-updates:
...
Enabling caches:
Current status:
layout: 1
block_html: 1
full_page: 1
Nothing to import.
Media files stored outside of 'Media Gallery Allowed' folders will not be available to the media gallery.
Please refer to Developer Guide for more details.

```

```bash
setup:uninstall
# 卸载 Magento application
bin/magento setup:uninstall
```

```bash
setup:install
# 安装 Magento application
bin/magento setup:install
```

```bash
setup:rollback 
# 回滚 Magento Application codebase, media and database
bin/magento setup:rollback 
```

```bash
setup:performance:generate-fixtures 
# 生成 fixtures 固定资产？，形参 "profile"
bin/magento setup:performance:generate-fixtures 
bin/magento setup:performance:generate-fixtures setup/performance-toolkit/profiles/ce/small.xml
Generating profile with following params:
 |- Admin Users: 50
 |- Websites: 1
 |- Store Groups Count: 1
 |- Store Views Count: 1
 |- Categories: 30
 |- Attribute Sets (Default): 3
 |- Attribute Sets (Extra): 10
 |- Simple products: 800
 |- Configurable products: 16
 |- Product images: 100, 3 per product
 |- Customers: 200
 |- Cart Price Rules: 20
 |- Catalog Price Rules: 20
 |- Coupon Codes: 20
 |- Orders: 80
Config Changes...  done in 00:00:00
SQLSTATE[HY000]: General error: 1419 You do not have the SUPER privilege and binary logging is enabled (you *might* want to use the less safe log_bin_trust_function_creators variable), query was: CREATE TRIGGER trg_catalog_category_entity_after_insert AFTER INSERT ON catalog_category_entity FOR EACH ROW
BEGIN
INSERT IGNORE INTO `catalog_category_product_cl` (`entity_id`) VALUES (NEW.`entity_id`);
END

# https://github.com/magento/magento2/tree/2.4/setup/performance-toolkit
```

```bash
setup:db:status
# 检查数据结构或数据是否满足升级
bin/magento setup:db:status
All modules are up to date.
```

```bash
setup:db-schema:upgrade
# 安装和升级数据结构 DB schema
bin/magento setup:db-schema:upgrade
```

```bash
setup:db-data:upgrade
# 安装和升级数据库数据 
bin/magento setup:db-data:upgrade
```

```bash
setup:db-declaration:generate-patch
# 生成patch补丁并放在指定文件夹
bin/magento setup:db-declaration:generate-patch
Arguments:
  module                         Module name
  patch                          Patch name

```

```bash
setup:db-declaration:generate-whitelist
#  Generate whitelist of tables and columns that are allowed to be edited by declaration installer
# 生成声明安装程序允许编辑的表和列的白名单
bin/magento setup:db-declaration:generate-whitelist
```

```bash
setup:store-config:set
# Installs the store configuration. Deprecated since 2.2.0. Use config:set instead
```

```bash
setup:backup
# 
bin/magento setup:backup
Options:
      --code                                     Take code and configuration files backup (excluding temporary files)
      --media                                    Take media backup
      --db                                       Take complete database backup
      --magento-init-params=MAGENTO-INIT-PARAMS  Add to any command to customize Magento initialization parameters
                                                 For example: "MAGE_MODE=developer&MAGE_DIRS[base][path]=/var/www/example.com&MAGE_DIRS[cache][path]=/var/tmp/cache"


bin/magento setup:backup --db
Enabling maintenance mode
DB backup is starting...
Backup functionality is disabled
Disabling maintenance mode
```

## store

```bash
store:list
# 表格方式列出所有stores
bin/magento store:list
+----+------------+----------+--------------------+---------+------------+-----------+
| ID | Website ID | Group ID | Name               | Code    | Sort Order | Is Active |
+----+------------+----------+--------------------+---------+------------+-----------+
| 1  | 1          | 1        | Default Store View | default | 0          | 1         |
| 0  | 0          | 0        | Admin              | admin   | 0          | 1         |
+----+------------+----------+--------------------+---------+------------+-----------+
```

```bash
store:website:list
# 表格方式列出所有website
bin/magento store:website:list
+----+------------------+--------------+-------+------------+------------+
| ID | Default Group Id | Name         | Code  | Sort Order | Is Default |
+----+------------------+--------------+-------+------------+------------+
| 0  | 0                | Admin        | admin | 0          | 0          |
| 1  | 1                | Main Website | base  | 0          | 1          |
+----+------------------+--------------+-------+------------+------------+
```

```bash
theme:uninstall
# 卸载主题，形参主题名 举例frontend/Magento/blank
bin/magento theme:uninstall
bin/magento theme:uninstall frontend/Magento/blank
Unable to uninstall. Please resolve the following issues:
frontend/Magento/blank is a parent of physical theme. Parent themes cannot be uninstalled.
frontend/Magento/blank has the following dependent package(s):
        magento/product-community-edition
        magento/theme-frontend-luma
```

```bash
varnish:vcl:generate
# Generates Varnish VCL and echos it to the command line
bin/magento varnish:vcl:generate
```

```bash
vertex:tax:warm-wsdl-cache 
# Execute WSDL Cache Warming
bin/magento vertex:tax:warm-wsdl-cache 
```

## yotpo

```bash
yotpo:reset 
# 重置Yotpo 同步标签、配置
bin/magento yotpo:reset 
```

```bash
yotpo:sync
# 手动同步Yotpo
bin/magento yotpo:sync
```

```bash
yotpo:update-metadata
# 手动发送元数据给Yotpo
bin/magento yotpo:update-metadata
```

````bash
```bash

# 
bin/magento 
```
````
