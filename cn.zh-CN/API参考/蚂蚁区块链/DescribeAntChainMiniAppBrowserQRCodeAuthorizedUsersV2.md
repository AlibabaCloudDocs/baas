# DescribeAntChainMiniAppBrowserQRCodeAuthorizedUsersV2

查询蚂蚁区块链的交易二维码授权扫码用户列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainMiniAppBrowserQRCodeAuthorizedUsersV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainMiniAppBrowserQRCodeAuthorizedUsersV2|系统规定参数。取值：DescribeAntChainMiniAppBrowserQRCodeAuthorizedUsersV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|PageNumber|Integer|是|1|页面编号，从1开始 |
|PageSize|Integer|是|10|每页显示条例数 |
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
|AntChainId|String|4505A1E4-0EDD-4A02-A4D7-B49219328D49|区块链ID |
|AuthorizationType|String|SPECIFIC\_USER\_AUTHORIZATION|授权类型， 当前可选值 为 ALL\_USER\_AUTHORIZATION 代表授权所有用户，SPECIFIC\_USER\_AUTHORIZATION 代表授权部分用户，UNAUTHORIZED 代表未授权 |
|AuthorizedUserList|Array of AuthorizedUserList| |授权用户列表 |
|GmtAuthorized|String|2021-01-07 10:55:42|授权时间 |
|Phone|String|13800138011|被授权手机号 |
|Pagination|Struct| |分页情况 |
|PageNumber|Integer|1|页面编号，从1开始 |
|PageSize|Integer|10|每页显示条例数 |
|TotalCount|Integer|100|总授权用户数 |
|QRCodeType|String|MINI\_APP\_BROWSER\_TRANSACTION|二维码类型，当前可以选值为 MINI\_APP\_BROWSER\_TRANSACTION 代表支付宝小程序区块链浏览器。 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainMiniAppBrowserQRCodeAuthorizedUsersV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>4505A1E4-0EDD-4A02-A4D7-B49219328D49</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <Pagination>
        <TotalCount>1</TotalCount>
        <PageSize>10</PageSize>
        <PageNumber>1</PageNumber>
    </Pagination>
    <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
    <AuthorizedUserList>
        <GmtAuthorized>2021-01-07 10:55:42.0</GmtAuthorized>
        <Phone>135XXXXXXXX</Phone>
    </AuthorizedUserList>
    <AuthorizationType>SPECIFIC_USER_AUTHORIZATION</AuthorizationType>
    <QRCodeType>MINI_APP_BROWSER_TRANSACTION</QRCodeType>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "4505A1E4-0EDD-4A02-A4D7-B49219328D49",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "Pagination": {
      "TotalCount": 1,
      "PageSize": 10,
      "PageNumber": 1
    },
    "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
    "AuthorizedUserList": [
      {
        "GmtAuthorized": "2021-01-07 10:55:42.0",
        "Phone": "135XXXXXXXX"
      }
    ],
    "AuthorizationType": "SPECIFIC_USER_AUTHORIZATION",
    "QRCodeType": "MINI_APP_BROWSER_TRANSACTION"
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

