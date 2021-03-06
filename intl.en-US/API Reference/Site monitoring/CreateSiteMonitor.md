# CreateSiteMonitor {#doc_api_Cms_CreateSiteMonitor .reference}

You can call this operation to create a site monitoring task.

Currently, site monitoring supports the following protocols: HTTP, Ping, TCP, UDP, DNS, SMTP, POP3, and FTP. Each protocol has a specific set of extended options specified by the OptionsJson parameter. The following tables list the extended options supported for each protocol.

 **HTTP** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| http\_method

 | String

 | The HTTP method. The following HTTP methods are supported: GET, POST, and HEAD. Default value: GET.

 |
| header

 | String

 | The user-defined HTTP headers. Separate the headers with line breaks \("\\n"\). The format of the header in each line must meet the requirement of the HTTP protocol, that is, the header name and value must be separated by a colon \(:\).

 |
| cookie

 | String

 | The HTTP cookie. Set this parameter in compliance with the HTTP request standard.

 |
| request\_content

 | String

 | The content of the request. The content can be in JSON or form format. If this parameter is not specified, the request has no body.

 |
| response\_content

 | String

 | The expected or unexpected content of the response. The first 64 KB of the content returned from the HTTP server will be checked in the monitoring process.

 |
| match\_rule

 | String

 | The match rule. A value of 0 indicates that the monitoring is successful if the response does not contain the content specified by the response\_content parameter. A value of 1 indicates that the monitoring is successful if the response contains the content specified by the response\_content parameter.

 |
| username

 | String

 | The username used to authenticate the HTTP request. If this parameter is specified, the HTTP request will contain the basic authentication header.

 |
| password

 | String

 | The password used to authenticate the HTTP request.

 |
| time\_out

 | Integer

 | The timeout value. Unit: milliseconds. Default value: 5000.

 |
| max\_redirect

 | Integer

 | The maximum number of redirects. The default value is 5 for an ECS detection point and 2 for a carrier detection point. Set this parameter to 0 to disable redirection. Valid values: 0 to 50.

 |

 **Ping** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| failure\_rate

 | Integer

 | The failure rate threshold. If the failure rate exceeds this value, the monitoring fails and the error 610 \(PingAllFail\) or 615 \(PingPartialFail\) is returned. Default value: 0.1.

 |
| ping\_num

 | Integer

 | The number of times that the target URL or IP address is pinged. Default value: 20. Valid values: 1 to 100.

 |

 **DNS** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| dns\_server

 | String

 | The domain name or IP address of the DNS server.

 |
| dns\_type

 | String

 | The type of DNS records to query. Valid values: A, NS, CNAME, MX, TXT, and ANY.

 |
| expect\_value

 | String

 | The list of expected values. Separate the expected values with spaces.

 |
| match\_rule

 | String

 | The relationship between the expected value list and the returned DNS record list. If the two lists do not meet the specified relationship, the monitoring fails.

 Empty string or IN\_DNS: The expected value list is a subset of the returned DNS record list.

 DNS\_IN: The returned DNS record list is a subset of the expected value list.

 EQUAL: The returned DNS record list is identical with the expected value list.

 ANY: The returned DNS record list intersects with the expected value list.

 |

 **FTP** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| port

 | Integer

 | The port number of the FTP server. If this parameter is not specified, the default port number is used. The default port number is 21 for FTP and 990 for FTPS.

 |
| username

 | String

 | The username used to log on to the FTP server. If this parameter is not specified, anonymous logon is used. The username and password for anonymous logon are anonymous and ftp@example.com.

 |
| password

 | String

 | The password used to log on to the FTP server.

 |

 **POP3 or SMTP** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| port

 | Integer

 | The port number of the POP3 server. The default port number is 110 for POP3 and 995 for POP3S.

 |
| username

 | String

 | The username used to log on to the server.

 |
| password

 | String

 | The password used to log on to the server.

 |

 **TCP or UDP** 

| Parameter

 | Type

 | Description

 |
|-------------|--------|---------------|
| port

 | Integer

 | The TCP or UDP port number to monitor.

 |
| request\_content

 | String

 | The content of the request. If the value of the request\_format parameter is hex, the value of the request\_content parameter must be in hexadecimal format.

 |
| request\_format

 | String

 | The format of the request content. If the value of the request\_format parameter is not hex, the value of the request\_content parameter will be sent to the server as common text.

 |
| response\_content

 | String

 | The expected content of the response. If the response of the server does not contain the content specified by the response\_content parameter, the monitoring fails. If the value of the response\_format parameter is hex, the value of the response\_content parameter must be in hexadecimal format. If the value of the response\_format parameter is not hex, the value of the response\_content parameter is interpreted as common text.

 |

## Debugging {#apiExplorer .section}

Alibaba Cloud provides OpenAPI Explorer to simplify API usage. You can use [OpenAPI Explorer](https://api.aliyun.com/#product=Cms&api=CreateSiteMonitor) to search for APIs, call APIs, and dynamically generate SDK example code.

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateSiteMonitor| The operation that you want to perform. Set this parameter to CreateSiteMonitor.

 |
|Address|String|Yes|http://www.aliyun.com| The URL or IP address monitored by the site monitoring task.

 |
|TaskName|String|Yes|Website monitoring| The name of the site monitoring task. The name must be 4 to 100 characters in length. The name can contain the following types of characters: letters, digits, and underscores.

 |
|TaskType|String|Yes|HTTP| The protocol of the site monitoring task. Currently, site monitoring supports the following protocols: HTTP, Ping, TCP, UDP, DNS, SMTP, POP3, and FTP.

 |
|AlertIds|String|No|49f7c317-7645-4cc9-94fd-ea42e122\*\*\*\*| The IDs of existing alert rules to be associated with the site monitoring task.

 |
|Interval|String|No|1| The monitoring interval of the site monitoring task. Unit: minutes. Valid values: 1, 5, and 15. Default value: 1.

 |
|IspCities|String|No|\[\{"city":"546","isp":"465"\},\{"city":"572","isp":"465"\},\{"city":"738","isp":"465"\}\]| The detection points in a JSON array. For example, `[{"city":"546","isp":"465"},{"city":"572","isp":"465"},{"city":"738","isp":"465"}]` indicates the detection points in Beijing, Hangzhou, and Qingdao respectively.

 You can call the DescribeISPAreaCity operation to query detection point information. If this parameter is not specified, three detection points will be chosen randomly for monitoring.

 |
|OptionsJson|String|No|\{"time\_out":5000\}| The extended options of the protocol of the site monitoring task. The options vary according to the protocol.

 |

Each protocol has a specific set of extended options specified by the OptionsJson parameter. For example, the OptionsJson parameter can be set to the following value for DNS:

`{ "dns_server":"8.8.8.8" }`

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AlertRule|String|\[\{"alarmActions":\["Default alert group"\],"metricName":"Availability","expression":"$Availability<96"\}\]| The alert rule that was set for the site monitoring task when it was created or modified. The value is a JSON array in the following format:

 `[{"alarmActions":["xxx"],"metricName":"Availability","expression":"$Availability<96"}]`.

 The alarmActions field indicates the alert group to which alert notifications are sent. The metricName field indicates the metric. The value of the metricName field can be Availability \(indicating the percentage of available detection points\) or AvailableNumber \(indicating the number of available detection points\).

 |
|Code|String|200| The status code. A value of 200 indicates that the call was successful.

 |
|Data| | | The result of creating the site monitoring task.

 |
|└AttachAlertResult| | | The result of associating the site monitoring task with existing alert rules.

 |
|└Code|String|200| The status code. A value of 200 indicates that site monitoring task was associated with the existing alert rule.

 |
|└Message|String|success| The error message about the association of the site monitoring task with the existing alert rule.

 |
|└RequestId|String|32565d-233-1b98-2231-892813f86c71| The ID of the request for associating the site monitoring task with the existing alert rule.

 |
|└RuleId|String|ruleId12345| The ID of the existing alert rule that was associated with the site monitoring task.

 |
|└Success|String|true| Indicates whether the site monitoring task was associated with the existing alert rule.

 |
|Message|String|successful| The error message.

 |
|RequestId|String|68192f5d-0d45-4b98-9724-892813f86c71| The ID of the request.

 |
|Success|String|true| Indicates whether the call was successful.

 |

## Examples {#demo .section}

Sample request

``` {#request_demo}

http(s)://[Endpoint]/? Action=CreateSiteMonitor
&Address=http://www.aliyun.com
&TaskName=Website monitoring
&TaskType=HTTP
&<Common request parameters>

```

Sample success response

`XML` format

``` {#xml_return_success_demo}
<CreateSiteMonitorResponse>
  <RequestId>04F0F334-1335-436C-A1D7-6C044FE73368</RequestId>
  <Success>true</Success>
  <Code>200</Code>
  <Message>successful</Message>
</CreateSiteMonitorResponse>

```

`JSON` format

``` {#json_return_success_demo}
{
	"Message":"successful",
	"Success":true,
	"Code":"200"
}
```

## Error codes {#section_xz6_ftx_8yr .section}

[View error codes.](https://error-center.aliyun.com/status/product/Cms)

