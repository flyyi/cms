# Cloud-Native Distributed Database PolarDB-X 1.0

This topic describes the metrics for PolarDB-X V1.0.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_drds**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|DRDS\_CPUUtilization|%|CPUUtilization|userId and instanceId|Average|
|DRDS\_ConnectionCount|count|ConnectionCount|userId and instanceId|Average|
|DRDS\_LogicQPS|count|LogicQPS|userId and instanceId|Average|
|DRDS\_LogicRT|ms|LogicRT|userId and instanceId|Average|
|DRDS\_MemoryUtilization|%|MemoryUtilization|userId and instanceId|Average|
|DRDS NetworkInput Traffic|bit/s|NetworkInputTraffic|userId and instanceId|Average|
|DRDS NetworkOutputTraffic|bit/s|NetworkOutputTraffic|userId and instanceId|Average|
|DRDS\_PhysicsQPS|count|PhysicsQPS|userId and instanceId|Average|
|DRDS\_PhysicsRT|ms|PhysicsRT|userId and instanceId|Average|
|DRDS\_ThreadCount|count|ThreadCount|userId and instanceId|Average|
|RDS\_MySQL InsertSelect/s|count|com\_insert\_select|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Replace/s|count|com\_replace|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL ReplaceSelect/s|count|com\_replace\_select|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Select/s|count|com\_select|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Update/s|count|com\_update|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Conn Usage|%|conn\_usage|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL CPU Usage|%|cpu\_usage|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Disk Usage|%|disk\_usage|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Dirty Ratio|%|ibuf\_dirty\_ratio|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Pool Reads|count|ibuf\_pool\_reads|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Read Hit|%|ibuf\_read\_hit|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Request Read|count|ibuf\_request\_r|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Request Write|count|ibuf\_request\_w|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Ibuf Use Ratio|%|ibuf\_use\_ratio|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno data read|KB|inno\_data\_read|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno data written|KB|inno\_data\_written|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno row delete|count|inno\_row\_delete|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno row insert|count|inno\_row\_insert|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno row readed|count|inno\_row\_readed|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Inno row update|count|inno\_row\_update|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Innodb log write requests|count|innodb\_log\_write\_requests|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Innodb log writes|count|innodb\_log\_writes|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Innodb os log fsyncs|count|innodb\_os\_log\_fsyncs|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Input traffic/s|bits/s|input\_traffic\_ps|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL IOPS Usage|%|iops\_usage|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Mem Usage|%|mem\_usage|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Output traffic/s|bits/s|output\_traffic\_ps|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL QPS|count|qps|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Slave lag|s|slave\_lag|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Slow queries|count|slow\_queries|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL Table tmp disk|count|tb\_tmp\_disk|userId, instanceId, and rdsInstId|Average|
|RDS\_MySQL TPS|count|tps|userId, instanceId, and rdsInstId|Average|
|DRDS\_CPUUtilization|%|CPUUtilization|userId and instanceId|Average|
|DRDS NetworkInput Traffic|bit/s|NetworkInputTraffic|userId and instanceId|Average|
|DRDS NetworkOutputTraffic|bit/s|NetworkOutputTraffic|userId and instanceId|Average|

