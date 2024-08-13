# staking

## 1.fp列表
```
GET    /v1/finality-providers
```

参数 | 说明 | 是否必填
---|---|:---:
pagination_key | 页码
### 成功操作返回
```json
{
  "data": [
      {active_delegations: 2496
      active_tvl: 1312939495
      btc_pk: "f4940b238dcd00535fde9730345bab6ff4ea6d413cc3602c4033c10f251c7e81"
      commission: "0.05"
      description: {moniker: "Chakra", identity: "", website: "https://chakrachain.io", security_contact: "",…}
      total_delegations: 2535
      total_tvl: 1320213445},
      {},{}],
  "pagination":{next_key: "eyJmaW5hbGl0eV9wcm92aWRlcl9wa19oZXgiOiIxN2QzM2UxOGFiODViMzMwNTBjNzYzYTQ0ZDg3NTdkZmU0ZTBhM2M0OWUxMjkxMWY2NWUwNTI5YzNjZDIyNGI2IiwiYWN0aXZlX3R2bCI6Mjk4OTU5MDB9"}
}
```
### 失败操作返回
```json

```

## 2 stake 数据概览
```
GET    /v1/stats
```
### 参数说明
参数 | 说明 | 是否必填
---|---|:---:


### 成功操作返回
```json
{
    "data": {
        "active_tvl": 5000242246,
        "total_tvl": 5088616776,
        "active_delegations": 32291,
        "total_delegations": 33129,
        "total_stakers": 30995,
        "unconfirmed_tvl": 5000192246
    }
}
```

## 3. 跟api版本相关的一组数据，比如质押池还剩多少，区块高度判断
```
GET    /v1/global-params
```

参数 | 说明 | 是否必填
---|---|:---:

### 成功操作返回
```json
{
    "data": {
        "versions": [
            {
                "version": 0,
                "activation_height": 197535,
                "staking_cap": 500000000,
                "tag": "62627434",
                "covenant_pks": [
                    "0249766ccd9e3cd94343e2040474a77fb37cdfd30530d05f9f1e96ae1e2102c86e",
                    "0276d1ae01f8fb6bf30108731c884cddcf57ef6eef2d9d9559e130894e0e40c62c",
                    "0217921cf156ccb4e73d428f996ed11b245313e37e27c978ac4d2cc21eca4672e4",
                    "02113c3a32a9d320b72190a04a020a0db3976ef36972673258e9a38a364f3dc3b0",
                    "0379a71ffd71c503ef2e2f91bccfc8fcda7946f4653cef0d9f3dde20795ef3b9f0",
                    "023bb93dfc8b61887d771f3630e9a63e97cbafcfcc78556a474df83a31a0ef899c",
                    "03d21faf78c6751a0d38e6bd8028b907ff07e9a869a43fc837d6b3f8dff6119a36",
                    "0340afaf47c4ffa56de86410d8e47baa2bb6f04b604f4ea24323737ddc3fe092df",
                    "03f5199efae3f28bb82476163a7e458c7ad445d9bffb0682d10d3bdb2cb41f8e8e"
                ],
                "covenant_quorum": 6,
                "unbonding_time": 1008,
                "unbonding_fee": 2000,
                "max_staking_amount": 5000000,
                "min_staking_amount": 50000,
                "max_staking_time": 64000,
                "min_staking_time": 64000,
                "confirmation_depth": 10
            },
            {
                "version": 1,
                "activation_height": 198665,
                "staking_cap": 5000000000,
                "tag": "62627434",
                "covenant_pks": [
                    "0209585ab55a971a231c945790a0a81df754e5a07263a5c20829931cc24683bbb7",
                    "0276d1ae01f8fb6bf30108731c884cddcf57ef6eef2d9d9559e130894e0e40c62c",
                    "0217921cf156ccb4e73d428f996ed11b245313e37e27c978ac4d2cc21eca4672e4",
                    "02113c3a32a9d320b72190a04a020a0db3976ef36972673258e9a38a364f3dc3b0",
                    "0379a71ffd71c503ef2e2f91bccfc8fcda7946f4653cef0d9f3dde20795ef3b9f0",
                    "023bb93dfc8b61887d771f3630e9a63e97cbafcfcc78556a474df83a31a0ef899c",
                    "03d21faf78c6751a0d38e6bd8028b907ff07e9a869a43fc837d6b3f8dff6119a36",
                    "0340afaf47c4ffa56de86410d8e47baa2bb6f04b604f4ea24323737ddc3fe092df",
                    "03f5199efae3f28bb82476163a7e458c7ad445d9bffb0682d10d3bdb2cb41f8e8e"
                ],
                "covenant_quorum": 6,
                "unbonding_time": 1008,
                "unbonding_fee": 10000,
                "max_staking_amount": 5000000,
                "min_staking_amount": 50000,
                "max_staking_time": 64000,
                "min_staking_time": 64000,
                "confirmation_depth": 10
            }
        ]
    }
}
```
### 失败操作返回
```json

```

## 4. 质押记录 和状态
```
GET    /v1/staker/delegations?pagination_key=&staker_btc_pk=0609c4384ee7bb3c32e860c41b1c90fc33f2b5a1c6e7ddfafb561795255012d1
```


参数 | 说明 | 是否必填
---|---|:---:

### 成功操作返回
```json
{"data":[],"pagination":{"next_key":""}}
```
### 失败操作返回
```json
{
    "msg": "失败原因",
    "errno": -1 //非0，会有10002等code,可以不用
}
```


## 5.
```
GET   https://babylon.mempool.space/signet/api/blocks/tip/height
```
### 参数说明

### 成功操作返回

200344


## 6. stake操作
```
直接调用了链上的交易？ 
```
### 成功操作返回
```json

```
### 失败操作返回
```json

```

## errno错误状态，50001未登录的特有code
## 7.查询可用次数
```
POST    /user/getNumber
```
### 成功操作返回
```json
{
  "data": {
    "number": 234,  //ocr可用次数
    },
  "errno": 0
}
```
### 失败操作返回
```json
{
    "msg": "失败原因",
    "errno": -1    //非0
}
```

## 8.查询配置
```
POST    /user/getConf
```
### 成功操作返回
```json
{
  "data": {
    "conf":{
      "using": 0, //当前使用的配置0
      "confList": [
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16},
        {},
        {}
      ]
    }
  },
  "errno": 0
}
```
## 9.更新配置
```
POST    /user/modConf

```

### 参数说明
参数 | 说明 | 是否必填
---|---|:---:
conf | 配置信息 | 是
##
> 请求参数的conf字段与查询接口返回的conf一致，相当于整体修改配置信息。可以限制下最多5个配置就行，多了就不让新增了
### 成功操作返回
```json
{
  "data": {
    "conf":{
      "using": 0,
      "confList": [
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16},
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16},
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16},
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16},
        {"scale": 12, "sizeCn": 100, "sizeEn": 100, "colorCn": 8, "colorEn": 8, "spaceCn": 20, "spaceEn": 20, "vertical": 150, "weightCn": 0, "weightEn": 0, "sealColor": "ff3f30", "horizontal": 50, "sealWeight": 16}
      ]
    }
  },
  "errno": 0
}
```
