# AutoScout24Listing

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**cross_reference_id** | Option<**String**> |  | [optional]
**position** | **i32** |  | 
**title** | **String** |  | 
**url** | **String** |  | 
**images** | Option<**Vec<String>**> |  | [optional]
**online_purchase_images** | Option<**Vec<String>**> |  | [optional]
**price** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> |  | [optional][default to EUR]
**price_formatted** | Option<**String**> |  | [optional]
**price_evaluation** | Option<**i32**> |  | [optional]
**price_evaluation_enabled** | Option<**bool**> |  | [optional]
**price_details** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**old_price_formatted** | Option<**String**> |  | [optional]
**is_super_deal** | Option<**bool**> |  | [optional]
**is_conditional_price** | Option<**bool**> |  | [optional]
**vat_label_required** | Option<**bool**> |  | [optional]
**make** | Option<**String**> |  | [optional]
**model** | Option<**String**> |  | [optional]
**model_id** | Option<**i32**> |  | [optional]
**model_group** | Option<**String**> |  | [optional]
**variant** | Option<**String**> |  | [optional]
**motor_type** | Option<**String**> |  | [optional]
**version** | Option<**String**> |  | [optional]
**subtitle** | Option<**String**> |  | [optional]
**article_type** | Option<**String**> |  | [optional]
**offer_type** | Option<**String**> |  | [optional]
**fuel** | Option<**String**> |  | [optional]
**fuel_type** | Option<**String**> |  | [optional]
**transmission** | Option<**String**> |  | [optional]
**mileage_km** | Option<**i32**> |  | [optional]
**first_registration** | Option<**String**> |  | [optional]
**registration_year** | Option<**i32**> |  | [optional]
**registration_month** | Option<**i32**> |  | [optional]
**power_kw** | Option<**f64**> |  | [optional]
**power_hp** | Option<**f64**> |  | [optional]
**displacement_cc** | Option<**i32**> |  | [optional]
**is_damaged** | Option<**bool**> |  | [optional]
**available_now** | Option<**bool**> |  | [optional]
**available_at** | Option<**String**> |  | [optional]
**available_utc** | Option<**f64**> |  | [optional]
**availability_in_days** | Option<**i32**> |  | [optional]
**location** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**seller** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**rating** | Option<**f64**> |  | [optional]
**rating_count** | Option<**i32**> |  | [optional]
**ratings_enabled** | Option<**bool**> |  | [optional]
**leasing** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**seals** | Option<[**Vec<std::collections::HashMap<String, serde_json::Value>>**](std::collections::HashMap.md)> |  | [optional]
**online_purchase** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**electric_vehicle_banner** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**is_deliverable** | Option<**bool**> |  | [optional]
**has_video** | Option<**bool**> |  | [optional]
**has_360_image** | Option<**bool**> |  | [optional]
**interest_level** | Option<**String**> |  | [optional]
**is_trending** | Option<**bool**> |  | [optional]
**ad_tier** | Option<**String**> |  | [optional]
**result_type** | Option<**String**> |  | [optional]
**result_section** | Option<**String**> |  | [optional]
**special_conditions** | Option<[**Vec<serde_json::Value>**](serde_json::Value.md)> |  | [optional]
**vehicle_details** | Option<[**Vec<std::collections::HashMap<String, serde_json::Value>>**](std::collections::HashMap.md)> |  | [optional]
**wltp_values** | Option<**Vec<String>**> |  | [optional]
**vehicle** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> | Additional native vehicle attributes, including localized labels. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


