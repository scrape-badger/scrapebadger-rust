# YelpSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**market** | **String** |  | 
**query** | Option<**String**> |  | 
**location** | **String** |  | 
**location_resolved** | [**models::YelpResolvedLocation**](YelpResolvedLocation.md) |  | 
**did_you_mean** | Option<**String**> |  | [optional]
**query_matched** | **bool** | False when Yelp could not place the query; results are then Yelp's broader ranking for the location, as Yelp shows them. | 
**total_results** | **i32** | Yelp's reported total; at most 110 are browsable. | 
**page** | **i32** |  | 
**page_size** | **i32** |  | 
**total_pages** | **i32** |  | 
**has_next_page** | **bool** |  | 
**next_page** | Option<**i32**> |  | [optional]
**results** | [**Vec<models::YelpBusiness>**](YelpBusiness.md) |  | 
**ads** | [**Vec<models::YelpBusiness>**](YelpBusiness.md) |  | 
**filters** | [**std::collections::HashMap<String, models::YelpFilterGroup>**](YelpFilterGroup.md) |  | 
**related_searches** | [**Vec<models::YelpLink>**](YelpLink.md) |  | 
**source_url** | **String** |  | 
**fetched_at** | **String** |  | 
**fetched_utc** | **f64** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


