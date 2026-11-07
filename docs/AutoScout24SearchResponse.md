# AutoScout24SearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**market** | **String** |  | 
**source_url** | **String** |  | 
**total_results** | **i32** |  | 
**total_pages** | **i32** |  | 
**page** | **i32** |  | 
**page_size** | Option<**i32**> |  | [optional][default to 20]
**has_next_page** | **bool** |  | 
**next_page** | Option<**i32**> |  | 
**pagination_cap** | Option<**i32**> |  | [optional][default to 200]
**results** | [**Vec<models::AutoScout24Listing>**](AutoScout24Listing.md) |  | 
**filters** | [**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md) |  | 
**applied_filters** | [**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md) |  | 
**latency_ms** | **i32** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


