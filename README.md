## API说明

项目启动默认端口： 6007

路径： /claim

参数信息：

| 字段    | 字段说明  | 必填 | 备注                              |
| ------- | --------- | ---- | --------------------------------- |
| rpc     | 测试网RPC | Y    |                                   |
| address | 领水地址  | Y    |                                   |
| amount  | 领水金额  | AVAX     | 单位是AVAX，金额太大链上会失败 |

返回值：

| 字段 | 字段说明 | 必填 | 备注 |
| ---- | -------- | ---- | ---- |
| hash | 交易hash |      |      |

请求示例：

```json
//URL: /request
//方法： POST
//请求体: 
{
"network": "xxx", // 要用于交易的网络
"address": "0xRecipientAddress", // 钱包地址
"amount":0   //数量
}


```

返回示例：

```json
{
"success": true, // 领水是否成功
“tx_id”: "0x交易哈希", 
“explorer_url”: “https://cchain.explorer.avax-test.network” //对应区块链浏览器地址
}
```



