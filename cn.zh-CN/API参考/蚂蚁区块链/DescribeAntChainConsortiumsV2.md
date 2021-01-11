# DescribeAntChainConsortiumsV2

获取联盟列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainConsortiumsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainConsortiumsV2|系统规定参数。取值：DescribeAntChainConsortiumsV2。 |
|PageNumber|Integer|是|10|页面编号，从1开始 |
|PageSize|Integer|是|1|每页显示条例数 |
|RegionId|String|否|cn-hangzhou|地域ID），限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Struct| |请求结果 |
|AntConsortiums|Array of AntConsortiums| |蚂蚁区块链联盟 |
|ChainNum|Long|2|联盟内区块链数量 |
|ConsortiumDescription|String|test|联盟描述 |
|ConsortiumId|String|M8GaMEyX|联盟ID |
|ConsortiumName|String|测试用|联盟名称 |
|CreateTime|Long|1609745002000|联盟创建时戳 |
|IsEmptyConsortium|Boolean|false|联盟是否为空 |
|MemberNum|Long|2|联盟成员数量 |
|Role|String|Member|账户身份角色 |
|Status|String|Active|联盟状态 |
|Pagination|Struct| |分页情况 |
|PageNumber|Integer|1|分页编号，从1开始 |
|PageSize|Integer|10|每页展示条例数 |
|TotalCount|Integer|10|联盟个数 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainConsortiumsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>11DA147F-8470-402C-BE79-3C03F50ACEC7</RequestId>
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
    <AntConsortiums>
        <Role>Member</Role>
        <Status>Active</Status>
        <ConsortiumId>M8GaMEyX</ConsortiumId>
        <ChainNum>1</ChainNum>
        <CreateTime>1609745002000</CreateTime>
        <IsEmptyConsortium>false</IsEmptyConsortium>
        <ConsortiumDescription>0.6.4</ConsortiumDescription>
        <ConsortiumName>测试用</ConsortiumName>
        <MemberNum>2</MemberNum>
    </AntConsortiums>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "11DA147F-8470-402C-BE79-3C03F50ACEC7",
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
    "AntConsortiums": [
      {
        "Role": "Member",
        "Status": "Active",
        "ConsortiumId": "M8GaMEyX",
        "ChainNum": 1,
        "CreateTime": 1609745002000,
        "IsEmptyConsortium": false,
        "ConsortiumDescription": "0.6.4",
        "ConsortiumName": "测试用",
        "MemberNum": 2
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

