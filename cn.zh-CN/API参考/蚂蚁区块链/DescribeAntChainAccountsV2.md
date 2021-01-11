# DescribeAntChainAccountsV2

查询一条蚂蚁区块链的账户列表（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainAccountsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainAccountsV2|系统规定参数。取值：DescribeAntChainAccountsV2。 |
|AntChainId|String|是|区块链ID|区块链ID |
|PageNumber|Integer|是|1|页面编号，从1开始 |
|PageSize|Integer|是|10|每页数量 |
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
|Accounts|Array of Accounts| |账户信息 |
|Account|String|test|账户名 |
|AccountPublicKey|String|2aa43bae103b6840ce8efdfe6f3fe5e52f8d1db0f44ff762df87ba17eb209979a0e22c934b2728c6c1bab864a6da52de60c5da89793bd839650a1a153e876e32|账户公钥 |
|AccountRecoveryKey|String|5a36312d78681794258bb33372586c676adf150ad69e67dbfcaae61bba3607705950bc9efe1bf4a17ac24b05b1615a410e48d2a005dca251c6173495bb47ae29|账户恢复公钥 |
|AccountStatus|String|NORMAL|状态 |
|AntChainId|String|8bd720bde18c4b37b0f4a1c7834db163|区块链ID |
|Pagination|Struct| |分页信息 |
|PageNumber|Integer|1|当前页面编号，从1开始 |
|PageSize|Integer|10|每页数量 |
|TotalCount|Integer|100|总数 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainAccountsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>3375F3B1-9F1D-42B8-B492-5BBBE62408BD</RequestId>
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
    <Accounts>
        <Account>test</Account>
        <AccountStatus>NORMAL</AccountStatus>
        <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
        <AccountRecoveryKey>5a36312d78681794258bb33372586c676adf150ad69e67dbfcaae61bba3607705950bc9efe1bf4a17ac24b05b1615a410e48d2a005dca251c6173495bb47ae29</AccountRecoveryKey>
        <AccountPublicKey>2aa43bae103b6840ce8efdfe6f3fe5e52f8d1db0f44ff762df87ba17eb209979a0e22c934b2728c6c1bab864a6da52de60c5da89793bd839650a1a153e876e32</AccountPublicKey>
    </Accounts>
    <Accounts>
        <Account>test1</Account>
        <AccountStatus>NORMAL</AccountStatus>
        <AntChainId>8bd720bde18c4b37b0f4a1c7834db163</AntChainId>
        <AccountRecoveryKey>2d2f0906643f68cd412b0f81448974a5a4407f254e54258752babd281dc7dcd2eedaed48446ecfab79944ab0817acc43be7c07898e9be8eaf4d771f001eaf764</AccountRecoveryKey>
        <AccountPublicKey>2d2f0906643f68cd412b0f81448974a5a4407f254e54258752babd281dc7dcd2eedaed48446ecfab79944ab0817acc43be7c07898e9be8eaf4d771f001eaf764</AccountPublicKey>
    </Accounts>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "3375F3B1-9F1D-42B8-B492-5BBBE62408BD",
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
    "Accounts": [
      {
        "Account": "test",
        "AccountStatus": "NORMAL",
        "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
        "AccountRecoveryKey": "5a36312d78681794258bb33372586c676adf150ad69e67dbfcaae61bba3607705950bc9efe1bf4a17ac24b05b1615a410e48d2a005dca251c6173495bb47ae29",
        "AccountPublicKey": "2aa43bae103b6840ce8efdfe6f3fe5e52f8d1db0f44ff762df87ba17eb209979a0e22c934b2728c6c1bab864a6da52de60c5da89793bd839650a1a153e876e32"
      },
      {
        "Account": "test1",
        "AccountStatus": "NORMAL",
        "AntChainId": "8bd720bde18c4b37b0f4a1c7834db163",
        "AccountRecoveryKey": "2d2f0906643f68cd412b0f81448974a5a4407f254e54258752babd281dc7dcd2eedaed48446ecfab79944ab0817acc43be7c07898e9be8eaf4d771f001eaf764",
        "AccountPublicKey": "2d2f0906643f68cd412b0f81448974a5a4407f254e54258752babd281dc7dcd2eedaed48446ecfab79944ab0817acc43be7c07898e9be8eaf4d771f001eaf764"
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

