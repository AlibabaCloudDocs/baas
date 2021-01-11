# DescribeAntChainMiniAppBrowserQRCodeAccessLogV2

查询蚂蚁区块链的交易二维码支付宝端扫码统计信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainMiniAppBrowserQRCodeAccessLogV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainMiniAppBrowserQRCodeAccessLogV2|系统规定参数。取值：DescribeAntChainMiniAppBrowserQRCodeAccessLogV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|QRCodeType|String|是|MINI\_APP\_BROWSER\_TRANSACTION|二维码类型，当前可以选值为 MINI\_APP\_BROWSER\_TRANSACTION 代表支付宝小程序区块链浏览器。 |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Struct| |请求结果 |
|AccessAlipayAccountCount|Long|10|总查询账号数 |
|AccessCount|Long|100|总查询次数 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainMiniAppBrowserQRCodeAccessLogV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>9DE96CA9-12E8-4758-A244-CCBC388593F8</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <AccessAlipayAccountCount>10</AccessAlipayAccountCount>
    <AccessCount>100</AccessCount>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "9DE96CA9-12E8-4758-A244-CCBC388593F8",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "AccessAlipayAccountCount": 10,
    "AccessCount": 100
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

