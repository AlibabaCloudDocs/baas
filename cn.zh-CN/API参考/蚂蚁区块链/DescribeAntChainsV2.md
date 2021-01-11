# DescribeAntChainsV2

获取联盟内的蚂蚁区块链列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainsV2|系统规定参数。取值：DescribeAntChainsV2。 |
|ConsortiumId|String|是|M8GaMEyX|联盟ID |
|PageNumber|Integer|是|1|分页号 |
|PageSize|Integer|是|10|分页大小 |
|RegionId|String|否|cn-hangzhou|区域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|DBD6C69E-22B9-419E-B072-7A715F3AA330|请求ID |
|Result|Struct| |请求结果 |
|AntChains|Array of AntChains| |区块链信息 |
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|AntChainName|String|专业链|区块链名称 |
|ChainType|String|Contract|区块链的类型 |
|CipherSuit|String|classic|加密套件类型 |
|CreateTime|Long|1609221924000|创建时间 |
|ExpireTime|Long|1672329600000|过期时间 |
|InstanceId|String|ALIYUN202012291405173265824745109|实例ID |
|IsAdmin|Boolean|false|是否为管理员 |
|MemberStatus|String|ChainApplied|成员状态 |
|MerkleTreeSuit|String|fdmt|Merkle树类型 |
|MonitorStatus|Boolean|true|监控状态 |
|Network|String|Running|网络信息 |
|NodeNum|Integer|4|节点数量 |
|RegionId|String|cn-hangzhou|区域信息 |
|ResourceSize|String|Basic|资源类型 |
|RestStatus|String|CREATE|Rest状态 |
|TlsAlgo|String|rsa|TLS加密算法 |
|Version|String|2.19.1|详细版本 |
|IsExist|Boolean|true|是否存在 |
|Pagination|Struct| |分页信息 |
|PageNumber|Integer|1|分页号 |
|PageSize|Integer|10|分页大小 |
|TotalCount|Integer|2|总数 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果信息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>DBD6C69E-22B9-419E-B072-7A715F3AA330</RequestId>
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
    <AntChains>
        <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
        <IsAdmin>false</IsAdmin>
        <AntChainName>专业链续费064</AntChainName>
        <NodeNum>4</NodeNum>
        <TlsAlgo>rsa</TlsAlgo>
        <CipherSuit>classic</CipherSuit>
        <InstanceId>ALIYUN202012291405173265824745109</InstanceId>
        <CreateTime>1609221924000</CreateTime>
        <ResourceSize>Basic</ResourceSize>
        <RestStatus>CREATE</RestStatus>
        <Version>2.19.1</Version>
        <Network>Running</Network>
        <ChainType>Contract</ChainType>
        <RegionId>cn-hangzhou</RegionId>
        <MerkleTreeSuit>fdmt</MerkleTreeSuit>
        <MemberStatus>ChainApplied</MemberStatus>
        <ExpireTime>1672329600000</ExpireTime>
        <MonitorStatus>true</MonitorStatus>
    </AntChains>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "DBD6C69E-22B9-419E-B072-7A715F3AA330",
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
    "AntChains": [
      {
        "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
        "IsAdmin": false,
        "AntChainName": "专业链续费064",
        "NodeNum": 4,
        "TlsAlgo": "rsa",
        "CipherSuit": "classic",
        "InstanceId": "ALIYUN202012291405173265824745109",
        "CreateTime": 1609221924000,
        "ResourceSize": "Basic",
        "RestStatus": "CREATE",
        "Version": "2.19.1",
        "Network": "Running",
        "ChainType": "Contract",
        "RegionId": "cn-hangzhou",
        "MerkleTreeSuit": "fdmt",
        "MemberStatus": "ChainApplied",
        "ExpireTime": 1672329600000,
        "MonitorStatus": true
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

