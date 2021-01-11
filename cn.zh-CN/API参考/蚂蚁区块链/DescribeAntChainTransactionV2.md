# DescribeAntChainTransactionV2

根据交易哈希查询一条蚂蚁区块链的交易信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainTransactionV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainTransactionV2|系统规定参数。取值：DescribeAntChainTransactionV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|Hash|String|是|227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061|交易哈希 |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |
|ConsortiumId|String|否|M8GaMEyX|联盟ID |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Struct| |请求结果 |
|BlockHash|String|1168bc5dd0b78d15446b15ea5a7f7822a7d07c007dd3a50becf98da220fc08f6|区块哈希 |
|BlockHeight|Long|100|区块高度 |
|BlockVersion|String|10|区块版本 |
|CreateTime|Long|1563954336850|交易创建时间 |
|Hash|String|b3b0d2db83d3e670449d1e2a39d1d13b7e0e6080b0f9c6945f79eca68d1dd2ca|交易哈希 |
|Transaction|Struct| |交易详情 |
|Data|String|""|数据 |
|Extentions|List|\[\]|扩展信息 |
|From|String|e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b|交易发送者哈希 |
|Gas|String|4000000|Gas值 |
|Hash|String|b3b0d2db83d3e670449d1e2a39d1d13b7e0e6080b0f9c6945f79eca68d1dd2ca|交易哈希 |
|Nonce|String|5675407026657953619|交易Nonce |
|Period|Long|1563954336850|Period |
|Signatures|List|5s6JhauIqAlMb6d+7...|签名 |
|Timestamp|Long|1563954336850|交易发送时戳 |
|To|String|961085f3c7ef705ad587d0cbe11d7863a5a11af7451f4e9b1edadd74402addf5|交易接收方地址 |
|TxType|String|UNFREEZE\_ACCOUNT\_CONTRACT|交易类型 |
|Value|String|0|交易金额 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainTransactionV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>D24DB224-51AC-476A-8222-DE316A1F1AB2</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <Transaction>
        <Period>1609847759344</Period>
        <Data>0n3wLA==</Data>
        <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
        <To>e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec</To>
        <Hash>227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061</Hash>
        <Signatures>4+oLPVkm2QuZm6Vm8fLiwtQ8w4HIGsimL6zqBTPH6k9MabbTympeUlaZT2NIulkrRRaTbzC3rqr/kQS3MLVMBwA=</Signatures>
        <Signatures>JhnOJFNhIYxwaNCpiScFJJRemrP4vyPjW3h/otm1ChgvTrK8vMD+vfE6BstI3MP1yqkW6DclUY7vqbXGATtlfgE=</Signatures>
        <Signatures>jH9q1A6aSxvgVLHgoEyM+LvYXQTi2aT5s94NkGewz9ArsgRu0BquJVIgkeaZzo75U7Tj+z18Kq0eksuiBX0RTAA=</Signatures>
        <Signatures>9y09fd+a5P/kitDkD8PvQd5dp6egnjZzUoSZZMPPyqh+uSCE2ZSCce1DqkJ+de/U8lTZZuh5LSFGy6ii9sgLTQA=</Signatures>
        <Timestamp>1609847759344</Timestamp>
    </Transaction>
    <BlockHash>83b2e08a5acdaf3106e88f9586b6241e513f9261e400989384fec135c5508c80</BlockHash>
    <CreateTime>1609847759344</CreateTime>
    <Hash>227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061</Hash>
    <BlockHeight>208196</BlockHeight>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "D24DB224-51AC-476A-8222-DE316A1F1AB2",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "Transaction": {
      "Extentions": [],
      "Period": 1609847759344,
      "Data": "0n3wLA==",
      "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
      "To": "e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec",
      "Hash": "227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061",
      "Signatures": [
        "4+oLPVkm2QuZm6Vm8fLiwtQ8w4HIGsimL6zqBTPH6k9MabbTympeUlaZT2NIulkrRRaTbzC3rqr/kQS3MLVMBwA=",
        "JhnOJFNhIYxwaNCpiScFJJRemrP4vyPjW3h/otm1ChgvTrK8vMD+vfE6BstI3MP1yqkW6DclUY7vqbXGATtlfgE=",
        "jH9q1A6aSxvgVLHgoEyM+LvYXQTi2aT5s94NkGewz9ArsgRu0BquJVIgkeaZzo75U7Tj+z18Kq0eksuiBX0RTAA=",
        "9y09fd+a5P/kitDkD8PvQd5dp6egnjZzUoSZZMPPyqh+uSCE2ZSCce1DqkJ+de/U8lTZZuh5LSFGy6ii9sgLTQA="
      ],
      "Timestamp": 1609847759344
    },
    "BlockHash": "83b2e08a5acdaf3106e88f9586b6241e513f9261e400989384fec135c5508c80",
    "CreateTime": 1609847759344,
    "Hash": "227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061",
    "BlockHeight": 208196
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

