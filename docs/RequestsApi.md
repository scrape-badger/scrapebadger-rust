# \RequestsApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**requests_callback_status**](RequestsApi.md#requests_callback_status) | **GET** /v1/requests/{request_id}/callback | Callback status
[**requests_poll_an_async_request**](RequestsApi.md#requests_poll_an_async_request) | **GET** /v1/requests/{request_id} | Poll an async request



## requests_callback_status

> models::AsyncCallbackStatus requests_callback_status(request_id)
Callback status

Webhook delivery state of a call submitted with `X-Callback-URL` / `callback_url`: kept for 24 h. Free. `404 callback_not_found` for a request without a callback, of another account, or older than 24 h.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_id** | **String** |  | [required] |

### Return type

[**models::AsyncCallbackStatus**](AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## requests_poll_an_async_request

> serde_json::Value requests_poll_an_async_request(request_id)
Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.  The final response carries `X-Callback-Status`, `X-Callback-Attempts` and `X-Callback-Error` for a call submitted with a callback; while it runs, the `202` body has a `callback` object. Full delivery state: `GET /v1/requests/{request_id}/callback`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

