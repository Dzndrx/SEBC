# Start Hive
```
curl -X POST -u Dzndrx:cloudera http://localhost:7180/api/v19/clusters/Dzndrx/services/hive/commands/stop
```

# Stop Hive
```
curl -X POST -u Dzndrx:cloudera http://localhost:7180/api/v19/clusters/Dzndrx/services/hive/commands/start
```

# Status Hive
```
curl -X GET -u Dzndrx:cloudera http://localhost:7180/api/v19/clusters/Dzndrx/services/hive
```