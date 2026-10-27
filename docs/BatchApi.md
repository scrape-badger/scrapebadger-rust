# \BatchApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batch_submit_a_batch_of_async_requests**](BatchApi.md#batch_submit_a_batch_of_async_requests) | **POST** /v1/batch | Submit a batch of async requests



## batch_submit_a_batch_of_async_requests

> serde_json::Value batch_submit_a_batch_of_async_requests(batch_request)
Submit a batch of async requests

Submit up to 100 GET reads in one call. Each item runs as its own ``Prefer: respond-async`` request under this key, with the same auth, credit check, rate limit and billing as if it were sent alone, and returns a request_id to poll (or a webhook to ``callback_url``). At most 10 items of a batch run at the same time. Submitting is free; each item bills as it runs. Items are checked against the spendable balance first, at the endpoint's base price, so a batch never starts more than the account can pay for.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**batch_request** | [**BatchRequest**](BatchRequest.md) |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

