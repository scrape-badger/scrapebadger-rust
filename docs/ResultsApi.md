# \ResultsApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**results_re_read_a_result_removed**](ResultsApi.md#results_re_read_a_result_removed) | **GET** /v1/results/{result_id} | Re-read a result (removed)



## results_re_read_a_result_removed

> serde_json::Value results_re_read_a_result_removed(result_id)
Re-read a result (removed)

Removed (SCR-396): ScrapeBadger no longer stores results, so there is nothing to re-read. Always 410. Narrow a call with _jq / _fields / _max_items instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**result_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

