# ExtractRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | The page to fetch. | 
**wait_for** | Option<**String**> |  | [optional]
**country** | Option<**String**> |  | [optional]
**proxy_tier** | Option<**String**> | Proxy pool: simple, premium or ultra. | [optional][default to Simple]
**extract_rules** | Option<[**std::collections::HashMap<String, models::ExtractRequestExtractRulesValue>**](ExtractRequest_extract_rules_value.md)> |  | [optional]
**ai_extract_rules** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**ai_query** | Option<**String**> |  | [optional]
**render_js** | Option<**bool**> | Render the page in a browser first. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


