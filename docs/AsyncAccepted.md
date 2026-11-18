# AsyncAccepted

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **String** |  | 
**status** | **String** |  | 
**retry_after_seconds** | **i32** |  | 
**next_action** | [**models::AsyncAcceptedNextAction**](AsyncAccepted_next_action.md) |  | 
**detail** | Option<**String**> |  | [optional]
**callback** | Option<[**serde_json::Value**](.md)> | Only on a poll of a call submitted with a callback: the delivery state so far (`status`, `attempts`, `last_error`). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


