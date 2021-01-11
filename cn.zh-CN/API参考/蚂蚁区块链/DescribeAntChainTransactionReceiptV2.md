# DescribeAntChainTransactionReceiptV2

根据交易哈希查询一条蚂蚁区块链的交易回执信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainTransactionReceiptV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainTransactionReceiptV2|系统规定参数。取值：DescribeAntChainTransactionReceiptV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|Hash|String|是|8bd720bde18c4b37b0f4a1c7834db163|交易哈希 |
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
|Data|String|data|Data |
|GasUsed|String|20000|消耗的Gas |
|Logs|List|\[""\]|logs |
|Result|Long|0|结果 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainTransactionReceiptV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>4CE888A8-2232-4091-817F-57C38A432C8B</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <Data>{ "nodes" : [ { "nodeId" : "0x185F7D2745FFB31E43082771A64222E944F125533C8D444B8AB44996D20EAEE5", "endpoints" : [{ "ip" : 143171187, "port" : "18230" }, { "ip" : 143171187, "port" : "18230" } ], "publicKey" : "0x44E20E9", "nodeType" : 1, "nodeState" : 2, "domainName" : "", "nodesACRule" : "" }, { "nodeId" : "0x44E20E9", "endpoints" : [{ "ip" : 143171187, "port" : "18231" }, { "ip" : 143171187, "port" : "18231" } ], "publicKey" : "0x44E20E9", "nodeType" : 1, "nodeState" : 2, "domainName" : "", "nodesACRule" : "" }, { "nodeId" : "0x437BCC0B400878F2F9C11430F37BE0A5FF3939BE9DD9E0F9F4CE854A1B68BBC1", "endpoints" : [{ "ip" : 143171187, "port" : "18232" }, { "ip" : 143171187, "port" : "18232" } ], "publicKey" : "0x44E20E9", "nodeType" : 1, "nodeState" : 2, "domainName" : "", "nodesACRule" : "" }, { "nodeId" : "0x44E20E9", "endpoints" : [{ "ip" : 143171187, "port" : "18233" }, { "ip" : 143171187, "port" : "18233" } ], "publicKey" : "0x44E20E9", "nodeType" : 1, "nodeState" : 2, "domainName" : "", "nodesACRule" : "" } ] }</Data>
    <GasUsed>578648</GasUsed>
    <Logs/>
    <Result>0</Result>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "4CE888A8-2232-4091-817F-57C38A432C8B",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "Data": "{ \"nodes\" : [ { \"nodeId\" : \"0x185F7D2745FFB31E43082771A64222E944F125533C8D444B8AB44996D20EAEE5\", \"endpoints\" : [{ \"ip\" : 143171187, \"port\" : \"18230\" }, { \"ip\" : 143171187, \"port\" : \"18230\" } ], \"publicKey\" : \"0x44E20E9\", \"nodeType\" : 1, \"nodeState\" : 2, \"domainName\" : \"\", \"nodesACRule\" : \"\" }, { \"nodeId\" : \"0x44E20E9\", \"endpoints\" : [{ \"ip\" : 143171187, \"port\" : \"18231\" }, { \"ip\" : 143171187, \"port\" : \"18231\" } ], \"publicKey\" : \"0x44E20E9\", \"nodeType\" : 1, \"nodeState\" : 2, \"domainName\" : \"\", \"nodesACRule\" : \"\" }, { \"nodeId\" : \"0x437BCC0B400878F2F9C11430F37BE0A5FF3939BE9DD9E0F9F4CE854A1B68BBC1\", \"endpoints\" : [{ \"ip\" : 143171187, \"port\" : \"18232\" }, { \"ip\" : 143171187, \"port\" : \"18232\" } ], \"publicKey\" : \"0x44E20E9\", \"nodeType\" : 1, \"nodeState\" : 2, \"domainName\" : \"\", \"nodesACRule\" : \"\" }, { \"nodeId\" : \"0x44E20E9\", \"endpoints\" : [{ \"ip\" : 143171187, \"port\" : \"18233\" }, { \"ip\" : 143171187, \"port\" : \"18233\" } ], \"publicKey\" : \"0x44E20E9\", \"nodeType\" : 1, \"nodeState\" : 2, \"domainName\" : \"\", \"nodesACRule\" : \"\" } ] }",
    "GasUsed": "578648",
    "Logs": [
      ""
    ],
    "Result": 0
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

