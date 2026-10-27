# \AccountApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**account_get_account_info**](AccountApi.md#account_get_account_info) | **GET** /v1/account/me | Get account info
[**account_get_the_webhook_signing_secret**](AccountApi.md#account_get_the_webhook_signing_secret) | **GET** /v1/account/webhook-secret | Get the webhook signing secret
[**account_rotate_the_webhook_signing_secret**](AccountApi.md#account_rotate_the_webhook_signing_secret) | **POST** /v1/account/webhook-secret/rotate | Rotate the webhook signing secret



## account_get_account_info

> models::AccountInfo account_get_account_info()
Get account info

Get account details for the authenticated API key.  Returns credit balances, tier, rate limit, and subscription details. No credits are deducted for this call.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AccountInfo**](AccountInfo.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## account_get_the_webhook_signing_secret

> models::WebhookSecret account_get_the_webhook_signing_secret()
Get the webhook signing secret

The secret that signs this account's async-request webhooks, created on first read. Verify a delivery by comparing ``X-ScrapeBadger-Signature`` with ``sha256=`` + hex HMAC-SHA256(secret, raw body).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::WebhookSecret**](WebhookSecret.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## account_rotate_the_webhook_signing_secret

> models::WebhookSecret account_rotate_the_webhook_signing_secret()
Rotate the webhook signing secret

Replace the signing secret. Deliveries that start from now on are signed with the new one; retries of a delivery already under way keep the old one.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::WebhookSecret**](WebhookSecret.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

