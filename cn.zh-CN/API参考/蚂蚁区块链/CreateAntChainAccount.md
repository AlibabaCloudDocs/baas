# CreateAntChainAccount {#doc_api_Baas_CreateAntChainAccount .reference}

在一条蚂蚁区块链上创建一个账户

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=CreateAntChainAccount&type=RPC&version=2018-12-21)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Account|String|是|test|账号名

 |
|AccountPubKey|String|是|AEDC32...|账户公钥

 |
|AccountRecoverPubKey|String|是|AEDC32...|账户恢复公钥

 |
|AntChainId|String|是|bDXK6boZ|区块链ID

 |
|Action|String|否|CreateAntChainAccount|系统规定参数。取值：CreateAntChainAccount。

 |
|RegionId|String|否|cn-hangzhou|地域ID

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0301F6CB-4FA6-4D03-8668-963623B63D0F|请求ID

 |
|Result| | |请求结果

 |
|Account|String|test|账户名

 |
|AntChainId|String|bDXK6boZ|区块链ID

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateAntChainAccount
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"successResponse":true,
	"requestId":"0301F6CB-4FA6-4D03-8668-963623B63D0F",
	"data":{
		"Result":{
			"Account":"test",
			"AntChainId":"bDXK6boZ"
		},
		"RequestId":"0301F6CB-4FA6-4D03-8668-963623B63D0F"
	},
	"code":"200"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

