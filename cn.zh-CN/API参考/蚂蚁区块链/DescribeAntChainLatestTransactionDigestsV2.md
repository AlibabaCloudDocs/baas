# DescribeAntChainLatestTransactionDigestsV2

查询一条蚂蚁区块链最新的交易摘要列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainLatestTransactionDigestsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainLatestTransactionDigestsV2|系统规定参数。取值：DescribeAntChainLatestTransactionDigestsV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |
|ConsortiumId|String|否|M8GaMEyX|联盟ID |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|List|\[\]|请求结果 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainLatestTransactionDigestsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>C75DDE10-D754-4CB5-9EA8-B6C343CC075C</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <CreateTime>1609987477483</CreateTime>
    <TransactionV10Type>CALL_CONTRACT</TransactionV10Type>
    <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
    <To>e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec</To>
    <Hash>076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2</Hash>
</Result>
<Result>
    <CreateTime>1609847759344</CreateTime>
    <TransactionV10Type>CALL_CONTRACT</TransactionV10Type>
    <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
    <To>e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec</To>
    <Hash>227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061</Hash>
</Result>
<Result>
    <CreateTime>1609227008399</CreateTime>
    <TransactionV10Type>CALL_CONTRACT</TransactionV10Type>
    <From>4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189</From>
    <To>9782291a957d28bec9e02f3dcb27d78392815ede7670b70793e0fd9763309cda</To>
    <Hash>ac73c8fa158436513e0b398632d9a082e04cee3eac6f9fb50087a46d801bdfd1</Hash>
</Result>
<Result>
    <CreateTime>1609226974574</CreateTime>
    <TransactionV10Type>DEPLOY_CONTRACT</TransactionV10Type>
    <From>4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189</From>
    <To>9782291a957d28bec9e02f3dcb27d78392815ede7670b70793e0fd9763309cda</To>
    <Hash>2747c362416ab4c11fafca15bf652c51efb363c1fbdd8c0ed45aa20c56083777</Hash>
</Result>
<Result>
    <CreateTime>1609226512448</CreateTime>
    <TransactionV10Type>CREATE_ACCOUNT</TransactionV10Type>
    <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
    <To>4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189</To>
    <Hash>954eb876a579698f4c09aa12a91e22020ca169e13c711db342d391b0ad233f3f</Hash>
</Result>
<Result>
    <CreateTime>1609223761557</CreateTime>
    <TransactionV10Type>CREATE_ACCOUNT</TransactionV10Type>
    <From>e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b</From>
    <To>b3d4c1bc05776e66e2f080d6a311b2c0667f623db1b65924a8823e31325e8d2c</To>
    <Hash>c3b4b3327731cf0221fbac39cc8816438e0617552ae0948ed3f68ec49a20b639</Hash>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "C75DDE10-D754-4CB5-9EA8-B6C343CC075C",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": [
    {
      "CreateTime": 1609987477483,
      "TransactionV10Type": "CALL_CONTRACT",
      "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
      "To": "e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec",
      "Hash": "076bba1b726b3bcb958cba6fffc03eaa5cbed59320271dcbc0e05648a18a94f2"
    },
    {
      "CreateTime": 1609847759344,
      "TransactionV10Type": "CALL_CONTRACT",
      "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
      "To": "e93372533f323b2f12783aa3a586135cf421486439c2cdcde47411b78f9839ec",
      "Hash": "227072dcd1a5d78098da99ccc8024304b9fb54fc6b65e37ef919d7f2da080061"
    },
    {
      "CreateTime": 1609227008399,
      "TransactionV10Type": "CALL_CONTRACT",
      "From": "4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189",
      "To": "9782291a957d28bec9e02f3dcb27d78392815ede7670b70793e0fd9763309cda",
      "Hash": "ac73c8fa158436513e0b398632d9a082e04cee3eac6f9fb50087a46d801bdfd1"
    },
    {
      "CreateTime": 1609226974574,
      "TransactionV10Type": "DEPLOY_CONTRACT",
      "From": "4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189",
      "To": "9782291a957d28bec9e02f3dcb27d78392815ede7670b70793e0fd9763309cda",
      "Hash": "2747c362416ab4c11fafca15bf652c51efb363c1fbdd8c0ed45aa20c56083777"
    },
    {
      "CreateTime": 1609226512448,
      "TransactionV10Type": "CREATE_ACCOUNT",
      "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
      "To": "4db58ada9221304b161ab0aa11b032a62d60d9ab29e41c6d238f4401c81c8189",
      "Hash": "954eb876a579698f4c09aa12a91e22020ca169e13c711db342d391b0ad233f3f"
    },
    {
      "CreateTime": 1609223761557,
      "TransactionV10Type": "CREATE_ACCOUNT",
      "From": "e7d3e769f3f593dadcb8634cc5b09fc90dd3a61c4a06a79cb0923662fe6fae6b",
      "To": "b3d4c1bc05776e66e2f080d6a311b2c0667f623db1b65924a8823e31325e8d2c",
      "Hash": "c3b4b3327731cf0221fbac39cc8816438e0617552ae0948ed3f68ec49a20b639"
    }
  ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

