# DescribeAntChainLatestTransactionV2

查询一条蚂蚁区块链最新的交易摘要列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainLatestTransactionV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainLatestTransactionV2|系统规定参数。取值：DescribeAntChainLatestTransactionV2。 |
|Bizid|String|否|查询一条蚂蚁区块链最新的交易摘要列表（仅适用于阿里云国内站）|区块链ID |
|Start|Long|否|1609084800000|统计开始时间 |
|End|Long|否|1609776000000|统计结束时间 |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Array of Result| |请求结果 |
|Alias|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|CreatTime|Long|1609171200000|创建时间 |
|Dt|Long|1609171200000|时间 |
|LastSumBlockHeight|Long|11511|最后统计的区块高度 |
|TransCount|Long|4|交易总量 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainLatestTransactionV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>22361E12-CF14-4A6F-B932-D817702097CF</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <Dt>1609171200000</Dt>
    <TransCount>4</TransCount>
    <Alias>8bd720bde18c4b37b0f4a1c7834db163</Alias>
    <LastSumBlockHeight>11511</LastSumBlockHeight>
</Result>
<Result>
    <Dt>1609257600000</Dt>
    <TransCount>0</TransCount>
    <Alias>8bd720bde18c4b37b0f4a1c7834db163</Alias>
    <LastSumBlockHeight>40306</LastSumBlockHeight>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "22361E12-CF14-4A6F-B932-D817702097CF",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": [
    {
      "Dt": 1609171200000,
      "TransCount": 4,
      "Alias": "8bd720bde18c4b37b0f4a1c7834db163",
      "LastSumBlockHeight": 11511
    },
    {
      "Dt": 1609257600000,
      "TransCount": 0,
      "Alias": "8bd720bde18c4b37b0f4a1c7834db163",
      "LastSumBlockHeight": 40306
    }
 ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

