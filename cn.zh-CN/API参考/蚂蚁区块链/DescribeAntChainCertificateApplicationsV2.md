# DescribeAntChainCertificateApplicationsV2

查看联盟成员申请连接一条蚂蚁区块链的信息（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainCertificateApplicationsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainCertificateApplicationsV2|系统规定参数。取值：DescribeAntChainCertificateApplicationsV2。 |
|AntChainId|String|是|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|PageNumber|Integer|是|10|页面编号，从1开始 |
|PageSize|Integer|是|1|每页数量 |
|Status|String|是|1|状态 |
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
|CertificateApplications|Array of CertificateApplications| |证书申请信息 |
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|Bid|String|26842|Bid |
|Createtime|Long|1609848404000|创建时间 |
|Status|String|1|状态 |
|Updatetime|Long|1609848404000|更新时间 |
|Username|String|uid-1034774750177934|账户名 |
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
http(s)://[Endpoint]/?Action=DescribeAntChainCertificateApplicationsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>72408F88-880E-4805-9E3C-6ACA6D693960</RequestId>
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
    <CertificateApplications>
        <Status>1</Status>
        <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
        <Username>uid-1034774750177934</Username>
        <Createtime>1609848404000</Createtime>
        <Updatetime>1609848404000</Updatetime>
    </CertificateApplications>
    <CertificateApplications>
        <Status>1</Status>
        <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
        <Username>uid-1374074750210905</Username>
        <Createtime>1609744560000</Createtime>
        <Updatetime>1609744560000</Updatetime>
    </CertificateApplications>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "72408F88-880E-4805-9E3C-6ACA6D693960",
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
    "CertificateApplications": [
      {
        "Status": "1",
        "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
        "Username": "uid-1034774750177934",
        "Createtime": 1609848404000,
        "Updatetime": 1609848404000
      },
      {
        "Status": "1",
        "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
        "Username": "uid-1374074750210905",
        "Createtime": 1609744560000,
        "Updatetime": 1609744560000
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

