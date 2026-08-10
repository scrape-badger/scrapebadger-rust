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

> serde_json::Value yandex_image_search(query, domain, page)
Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Image search query, e.g. 'coffee machine' | [required] |
**domain** | Option<**String**> | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. |  |[default to tr]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_list_supported_markets

> serde_json::Value yandex_list_supported_markets()
List supported markets

Supported Yandex markets (domains, default region and language).

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


## yandex_reverse_image_search

> serde_json::Value yandex_reverse_image_search(image_url, domain)
Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**image_url** | **String** | Public URL of the image to reverse-search | [required] |
**domain** | Option<**String**> | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. |  |[default to tr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yandex_web_search

> serde_json::Value yandex_web_search(query, domain, page, lr, lang)
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

