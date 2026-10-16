# PortalApiRoutersV1AsosSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**market** | **String** |  | 
**search_term** | Option<[**models::Searchterm**](Searchterm.md)> |  | [optional]
**category_name** | Option<[**models::Categoryname**](Categoryname.md)> |  | [optional]
**total_results** | **i32** |  | 
**offset** | **i32** |  | 
**limit** | **i32** |  | 
**next_offset** | Option<[**models::NextOffset**](Next_Offset.md)> |  | [optional]
**products** | [**Vec<models::Product>**](Product.md) |  | 
**facets** | Option<[**Vec<std::collections::HashMap<String, serde_json::Value>>**](std::collections::HashMap.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


