# WebhookEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **String** |  | 
**request_id** | Option<**String**> |  | 
**batch_id** | Option<**String**> |  | 
**status** | **i32** | The call's own HTTP status. | 
**headers** | **std::collections::HashMap<String, String>** | The call's kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). | 
**result_url** | Option<**String**> |  | 
**result_expires_at** | **i32** | Unix time. | 
**body_size** | Option<**i32**> |  | 
**body** | Option<[**serde_json::Value**](.md)> |  | 
**body_omitted** | Option<**bool**> | Present (true) when the body was over 1 MB: fetch `result_url`. | [optional]
**attempt** | Option<**i32**> |  | 
**sent_at** | **i32** | Unix time of this attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


