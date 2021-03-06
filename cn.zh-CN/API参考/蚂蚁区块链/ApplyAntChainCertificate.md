# ApplyAntChainCertificate {#doc_api_Baas_ApplyAntChainCertificate .reference}

申请链接一条蚂蚁区块链，上传tls证书请求

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=ApplyAntChainCertificate&type=RPC&version=2018-12-21)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|AntChainId|String|是|bDXK6boZ|区块链ID

 |
|UploadReq|String|是|LS0tLS1...|上传内容

 |
|Action|String|否|ApplyAntChainCertificate|系统规定参数。取值：ApplyAntChainCertificate。

 |
|RegionId|String|否|cn-hangzhou|地域ID

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|D3FB9E67-0E31-4B8B-8895-3660CCE8CA62|请求ID

 |
|Result|String|success|请求结果

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ApplyAntChainCertificate
&<公共请求参数>

```

正常返回示例

`JSON` 格式

``` {#json_return_success_demo}
{
	"successResponse":true,
	"requestId":"D3FB9E67-0E31-4B8B-8895-3660CCE8CA62",
	"data":{
		"Result":"success",
		"RequestId":"D3FB9E67-0E31-4B8B-8895-3660CCE8CA62"
	},
	"code":"200"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

