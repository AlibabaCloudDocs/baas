# DescribeAntChainQRCodeAuthorizationV2

查询蚂蚁区块链交易二维码授权状态（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainQRCodeAuthorizationV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainQRCodeAuthorizationV2|系统规定参数。取值：DescribeAntChainQRCodeAuthorizationV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|QRCodeType|String|是|MINI\_APP\_BROWSER\_TRANSACTION|二维码类型，当前可以选值为 MINI\_APP\_BROWSER\_TRANSACTION 代表支付宝小程序区块链浏览器。 |
|RegionId|String|否|cn-hangzhou|地域ID（RegionId），限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|返回消息 |
|RequestId|String|980061FC-058D-4298-8598-D9DDB10D0ED4|请求ID |
|Result|Struct| |请求结果 |
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|AuthorizationType|String|ALL\_USER\_AUTHORIZATION|授权类型， 当前可选值为 ALL\_USER\_AUTHORIZATION 代表授权所有用户，SPECIFIC\_USER\_AUTHORIZATION 代表授权部分用户，UNAUTHORIZED 代表未授权 |
|QRCodeType|String|MINI\_APP\_BROWSER\_TRANSACTION|二维码类型，当前可以选值为 MINI\_APP\_BROWSER\_TRANSACTION 代表支付宝小程序区块链浏览器。 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainQRCodeAuthorizationV2
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<RequestId>980061FC-058D-4298-8598-D9DDB10D0ED4</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <AuthorizationType>ALL_USER_AUTHORIZATION</AuthorizationType>
    <QRCodeType>MINI_APP_BROWSER_TRANSACTION</QRCodeType>
</Result>
```

`JSON`格式

```
{
  "RequestId": "980061FC-058D-4298-8598-D9DDB10D0ED4",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "AuthorizationType": "ALL_USER_AUTHORIZATION",
    "QRCodeType": "MINI_APP_BROWSER_TRANSACTION"
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

