# DescribeAntChainLatestBlocksV2

查询一条蚂蚁区块链最新的区块信息列表（仅适用于阿里云国内站

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainLatestBlocksV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainLatestBlocksV2|系统规定参数。取值：DescribeAntChainLatestBlocksV2。 |
|AntChainId|String|是|查询一条蚂蚁区块链最新的区块信息列表（仅适用于阿里云国内站|区块链ID |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |
|ConsortiumId|String|否|M8GaMEyX|联盟ID |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Array of Result| |请求结果 |
|Alias|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|BizData|String|b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5|区块哈希 |
|BlockHash|String|b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5|区块哈希 |
|CreateTime|Long|1610002621000|创建时间 |
|Height|Long|259808|区块高度 |
|PreviousHash|String|f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f|上一个区块哈希 |
|RootTxHash|String|0000000000000000000000000000000000000000000000000000000000000000|根哈希 |
|Size|Long|1024|区块大小 |
|TransactionSize|Long|0|区块中交易数量 |
|Version|Long|33556226|版本信息 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainLatestBlocksV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>5479D9A8-F0ED-4751-A52C-C5B02C65D8B6</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <BizData>b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5</BizData>
    <TransactionSize>0</TransactionSize>
    <Version>33556226</Version>
    <Alias>8bd720bde18c4b37b0f4a1c7834db163</Alias>
    <BlockHash>b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5</BlockHash>
    <Size>1024</Size>
    <CreateTime>1610002621000</CreateTime>
    <PreviousHash>f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f</PreviousHash>
    <Height>259808</Height>
    <RootTxHash>0000000000000000000000000000000000000000000000000000000000000000    0000000000000000000000000000000000000000000000000000000000000000    c1e9582dec94334b5b11ecb0c173b8350f2a125b28d81216a58235450e6c0c73</RootTxHash>
</Result>
<Result>
    <BizData>f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f</BizData>
    <TransactionSize>0</TransactionSize>
    <Version>33556226</Version>
    <Alias>8bd720bde18c4b37b0f4a1c7834db163</Alias>
    <BlockHash>f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f</BlockHash>
    <Size>1024</Size>
    <CreateTime>1610002618000</CreateTime>
    <PreviousHash>02350b3b09ad38042a86b4f8a385590358434f0193be5d3a40a423f1ad7bef98</PreviousHash>
    <Height>259807</Height>
    <RootTxHash>0000000000000000000000000000000000000000000000000000000000000000    0000000000000000000000000000000000000000000000000000000000000000    c1e9582dec94334b5b11ecb0c173b8350f2a125b28d81216a58235450e6c0c73</RootTxHash>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "5479D9A8-F0ED-4751-A52C-C5B02C65D8B6",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": [
    {
      "BizData": "b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5",
      "TransactionSize": 0,
      "Version": 33556226,
      "Alias": "8bd720bde18c4b37b0f4a1c7834db163",
      "BlockHash": "b21baa257788d97eb0006672ccc5008f465365e1dec88d0bbd833e150414b3d5",
      "Size": 1024,
      "CreateTime": 1610002621000,
      "PreviousHash": "f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f",
      "Height": 259808,
      "RootTxHash": "0000000000000000000000000000000000000000000000000000000000000000    0000000000000000000000000000000000000000000000000000000000000000    c1e9582dec94334b5b11ecb0c173b8350f2a125b28d81216a58235450e6c0c73"
    },
    {
      "BizData": "f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f",
      "TransactionSize": 0,
      "Version": 33556226,
      "Alias": "8bd720bde18c4b37b0f4a1c7834db163",
      "BlockHash": "f208834bdc72bd6bb05c5ef1a35abbc8295a16deda9526b7b78c69ec24591b9f",
      "Size": 1024,
      "CreateTime": 1610002618000,
      "PreviousHash": "02350b3b09ad38042a86b4f8a385590358434f0193be5d3a40a423f1ad7bef98",
      "Height": 259807,
      "RootTxHash": "0000000000000000000000000000000000000000000000000000000000000000    0000000000000000000000000000000000000000000000000000000000000000    c1e9582dec94334b5b11ecb0c173b8350f2a125b28d81216a58235450e6c0c73"
    }
  ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

