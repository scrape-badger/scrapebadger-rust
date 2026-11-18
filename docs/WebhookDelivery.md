# WebhookDelivery

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **String** |  | 
**endpoint** | **String** | Path of the call, e.g. `/v1/perplexity/ask` (never its query). | 
**state** | **String** | `pending`: the call is still running. `delivering`: an attempt is under way or the next retry is due at `next_attempt_at`. `delivered`: the endpoint answered 2xx. `failed`: every attempt failed, a final status (not 408/429/5xx) came back, or a gateway restart interrupted the delivery (`last_error` \"interrupted (gateway restart)\"). | 
**attempts** | **i32** |  | 
**last_status** | Option<**i32**> |  | [optional]
**last_error** | Option<**String**> |  | [optional]
**created_at** | **i32** | Unix time the call was submitted. | 
**delivered_at** | Option<**i32**> |  | [optional]
**callback_host** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


