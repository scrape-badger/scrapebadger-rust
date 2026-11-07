# YelpBusiness

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**position** | **i32** | 1-based place in Yelp's organic order across pages (page 2 starts at 11): Yelp's own number where it numbers the results; services searches are unnumbered and keep Yelp's order. For ads, the slot order. | 
**is_ad** | **bool** |  | 
**id** | **String** | Yelp encrypted business ID. | 
**alias** | **String** | Business slug used in /biz/<alias>. | 
**name** | **String** |  | 
**url** | **String** |  | 
**rating** | Option<**f64**> |  | [optional]
**review_count** | Option<**i32**> |  | [optional]
**price** | Option<**String**> |  | [optional]
**price_level** | Option<**i32**> |  | [optional]
**categories** | Option<[**Vec<models::YelpCategory>**](YelpCategory.md)> |  | [optional]
**neighborhoods** | Option<**Vec<String>**> |  | [optional]
**address** | Option<**String**> |  | [optional]
**city** | Option<**String**> |  | [optional]
**phone** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> |  | [optional]
**opening_hours** | Option<[**Vec<models::YelpHours>**](YelpHours.md)> |  | [optional]
**snippet** | Option<**String**> |  | [optional]
**snippet_type** | Option<**String**> |  | [optional]
**highlights** | Option<**Vec<String>**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**photos** | Option<**Vec<String>**> |  | [optional]
**alternate_names** | Option<**Vec<String>**> |  | [optional]
**is_service_area_business** | Option<**bool**> |  | [optional]
**is_yelp_guaranteed** | Option<**bool**> |  | [optional]
**has_verified_license** | Option<**bool**> |  | [optional]
**ad_placement** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


