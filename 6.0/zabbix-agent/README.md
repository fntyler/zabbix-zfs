# Zabbix Server 6.0

server version: 6.0.9


## host configuration

### item

key: `zfs.pool.status[<zfs_pool_name>]`

parameters:

`zfs_pool_name`, string value of ZFS pool name.

return value type: text

Example 1

```
zfs.zpool.status[ztank]
```

Example trigger expression 1: `find(/host/key,,"like","healthy")<>1`

Ref: [6.0/functions/history-functions](https://www.zabbix.com/documentation/6.0/en/manual/appendix/functions/history)


# Zabbix Agent

agent version: 6.0.23

agent version v2: Null


## zabbix_agentd.conf

Add `Include=<value>` parameter to Zabbix Agent configuration file.

Set `<value>` as the absolute path to single file or all files of a directory.

```
Include=/absolute/path/to/config/files/*.conf
```

Ref: [6.0/config/zabbix-agentd](https://www.zabbix.com/documentation/6.0/en/manual/appendix/config/zabbix_agentd)


## zfs.conf

Add `zfs.conf` configuration file to the `Include=<value>` directory or append the contents to the `zabbix_agentd.conf` directly.

Ref: [6.0/items/user-parameters](https://www.zabbix.com/documentation/6.0/en/manual/config/items/userparameters)
