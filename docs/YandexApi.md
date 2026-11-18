# \YandexApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yandex_image_search**](YandexApi.md#yandex_image_search) | **GET** /v1/yandex/images/search | Image search
[**yandex_list_supported_markets**](YandexApi.md#yandex_list_supported_markets) | **GET** /v1/yandex/markets | List supported markets
[**yandex_reverse_image_search**](YandexApi.md#yandex_reverse_image_search) | **GET** /v1/yandex/images/reverse | Reverse image search
[**yandex_web_search**](YandexApi.md#yandex_web_search) | **GET** /v1/yandex/search | Web search
[**yandex_yandex_scraper_health_check**](YandexApi.md#yandex_yandex_scraper_health_check) | **GET** /v1/yandex/health | Yandex scraper health check
[**yandex_yandex_scraper_health_check_head**](YandexApi.md#yandex_yandex_scraper_health_check_head) | **HEAD** /v1/yandex/health | Yandex scraper health check



## yandex_image_search

> serde_json::Value yandex_image_search(query, domain, page, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Image search query, e.g. 'coffee machine' | [required] |
**domain** | Option<**String**> | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. |  |[default to tr]
**page** | Option<**i32**> |  |  |[default to 1]
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_list_supported_markets

> serde_json::Value yandex_list_supported_markets(prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List supported markets

Supported Yandex markets (domains, default region and language).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_reverse_image_search

> serde_json::Value yandex_reverse_image_search(image_url, domain, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**image_url** | **String** | Public URL of the image to reverse-search | [required] |
**domain** | Option<**String**> | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. |  |[default to tr]
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_web_search

> serde_json::Value yandex_web_search(query, domain, page, lr, lang, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search query, e.g. 'coffee machine' | [required] |
**domain** | Option<**String**> | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. |  |[default to tr]
**page** | Option<**i32**> |  |  |[default to 1]
**lr** | Option<**i32**> | Yandex region id, e.g. 213=Moscow, 84=USA |  |
**lang** | Option<**String**> | UI language: ru, en, tr, be, kk, uk |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_yandex_scraper_health_check

> serde_json::Value yandex_yandex_scraper_health_check()
Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_yandex_scraper_health_check_head

> serde_json::Value yandex_yandex_scraper_health_check_head()
Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

