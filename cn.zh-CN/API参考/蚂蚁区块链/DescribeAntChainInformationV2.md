# DescribeAntChainInformationV2

查询一条蚂蚁区块链的基本信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainInformationV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainInformationV2|系统规定参数。取值：DescribeAntChainInformationV2。 |
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
|Result|Struct| |请求结果 |
|AbnormalNodes|Integer|0|异常节点数 |
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|BlockHeight|Integer|259988|区块链高度 |
|CreateTime|Long|1609221924000|创建时戳 |
|IsRole|Boolean|false| |
|NodeInfos|Array of NodeInfos| |节点信息 |
|BlockHeight|Long|259988|区块链高度 |
|NodeName|String|8.136.158.115 18130|节点地址 |
|Status|Boolean|true|节点状态 |
|Version|String|0.10|运行版本 |
|NodeNumber|Integer|4|节点总数 |
|Normal|Boolean|true|运行状态 |
|TransactionSum|Integer|6|交易总数 |
|Version|String|0.10|区块链版本 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainInformationV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>E26BACC1-9F8B-40AB-B560-4A834FE4F02A</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
    <Version>0.10</Version>
    <CreateTime>1609221924000</CreateTime>
    <AbnormalNodes>0</AbnormalNodes>
    <Normal>true</Normal>
    <IsRole>false</IsRole>
    <NodeNumber>4</NodeNumber>
    <BlockHeight>259988</BlockHeight>
    <NodeInfos>
        <Status>true</Status>
        <NodeName>8.136.158.115 18130</NodeName>
        <Version>0.10</Version>
        <BlockHeight>259988</BlockHeight>
    </NodeInfos>
    <NodeInfos>
        <Status>true</Status>
        <NodeName>8.136.158.115 18131</NodeName>
        <Version>0.10</Version>
        <BlockHeight>259988</BlockHeight>
    </NodeInfos>
    <NodeInfos>
        <Status>true</Status>
        <NodeName>8.136.158.115 18132</NodeName>
        <Version>0.10</Version>
        <BlockHeight>259988</BlockHeight>
    </NodeInfos>
    <NodeInfos>
        <Status>true</Status>
        <NodeName>8.136.158.115 18133</NodeName>
        <Version>0.10</Version>
        <BlockHeight>259988</BlockHeight>
    </NodeInfos>
    <TransactionSum>6</TransactionSum>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "E26BACC1-9F8B-40AB-B560-4A834FE4F02A",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
    "Version": "0.10",
    "CreateTime": 1609221924000,
    "AbnormalNodes": 0,
    "Normal": true,
    "IsRole": false,
    "NodeNumber": 4,
    "BlockHeight": 259988,
    "NodeInfos": [
      {
        "Status": true,
        "NodeName": "8.136.158.115 18130",
        "Version": "0.10",
        "BlockHeight": 259988
      },
      {
        "Status": true,
        "NodeName": "8.136.158.115 18131",
        "Version": "0.10",
        "BlockHeight": 259988
      },
      {
        "Status": true,
        "NodeName": "8.136.158.115 18132",
        "Version": "0.10",
        "BlockHeight": 259988
      },
      {
        "Status": true,
        "NodeName": "8.136.158.115 18133",
        "Version": "0.10",
        "BlockHeight": 259988
      }
    ],
    "TransactionSum": 6
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

