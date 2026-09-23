# VintedItemSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **i32** |  | 
**title** | **String** |  | 
**price** | [**models::VintedPrice**](VintedPrice.md) |  | 
**brand_title** | Option<**String**> |  | [optional]
**display_title** | Option<**String**> |  | [optional]
**display_subtitle** | Option<**String**> |  | [optional]
**size_title** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**url** | **String** |  | 
**path** | Option<**String**> |  | [optional]
**is_visible** | Option<**bool**> |  | [optional][default to true]
**promoted** | Option<**bool**> |  | [optional][default to false]
**favourite_count** | Option<**i32**> |  | [optional][default to 0]
**view_count** | Option<**i32**> |  | [optional][default to 0]
**service_fee** | Option<**String**> |  | [optional]
**total_item_price** | Option<**String**> |  | [optional]
**content_source** | Option<**String**> |  | [optional]
**seller_country_code** | Option<**String**> |  | [optional]
**similarity_score** | Option<**f64**> |  | [optional]
**user** | Option<[**models::VintedUserSummary**](VintedUserSummary.md)> |  | [optional]
**photo** | Option<[**models::VintedPhoto**](VintedPhoto.md)> |  | [optional]
**photos** | Option<[**Vec<models::VintedPhoto>**](VintedPhoto.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


