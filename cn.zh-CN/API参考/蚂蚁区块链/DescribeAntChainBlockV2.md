# DescribeAntChainBlockV2

根据块高查询一条蚂蚁区块链的区块信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainBlockV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainBlockV2|系统规定参数。取值：DescribeAntChainBlockV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|Height|Long|是|100|区块高度 |
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
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|BlockHash|String|5abf96debc87f1b64dcbaf4fa57fd46f2a06acdb5de0ba91ef9718d81aebafc7|区块哈希 |
|CreateTime|Long|1609223363570|创建时间 |
|Height|Integer|254761|区块高度 |
|PreviousHash|String|2444ef0617e0c6845549dead70f118c5a58f03c04575ecb79e283ab5c34b491d|前一个区块链哈希 |
|RootTxHash|String|0000000000000000000000000000000000000000000000000000000000000000|根交易哈希 |
|TransSummaryList|Array of TransSummaryList| |交易列表 |
|Alias|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|BlockHash|String|5abf96debc87f1b64dcbaf4fa57fd46f2a06acdb5de0ba91ef9718d81aebafc7|区块Hash |
|Category|Integer|-1|分类 |
|CreateTime|Long|1609223363570|创建时间 |
|From|String|e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b|源地址 |
|GasUsed|Long|4000000|Gas使用值 |
|Hash|String|076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2|交易Hash |
|Height|Long|254761|区块高度 |
|ReferenceCount|Integer|0|数值 |
|To|String|e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec|目的地址 |
|TransTypeV10|String|CALL\_CONTRACT|合约链类型 |
|TransTypeV6|String|""|存证链类型 |
|TransactionSize|Integer|1|交易数 |
|Version|Long|1|区块版本 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainBlockV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>3C9D2C34-70F1-4E24-9276-42A16A06205D</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
    <TransactionSize>1</TransactionSize>
    <BlockHash>b19463f765d36e7531d78e53dbafef28d438bfbf628a4b0b83dead9d28e24f72</BlockHash>
    <CreateTime>1609987477500</CreateTime>
    <PreviousHash>1f31b85ceef5a12d6ee7a5290d385130c8bd09d8fda9a6109bb81c241c91c1db</PreviousHash>
    <Height>254761</Height>
    <TransSummaryList>
        <TransTypeV10>CALL_CONTRACT</TransTypeV10>
        <Category>-1</Category>
        <Alias>8bd720bde18c4b37b0f4a1c7834db163</Alias>
        <BlockHash>b19463f765d36e7531d78e53dbafef28d438bfbf628a4b0b83dead9d28e24f72</BlockHash>
        <CreateTime>1609987477483</CreateTime>
        <Height>254761</Height>
        <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
        <GasUsed>4000000</GasUsed>
        <To>e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec</To>
        <Hash>076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2</Hash>
        <ReferenceCount>0</ReferenceCount>
    </TransSummaryList>
    <RootTxHash>076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2</RootTxHash>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "3C9D2C34-70F1-4E24-9276-42A16A06205D",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
    "TransactionSize": 1,
    "BlockHash": "b19463f765d36e7531d78e53dbafef28d438bfbf628a4b0b83dead9d28e24f72",
    "CreateTime": 1609987477500,
    "PreviousHash": "1f31b85ceef5a12d6ee7a5290d385130c8bd09d8fda9a6109bb81c241c91c1db",
    "Height": 254761,
    "TransSummaryList": [
      {
        "TransTypeV10": "CALL_CONTRACT",
        "Category": -1,
        "Alias": "8bd720bde18c4b37b0f4a1c7834db163",
        "BlockHash": "b19463f765d36e7531d78e53dbafef28d438bfbf628a4b0b83dead9d28e24f72",
        "CreateTime": 1609987477483,
        "Height": 254761,
        "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
        "GasUsed": 4000000,
        "To": "e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec",
        "Hash": "076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2",
        "ReferenceCount": 0
      }
    ],
    "RootTxHash": "076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2"
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

