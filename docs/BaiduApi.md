# \BaiduApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baidu_baidu_image_search**](BaiduApi.md#baidu_baidu_image_search) | **GET** /v1/baidu/images | Baidu image search
[**baidu_baidu_news_search**](BaiduApi.md#baidu_baidu_news_search) | **GET** /v1/baidu/news | Baidu news search
[**baidu_baidu_scraper_health_check**](BaiduApi.md#baidu_baidu_scraper_health_check) | **GET** /v1/baidu/health | Baidu scraper health check
[**baidu_baidu_scraper_health_check_head**](BaiduApi.md#baidu_baidu_scraper_health_check_head) | **HEAD** /v1/baidu/health | Baidu scraper health check
[**baidu_baidu_web_search**](BaiduApi.md#baidu_baidu_web_search) | **GET** /v1/baidu/search | Baidu web search
[**baidu_search_suggestions**](BaiduApi.md#baidu_search_suggestions) | **GET** /v1/baidu/autocomplete | Search suggestions



## baidu_baidu_image_search

> serde_json::Value baidu_baidu_image_search(query, page)
Baidu image search

Baidu image search via the acjson JSON API.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**page** | Option<**i32**> | 30 images per page |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## baidu_baidu_news_search

> serde_json::Value baidu_baidu_news_search(query, page)
Baidu news search

Baidu news vertical — articles with source, publish date and real URLs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## baidu_baidu_scraper_health_check

> serde_json::Value baidu_baidu_scraper_health_check()
Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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


## baidu_baidu_scraper_health_check_head

> serde_json::Value baidu_baidu_scraper_health_check_head()
Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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


## baidu_baidu_web_search

> serde_json::Value baidu_baidu_web_search(query, page, num)
Baidu web search

Baidu web SERP — organic results with real target URLs, related searches, total count.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. '咖啡机' or 'coffee machine' | [required] |
**page** | Option<**i32**> | Result page (10 results per page) |  |[default to 1]
**num** | Option<**i32**> | Results per page (rn) |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## baidu_search_suggestions

> serde_json::Value baidu_search_suggestions(query)
Search suggestions

Baidu search-box suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. '咖啡' or 'coff' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

