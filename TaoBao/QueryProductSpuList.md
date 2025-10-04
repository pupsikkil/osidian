#Product_Distribution #QueryProductSpuList
GET/POST/product/spus/get
Description：铺货商品列表获取。使用场景：仅铺货商品ID获取，素材等详情信息请通过“/product/details/query” 接口获取。

## Parameter

|Name|Type|Required or not|Description|
|---|---|---|---|
|sort_field|String|No|sort field，If the search mode of spus_get_type is SCROLL，Sorting is not supported at this time|
|page_size|Number|Yes|page size，If the search mode of spus_get_type is SCROLL，This parameter can be set only for the first time|
|end_modified_time|Number|Yes|timestamp|
|status|String|Yes|NORMAL("NORMAL", "正常铺货"), CANCEL("CANCEL", "已取消铺货”),INACTIVE("INACTIVE", "商品不可用");|
|item_id|Number|No|spu id ，If you do not query by time interval, you can query by product spu id|
|spus_get_type|String|No|There are two query methods，default（PAGINATION）： PAGINATION("PAGINATION", "Ordinary paging query")， SCROLL("SCROLL", "scroll query”)|
|scroll_id|String|No|If the search mode of spus_get_type is SCROLL, the scroll_id parameter in the first query can be empty. Follow-up query must be performed based on the scroll_id returned in the previous query.Until the query ends|
|sort_type|String|No|sort type，If the search mode of spus_get_type is SCROLL，Sorting is not supported at this time|
|page_no|Number|No|page no，If the search mode of spus_get_type is SCROLL，Paging is not supported|
|start_modified_time|Number|Yes|timestamp|

## Response Parameters

|Name|Type|Description|
|---|---|---|
|success|Boolean|success flag|
|error_code|String|error code|
|error_msg|String|error message|
|data|Object|business response|
#QueryProductSpuList JAVA
#QueryProductSpuList PHP
#QueryProductSpuList .NET
#QueryProductSpuList PYTHON
