#Product_Distribution
GET/POST/product/batchGetProductLogisticPrice

Description：获取铺货商品国内段运费

## Parameter

|Name|Type|Required or not|Description|
|---|---|---|---|
|mp_ids|Number[]|Yes|铺货商品ID|
|address_info|Object|Yes|收货地址|

## Response Parameters

| Name       | Type     | Description |
| ---------- | -------- | ----------- |
| data       | Object[] | 铺货商品物流费用    |
| success    | Boolean  | 是否成功        |
| error_code | String   | 错误码         |
| error_msg  | String   | 错误信息        |
|            |          |             |

#BatchGetProductLogisticPrice JAVA
#BatchGetProductLogisticPrice PHP
#BatchGetProductLogisticPrice  .NET
#BatchGetProductLogisticPrice  PYTHON