#Product_Distribution #QueryProductsDetails
GET/POST/product/details/query
Description：distributor query product details

## Parameter

|Name|Type|Required or not|Description|
|---|---|---|---|
|items|Number[]|Yes|供销商品Id列表，最大20个|
|language|String|No|素材语言（'zh' 默认、'en' ）|
|market_code|String|No|主营市场（国际标准地区编码前2位，例如：US 欧美地区）|
|query_options_map|Object|No|查询可选项（如需获取该字段下的素材信息，请联系商务同学申请开通）|

## Response Parameters

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| success    | Boolean | 是否成功        |
| error_code | String  | 错误码         |
| error_msg  | String  | 错误原因        |
| data       | Object  | -           |
- #QueryProductsDetails JAVA
- #QueryProductsDetails PHP
- #QueryProductsDetails .NET
- #QueryProductsDetails PYTHON
