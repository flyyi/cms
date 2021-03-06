# 弹性公网IP监控 {#concept_mng_pf5_xdb .concept}

云监控通过监控弹性公网IP的流出流量、流入流量、流出数据包数、流入数据包数等监控项，帮助您监测服务的运行状态，并支持您对监控项设置报警规则。在您购买弹性公网IP服务后，云监控会自动对上述监控项收集数据。

## 监控服务 {#section_bbw_jk4_ydb .section}

-   **监控项说明** 

    |监控项|含义|维度|单位|最小监控粒度|
    |:--|:-|:-|:-|:-----|
    |网络流入带宽|平均每秒通过EIP流入ECS的流量|实例|bit/s|1分钟|
    |网络流出带宽|平均每秒ECS通过EIP向外流出的流量|实例|bit/s|1分钟|
    |流入数据包数|平均每秒通过EIP流入ECS的数据包数量|实例|packages/s|1分钟|
    |流出数据包数|平均每秒ECS通过EIP向外流出的数据包数量|实例|packages/s|1分钟|
    |限速丢包速率|由于实际业务带宽使用超过设置的带宽峰值导致的数据包被丢弃的速率。|实例|pps|1分钟|


-   **查看监控数据** 
    1.  登录[云监控控制台](https://cms-intl.console.aliyun.com)。
    2.  单击左侧导航栏中**云服务监控**下的**弹性公网IP**，进入弹性公网IP监控列表页面。
    3.  单击实例名称或**操作**中的**监控图表**，进入监控图表页面。
    4.  \(可选\)单击大小图切换图标，切换大图显示。

## 报警服务 {#section_xtw_qk4_ydb .section}

-   **设置报警规则** 
    1.  登录[云监控控制台](https://cms-intl.console.aliyun.com)。
    2.  单击左侧导航栏中**云服务监控**下的**弹性公网IP**，进入弹性公网IP监控列表页面。
    3.  单击实例列表**操作**中的**报警规则**，进入实例的报警规则页面。
    4.  单击右上角的**创建报警规则**，选择资源范围、根据参数设置报警规则，选择通知方式，单击**确认**即可。
-   **参数说明** 

    报警规则参数相关说明，请参见[报警规则参数说明](intl.zh-CN/用户指南/报警服务/报警规则/报警规则参数说明.md#)。


