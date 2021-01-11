# DescribeAntChainContractProjectsV2

获取联盟内合约工程的列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainContractProjectsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainContractProjectsV2|系统规定参数。取值：DescribeAntChainContractProjectsV2。 |
|ConsortiumId|String|是|M8GaMEyX|联盟ID |
|PageNumber|Integer|是|1|页面编号，从1开始 |
|PageSize|Integer|是|10|每页数量 |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Struct| |请求结果 |
|ContractProjects|Array of ContractProjects| |合约工程 |
|ConsortiumId|String|M8GaMEyX|联盟ID |
|CreateTime|Long|1609848383000|创建时间 |
|ProjectDescription|String|test|工程描述 |
|ProjectId|String|RXwQj6m8|工程ID |
|ProjectName|String|test|工程名称 |
|ProjectVersion|String|1.0.0|工程版本 |
|UpdateTime|Long|1609848383000|更新时间 |
|Pagination|Struct| |分页信息 |
|PageNumber|Integer|1|页面编号，从1开始 |
|PageSize|Integer|10|每页数量 |
|TotalCount|Integer|100|总数 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainContractProjectsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>7C5D974A-B6D8-4886-A294-781EF3884512</RequestId>
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
    <ContractProjects>
        <ConsortiumId>M8GaMEyX</ConsortiumId>
        <ProjectName>test</ProjectName>
        <CreateTime>1609848383000</CreateTime>
        <ProjectId>RXwQj6m8</ProjectId>
        <UpdateTime>1609848383000</UpdateTime>
        <ProjectVersion>1.0.0</ProjectVersion>
        <ProjectDescription>test</ProjectDescription>
    </ContractProjects>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "7C5D974A-B6D8-4886-A294-781EF3884512",
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
    "ContractProjects": [
      {
        "ConsortiumId": "M8GaMEyX",
        "ProjectName": "test",
        "CreateTime": 1609848383000,
        "ProjectId": "RXwQj6m8",
        "UpdateTime": 1609848383000,
        "ProjectVersion": "1.0.0",
        "ProjectDescription": "test"
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

