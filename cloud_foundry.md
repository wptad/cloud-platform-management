#CLOUD FOUNDRY



* Components <http://docs.cloudfoundry.com/docs/running/bosh/components/index.html>
* Architecture <http://docs.cloudfoundry.com/docs/running/architecture/index.html>

* How Applications Are Staged <http://docs.cloudfoundry.com/docs/running/architecture/how-applications-are-staged.html>


#Get started

* Installing Ruby

<http://docs.cloudfoundry.com/docs/common/install_ruby.html#osx>

* RubyGems Install 

<https://rubygems.org/pages/download>

* BOSH Local Setup
```
gem install bosh_cli_plugin_micro "~> 1.5.0.pre" --source https://s3.amazonaws.com/bosh-jenkins-gems/

rbenv rehash
```

<http://docs.cloudfoundry.com/docs/running/bosh/setup/>


* gem install bosh_deployer

```
gem install bosh_deployer
```
* FROM <http://docs.cloudfoundry.com/docs/running/deploying-cf/vcloud/deploying_to_vcloud_director.html>


* Using the latest CF-Release 

<http://docs.cloudfoundry.com/docs/running/deploying-cf/common/cf-release.html>


```
Building release
----------------

Generating manifest...
----------------------
Writing manifest...

Release summary
---------------
Packages
+---------------------------+----------+-------------+
| Name                      | Version  | Notes       |
+---------------------------+----------+-------------+
| backup_manager            | 39.1-dev |             |
| bandwidth_proxy           | 2        |             |
| buildpack_cache           | 0.1-dev  |             |
| cloud_controller_ng       | 12.1-dev |             |
| collector                 | 7.1-dev  |             |
| common                    | 5        |             |
| dashboard                 | 13       |             |
| daylimit                  | 5.1-dev  |             |
| dea_jvm                   | 3.1-dev  |             |
| dea_next                  | 15.1-dev |             |
| debian_nfs_server         | 3        |             |
| erlang                    | 3        |             |
| git                       | 1        |             |
| golang                    | 1.1-dev  |             |
| gorouter                  | 3.1-dev  |             |
| hadoop                    | 1        |             |
| hbase                     | 4        |             |
| health_manager_next       | 17.1-dev |             |
| imagemagick               | 2        |             |
| insight_agent             | 2        |             |
| libpq                     | 4.1-dev  |             |
| libyaml                   | 0.1-dev  |             |
| login                     | 12.1-dev |             |
| mongodb18                 | 1        |             |
| mongodb20                 | 2        |             |
| mongodb22                 | 1.1-dev  | new version |
| mongodb_gateway           | 56.1-dev | new version |
| mongodb_node              | 53.1-dev | new version |
| mongodb_node_ng           | 14.1-dev | new version |
| mongodb_proxy             | 9.1-dev  | new version |
| mysql                     | 13       |             |
| mysql55                   | 6        |             |
| mysql_gateway             | 61.1-dev | new version |
| mysql_node                | 57.1-dev | new version |
| mysql_node_ng             | 15.1-dev | new version |
| mysqlclient               | 3        |             |
| nats                      | 8        |             |
| nginx                     | 9        |             |
| nginx_next                | 1        |             |
| oauth2_gateway            | 4.1-dev  | new version |
| opentsdb                  | 4        |             |
| postgres                  | 4        |             |
| postgresql                | 7        |             |
| postgresql91              | 2        |             |
| postgresql92              | 0.1-dev  | new version |
| postgresql_gateway        | 44.1-dev | new version |
| postgresql_node           | 40.1-dev | new version |
| postgresql_node_ng        | 14.1-dev | new version |
| rabbit_gateway            | 52.1-dev | new version |
| rabbit_node               | 48.1-dev | new version |
| rabbit_node_ng            | 14.1-dev | new version |
| rabbitmq                  | 4        |             |
| rabbitmq-2.4              | 1        |             |
| rabbitmq-2.8              | 1        |             |
| rabbitmq-3.0              | 0.1-dev  | new version |
| redis22                   | 1        |             |
| redis24                   | 1        |             |
| redis26                   | 1        |             |
| redis_gateway             | 57.1-dev | new version |
| redis_node                | 54.1-dev | new version |
| redis_node_ng             | 15.1-dev | new version |
| rootfs_lucid64            | 0.1-dev  | new version |
| ruby                      | 7.1-dev  | new version |
| ruby_next                 | 2.1-dev  | new version |
| serialization_data_server | 16.1-dev | new version |
| service_broker            | 34.1-dev | new version |
| service_utilities         | 8        |             |
| servicesmgmt              | 0.1-dev  | new version |
| sqlite                    | 3        |             |
| syslog_aggregator         | 3.1-dev  | new version |
| uaa                       | 23.1-dev | new version |
| warden                    | 25.1-dev | new version |
+---------------------------+----------+-------------+

Jobs
+---------------------------+----------+-------------+
| Name                      | Version  | Notes       |
+---------------------------+----------+-------------+
| backup_manager            | 16.1-dev | new version |
| ccdb_postgres             | 6.1-dev  | new version |
| cloud_controller_ng       | 6.1-dev  | new version |
| collector                 | 5.1-dev  | new version |
| dashboard                 | 9.1-dev  | new version |
| dea_next                  | 11.1-dev | new version |
| debian_nfs_server         | 7        |             |
| gorouter                  | 1.1-dev  | new version |
| hbase_master              | 1        |             |
| hbase_slave               | 2.1-dev  | new version |
| health_manager_next       | 6.1-dev  | new version |
| login                     | 10.1-dev | new version |
| mongodb_gateway           | 31.1-dev | new version |
| mongodb_node              | 27.1-dev | new version |
| mongodb_node_ng           | 16.1-dev | new version |
| mysql_gateway             | 27.1-dev | new version |
| mysql_node                | 31.1-dev | new version |
| mysql_node_ng             | 14.1-dev | new version |
| nats                      | 9.1-dev  | new version |
| oauth2_gateway            | 2.1-dev  | new version |
| opentsdb                  | 15       |             |
| postgres                  | 3.1-dev  | new version |
| postgresql_gateway        | 26.1-dev | new version |
| postgresql_node           | 22.1-dev | new version |
| postgresql_node_ng        | 15.1-dev | new version |
| rabbit_gateway            | 20.1-dev | new version |
| rabbit_node               | 21       |             |
| rabbit_node_ng            | 14.1-dev | new version |
| redis_gateway             | 25.1-dev | new version |
| redis_node                | 24.1-dev | new version |
| redis_node_ng             | 14.1-dev | new version |
| router_next               | 9.1-dev  | new version |
| serialization_data_server | 9.1-dev  | new version |
| service_broker            | 8.1-dev  | new version |
| service_utilities         | 3        |             |
| servicesmgmt              | 0.1-dev  | new version |
| syslog_aggregator         | 9.1-dev  | new version |
| uaa                       | 26.1-dev | new version |
| vcap_redis                | 6.1-dev  | new version |
+---------------------------+----------+-------------+

Jobs affected by changes in this release
+---------------------------+----------+
| Name                      | Version  |
+---------------------------+----------+
| backup_manager            | 16.1-dev |
| ccdb_postgres             | 6.1-dev  |
| cloud_controller_ng       | 6.1-dev  |
| collector                 | 5.1-dev  |
| dashboard                 | 9.1-dev  |
| dea_next                  | 11.1-dev |
| gorouter                  | 1.1-dev  |
| hbase_slave               | 2.1-dev  |
| health_manager_next       | 6.1-dev  |
| login                     | 10.1-dev |
| mongodb_gateway           | 31.1-dev |
| mongodb_node              | 27.1-dev |
| mongodb_node_ng           | 16.1-dev |
| mysql_gateway             | 27.1-dev |
| mysql_node                | 31.1-dev |
| mysql_node_ng             | 14.1-dev |
| nats                      | 9.1-dev  |
| oauth2_gateway            | 2.1-dev  |
| postgres                  | 3.1-dev  |
| postgresql_gateway        | 26.1-dev |
| postgresql_node           | 22.1-dev |
| postgresql_node_ng        | 15.1-dev |
| rabbit_gateway            | 20.1-dev |
| rabbit_node_ng            | 14.1-dev |
| redis_gateway             | 25.1-dev |
| redis_node                | 24.1-dev |
| redis_node_ng             | 14.1-dev |
| router_next               | 9.1-dev  |
| serialization_data_server | 9.1-dev  |
| service_broker            | 8.1-dev  |
| servicesmgmt              | 0.1-dev  |
| syslog_aggregator         | 9.1-dev  |
| uaa                       | 26.1-dev |
| vcap_redis                | 6.1-dev  |
| rabbit_node               | 21       |
| service_utilities         | 3        |
+---------------------------+----------+

Release version: 131.1-dev
Release manifest: /Users/tad/src/cloudfoundry/cf-release/dev_releases/tad-test-release-131.1-dev.yml


```