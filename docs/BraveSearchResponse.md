# BraveSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **String** |  | 
**country** | **String** |  | 
**ui_language** | **String** |  | 
**safe_search** | **String** |  | 
**result_count** | **i32** |  | 
**results** | [**Vec<models::BraveResult>**](BraveResult.md) |  | 
**query_info** | [**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md) |  | 
**source_url** | **String** |  | 
**fetched_at** | **String** |  | 
**fetched_utc** | **f64** |  | 
**page** | **i32** |  | 
**has_next** | **bool** |  | 
**next_page** | Option<[**models::NextPage**](Next_Page.md)> |  | [optional]
**faq** | Option<[**Vec<std::collections::HashMap<String, serde_json::Value>>**](std::collections::HashMap.md)> |  | [optional]
**discussions** | Option<[**Vec<models::BraveResult>**](BraveResult.md)> |  | [optional]
**videos** | Option<[**Vec<models::BraveResult>**](BraveResult.md)> |  | [optional]
**news** | Option<[**Vec<models::BraveResult>**](BraveResult.md)> |  | [optional]
**images** | Option<[**Vec<models::BraveResult>**](BraveResult.md)> |  | [optional]
**related_searches** | Option<[**Vec<std::collections::HashMap<String, String>>**](std::collections::HashMap.md)> |  | [optional]
**rich_blocks** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


