# DescribeAntChainDownloadPathsV2

获取一条蚂蚁区块链相关证书下载地址（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainDownloadPathsV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainDownloadPathsV2|系统规定参数。取值：DescribeAntChainDownloadPathsV2。 |
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
|CaCrtUrl|String|http://\*\*\*ca.crt|ca.crt下载链接 |
|ClientCrtUrl|String|http://\*\*\*client.crt|client.crt下载链接 |
|SdkUrl|String|http://\*\*\*|sdk下载链接 |
|TrustCaUrl|String|http://\*\*\*trustCa|trustCA下载链接 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainDownloadPathsV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>3213170D-59A5-44CE-8837-37313317690A</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>
    <SdkUrl>https://help.aliyun.com/document_detail/154544.html?spm=5176.11638311.0.0.75d54a924Ptnt9</SdkUrl>
    <TrustCaUrl>https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/mvp_8bd720bde18c4b37b0f4a1c7834db163_mychain010/trustCa?Expires=1609989075&amp;OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&amp;Signature=13q9CULCT4kG%2FkJPTA%2Fn3GlYzLc%3D&amp;response-content-disposition=attachment%3B%20filename%3DtrustCa</TrustCaUrl>
    <CaCrtUrl>https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/mvp_8bd720bde18c4b37b0f4a1c7834db163_mychain010/ca.crt?Expires=1609989075&amp;OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&amp;Signature=8drsyeYi8wQmiVvnLNZ2%2FnuYdRs%3D&amp;response-content-disposition=attachment%3B%20filename%3Dca.crt</CaCrtUrl>
    <ClientCrtUrl>https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/aliyun_8bd720bde18c4b37b0f4a1c7834db163_mychain010/certificate/3a6bd8d8dec087aff737e3b92dfac034b35c63c87d3d226e0977f94679615df2.crt?Expires=1609989075&amp;OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&amp;Signature=rHkv2TBclPssp69kHmCVZ53OU0k%3D&amp;response-content-disposition=attachment%3B%20filename%3Dclient.crt</ClientCrtUrl>
</Result>
```

`JSON` 格式

```
{
  "RequestId": "3213170D-59A5-44CE-8837-37313317690A",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": {
    "SdkUrl": "https://help.aliyun.com/document_detail/154544.html?spm=5176.11638311.0.0.75d54a924Ptnt9",
    "TrustCaUrl": "https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/mvp_8bd720bde18c4b37b0f4a1c7834db163_mychain010/trustCa?Expires=1609989075&OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&Signature=13q9CULCT4kG%2FkJPTA%2Fn3GlYzLc%3D&response-content-disposition=attachment%3B%20filename%3DtrustCa",
    "CaCrtUrl": "https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/mvp_8bd720bde18c4b37b0f4a1c7834db163_mychain010/ca.crt?Expires=1609989075&OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&Signature=8drsyeYi8wQmiVvnLNZ2%2FnuYdRs%3D&response-content-disposition=attachment%3B%20filename%3Dca.crt",
    "ClientCrtUrl": "https://mychain-baas-oss.oss-cn-shanghai.aliyuncs.com/aliyun_8bd720bde18c4b37b0f4a1c7834db163_mychain010/certificate/3a6bd8d8dec087aff737e3b92dfac034b35c63c87d3d226e0977f94679615df2.crt?Expires=1609989075&OSSAccessKeyId=LTAI4G6VCwi7xUigc3hcNUZR&Signature=rHkv2TBclPssp69kHmCVZ53OU0k%3D&response-content-disposition=attachment%3B%20filename%3Dclient.crt"
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

