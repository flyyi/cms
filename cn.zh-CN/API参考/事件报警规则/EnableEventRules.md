# EnableEventRules {#doc_api_Cms_EnableEventRules .reference}

启用一个或者多个事件监控报警规则。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=EnableEventRules&type=RPC&version=2019-01-01)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|EnableEventRules|系统规定参数。取值：EnableEventRules。

 |
|RuleNames.N|RepeatList|是|ruleName1|报警规则名称。N 的取值范围为 1~20。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码，200表示成功。

 |
|Message|String|success|错误信息。

 |
|RequestId|String|20F2896A-6684-4A04-8255-4155B1593C70|请求ID，用于排查问题。

 |
|Success|Boolean|true|是否成功。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=EnableEventRules
&RuleNames.1=ruleName1
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<EnableEventRulesResponse>
      <RequestId>20F2896A-6684-4A04-8255-4155B1593C70</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</EnableEventRulesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"20F2896A-6684-4A04-8255-4155B1593C70",
	"Success":true,
	"Code":"200"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

