# DescribeAntChainMembersV2

获取联盟成员列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainMembersV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainMembersV2|系统规定参数。取值：DescribeAntChainMembersV2。 |
|ConsortiumId|String|是|M8GaMEyX|联盟ID |
|PageNumber|Integer|是|1|页面编号，从1开始 |
|PageSize|Integer|是|10|页面包含条例数 |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|Struct| |请求结果 |
|Members|Array of Members| |联盟成员 |
|JoinTime|Long|1609745002000|成员加入联盟时戳 |
|MemberId|String|1034774750177934|成员ID |
|MemberName|String|uid-1034774750177934|成员名称 |
|Role|String|Member|加入联盟状态 |
|Status|String|AllianceJoined|成员身份 |
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
http(s)://[Endpoint]/?Action=DescribeAntChainMembersV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>2CB7F6F2-E636-4A17-A639-E373D4C3D341</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <Pagination>
        <TotalCount>2</TotalCount>
        <PageSize>10</PageSize>
        <PageNumber>1</PageNumber>
    </Pagination>
    <Members>
        <Role>Member</Role>
        <Status>AllianceJoined</Status>
        <MemberId>1034774750177934</MemberId>
        <JoinTime>1609745002000</JoinTime>
        <MemberName>uid-1034774750177934</MemberName>
    </Members>
    <Members>
        <Role>SuperAdmin</Role>
        <Status>AllianceJoined</Status>
        <MemberId>1374074750210905</MemberId>
        <JoinTime>1609221290000</JoinTime>
        <MemberName>uid-1374074750210905</MemberName>
    </Members>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "2CB7F6F2-E636-4A17-A639-E373D4C3D341",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "Pagination": {
      "TotalCount": 2,
      "PageSize": 10,
      "PageNumber": 1
    },
    "Members": [
      {
        "Role": "Member",
        "Status": "AllianceJoined",
        "MemberId": "1034774750177934",
        "JoinTime": 1609745002000,
        "MemberName": "uid-1034774750177934"
      },
      {
        "Role": "SuperAdmin",
        "Status": "AllianceJoined",
        "MemberId": "1374074750210905",
        "JoinTime": 1609221290000,
        "MemberName": "uid-1374074750210905"
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

