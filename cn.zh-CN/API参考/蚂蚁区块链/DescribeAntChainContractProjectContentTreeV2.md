# DescribeAntChainContractProjectContentTreeV2

获取一个合约工程的内容树（仅适用于阿里云国内站）

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Baas&api=DescribeAntChainContractProjectContentTreeV2&type=RPC&version=2018-12-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAntChainContractProjectContentTreeV2|系统规定参数。取值：DescribeAntChainContractProjectContentTreeV2。 |
|ConsortiumId|String|是|M8GaMEyX|联盟ID |
|ProjectId|String|是|2L9VK68g|项目ID |
|RegionId|String|否|cn-hangzhou|地域ID，限制cn-hangzhou |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|返回码 |
|HttpStatusCode|String|200|请求返回码 |
|Message|String|OK|请求消息 |
|RequestId|String|D68D66B6-1964-4073-8714-B49F5EF1AEFC|请求ID |
|Result|String|""|请求结果 |
|ResultCode|String|OK|结果码 |
|ResultMessage|String|OK|结果消息 |
|Success|Boolean|true|结果状态 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAntChainContractProjectContentTreeV2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>E568090A-FBB3-4830-84E4-4A31A30E716C</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Code>OK</Code>
<ResultCode>OK</ResultCode>
<Success>true</Success>
<Result>{"description":"test","projectId":"RXwQj6m8","projectName":"test","treeContractContent":[{"content":"pragma solidity ^0.4.20;\n// We have to specify which version of compiler this code will compile with,\n// version should be lower than (or equals to) the supported version showing on this tool.\ncontract Voting {\n    /* Solidity doesn't let you pass in an array of strings in the constructor (yet).\n    We will use an array of bytes32 instead to store the list of candidates with string type.\n    */\n    bytes32[] public candidateList;\n\n    /* mapping field below is equivalent to an associative array or hash.\n    The key of the mapping is candidate name stored as type bytes32 and value is\n    an unsigned integer to store the vote count.\n    */\n    mapping (bytes32 =&gt; uint8) public votesReceived;\n\n    /* Counting for candidate counts and total votes for all candidates\n    */\n    uint256 public candidateCount;\n    uint256 public totalVotes;\n\n\n    /* Events which will help for logging and debugging\n    'identity' is like 'address' in original Solidity, length of 'identity' is 256 (bits).\n    */\n    event VOTE(bytes32 candidate, identity voterId);\n    event VALID(bool valid);\n\n\n    /* This is the constructor which will be called once when you\n    deploy the contract to the blockchain. When we deploy the contract,\n    we will pass an array of candidates who will be contesting in the election.\n    You can input a candidate name like: Mike , it will be converted to bytes32.\n    */\n    constructor(bytes32[] candidateNames) public {\n        candidateList = candidateNames;\n        candidateCount = candidateList.length;\n    }\n\n    // This function returns the total votes a candidate has received so far.\n    function totalVotesFor(bytes32 candidate) view public returns (uint8) {\n        require(validCandidate(candidate), \"candidate is invalid\");\n        return votesReceived[candidate];\n    }\n\n    // This function increments the vote count for the specified candidate.\n    // This is equivalent to casting a vote.\n    function voteForCandidate(bytes32 candidate) public {\n        require(validCandidate(candidate), \"candidate is invalid\");\n        votesReceived[candidate] += 1;\n        totalVotes += 1;\n\n        emit VOTE(candidate, msg.sender);\n    }\n\n    // This function will help to check whether target candidate is in the candidateList.\n    function validCandidate(bytes32 candidate) view public returns (bool) {\n        for (uint i = 0; i &lt; candidateList.length; i++) {\n            if (candidateList[i] == candidate) {\n                emit VALID(true);\n                return true;\n            }\n        }\n        emit VALID(false);\n        return false;\n    }\n}\n","fileName":"test.sol","id":"mozxjne9","isDir":false,"parentId":"AVXek8R4"}],"type":"solidity","version":"1.0.0"}</Result>
```

`JSON` 格式

```
{
  "RequestId": "E568090A-FBB3-4830-84E4-4A31A30E716C",
  "HttpStatusCode": "200",
  "Code": "OK",
  "ResultCode": "OK",
  "Success": true,
  "Result": "{\"description\":\"test\",\"projectId\":\"RXwQj6m8\",\"projectName\":\"test\",\"treeContractContent\":[{\"content\":\"pragma solidity ^0.4.20;\\n// We have to specify which version of compiler this code will compile with,\\n// version should be lower than (or equals to) the supported version showing on this tool.\\ncontract Voting {\\n    /* Solidity doesn't let you pass in an array of strings in the constructor (yet).\\n    We will use an array of bytes32 instead to store the list of candidates with string type.\\n    */\\n    bytes32[] public candidateList;\\n\\n    /* mapping field below is equivalent to an associative array or hash.\\n    The key of the mapping is candidate name stored as type bytes32 and value is\\n    an unsigned integer to store the vote count.\\n    */\\n    mapping (bytes32 => uint8) public votesReceived;\\n\\n    /* Counting for candidate counts and total votes for all candidates\\n    */\\n    uint256 public candidateCount;\\n    uint256 public totalVotes;\\n\\n\\n    /* Events which will help for logging and debugging\\n    'identity' is like 'address' in original Solidity, length of 'identity' is 256 (bits).\\n    */\\n    event VOTE(bytes32 candidate, identity voterId);\\n    event VALID(bool valid);\\n\\n\\n    /* This is the constructor which will be called once when you\\n    deploy the contract to the blockchain. When we deploy the contract,\\n    we will pass an array of candidates who will be contesting in the election.\\n    You can input a candidate name like: Mike , it will be converted to bytes32.\\n    */\\n    constructor(bytes32[] candidateNames) public {\\n        candidateList = candidateNames;\\n        candidateCount = candidateList.length;\\n    }\\n\\n    // This function returns the total votes a candidate has received so far.\\n    function totalVotesFor(bytes32 candidate) view public returns (uint8) {\\n        require(validCandidate(candidate), \\\"candidate is invalid\\\");\\n        return votesReceived[candidate];\\n    }\\n\\n    // This function increments the vote count for the specified candidate.\\n    // This is equivalent to casting a vote.\\n    function voteForCandidate(bytes32 candidate) public {\\n        require(validCandidate(candidate), \\\"candidate is invalid\\\");\\n        votesReceived[candidate] += 1;\\n        totalVotes += 1;\\n\\n        emit VOTE(candidate, msg.sender);\\n    }\\n\\n    // This function will help to check whether target candidate is in the candidateList.\\n    function validCandidate(bytes32 candidate) view public returns (bool) {\\n        for (uint i = 0; i < candidateList.length; i++) {\\n            if (candidateList[i] == candidate) {\\n                emit VALID(true);\\n                return true;\\n            }\\n        }\\n        emit VALID(false);\\n        return false;\\n    }\\n}\\n\",\"fileName\":\"test.sol\",\"id\":\"mozxjne9\",\"isDir\":false,\"parentId\":\"AVXek8R4\"}],\"type\":\"solidity\",\"version\":\"1.0.0\"}"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Baas)查看更多错误码。

